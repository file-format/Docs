{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "확장자", "파일", "포맷", "시스템", "MemoryDump", "미니덤프", "프로그램", "컴퓨터", "응용 프로그램"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - 메모리 덤프 파일 형식",
  "description":"DMP 파일 형식과 DMP 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## .DMP 파일이란? ##

DMP 파일은 주로 MemoryDump 또는 Minidump 파일 형식과 연결됩니다. Microsoft Windows 운영 체제에서 컴퓨터의 메모리 공간에서 덤프된 데이터를 저장하는 데 사용됩니다. 일반적으로 DMP 파일은 파일이 충돌하거나 오류가 발생하면 생성됩니다. 때때로 DMP 파일은 기술 전문가 또는 고급 컴퓨터 사용자가 직면한 문제를 해결하고 모든 종류의 응용 프로그램 문제를 해결하는 데 매우 중요합니다. DMP 파일은 운영 체제에서 시스템에 설치된 모든 응용 프로그램을 디버깅하는 데 사용되는 독점 형식으로 Microsoft에 저장됩니다.


## DMP 파일 형식의 기술 사양

Windows에서 "savedump.exe" 시스템 도구는 .dmp 파일을 생성한 다음 사용 가능한 다양한 디버깅 유틸리티에서 처리할 수 있습니다. 미니 덤프(64/128Kb)는 Windows에 의해 '%SystemRoot%\Minidump' 디렉토리에 저장됩니다. 반면에 커널 메모리와 전체 메모리 덤프는 시스템 루트에 'Memory.dmp' 파일로 저장됩니다. 메모리 덤프 파일은 비교적 큰 파일이므로 충분한 저장 공간을 차지할 수 있습니다. 따라서 문제 해결에 유용하지 않다고 생각되는 쓸모없는 .dmp 파일은 삭제하는 것이 좋습니다.

.dmp 파일은 수동으로 삭제하거나 컴퓨터의 기본 "디스크 정리 마법사"를 사용하여 삭제할 수 있습니다. DMP 확장은 Oracle 데이터베이스 제품에서 생성 및 사용되는 백업 및 복구 데이터베이스 파일의 .dmp 파일을 사용하는 데 사용됩니다. Oracle에서 생성한 DMP 파일은 데이터베이스 서버를 통해 실행 중인 데이터베이스 인스턴스로 가져오거나 복원하는 데 사용할 수 있는 데이터베이스 백업입니다. 대부분의 경우 .dmp 파일에는 파일 이름으로 시간 및 날짜 스탬프가 있습니다.

### DMP 파일 내용

메모리 덤프 파일에는 다음이 포함됩니다.

* stop 문과 그 매개변수;
* 로드된 드라이버 목록;
* Windows의 정상 작동을 중단시킨 프로세스에 대한 프로세서 컨텍스트(PRCB);
* 중단된 프로세스에 대한 커널 컨텍스트 및 프로세서 정보(EPROCESSES)
* 중단된 스레드에 대한 커널 컨텍스트 및 프로세서 정보(ETHREAD)
* 프로세스 수행을 종료한 스레드에 대한 커널 모드 호출 스택.


## DMP 예

중지 오류 0XC0000218(Registry_File_Failure)은 다음과 같이 DMP 파일을 생성합니다.

```
Symbol search path is: srv*
Executable search path is:
Windows XP Kernel Version 2600 (Service Pack 1) UP Free x86 compatible
Product: WinNt, suite: TerminalServer SingleUserTS
Built by: 2600.xpsp2.030422-1633
Kernel base = 0x804d4000 PsLoadedModuleList = 0x80543530
Debug session time: Fri Jun 11 10:22:46 2004
System Uptime: 0 days 0:00:24.187
Loading Kernel Symbols
.................................................
Loading unloaded module list

Loading User Symbols
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Use !analyze -v to get detailed debugging information.

BugCheck C0000218, {e144c418, 0, 0, 0}

Probably caused by : ntoskrnl.exe ( nt!ExRaiseHardError+13c )

Followup: MachineOwner
---------

kd> !analyze -v
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Unknown bugcheck code (c0000218)
Unknown bugcheck description
Arguments:
Arg1: e144c418
Arg2: 00000000
Arg3: 00000000
Arg4: 00000000

Debugging Details:
------------------


BUGCHECK_STR: 0xc0000218

ERROR_CODE: (NTSTATUS) 0xc0000218 - {Registry File Failure} The registry cannot load the hive (file): %hs or its log or alternate. It is corrupt, absent, or not writable.

DEFAULT_BUCKET_ID: DRIVER_FAULT

LAST_CONTROL_TRANSFER: from 8062be87 to 804f4103

STACK_TEXT:
f96f0870 8062be87 0000004c c0000218 f96f09d4 nt!KeBugCheckEx+0x19
f96f0a20 805e9f96 c0000218 00000001 00000001 nt!ExpSystemErrorHandler+0x44c
f96f0bcc 805ea21c c0000218 00000001 00000001 nt!ExpRaiseHardError+0x9a
f96f0c3c 805fb94c c0000218 00000001 00000001 nt!ExRaiseHardError+0x13c
f96f0dac 805aa2b6 00000000 00000000 00000000 nt!CmpLoadHiveThread+0x16a
f96f0ddc 805319c6 805fb7e2 00000001 00000000 nt!PspSystemThreadStartup+0x34
00000000 00000000 00000000 00000000 00000000 nt!KiThreadStartup+0x16


FOLLOWUP_IP:
nt!ExRaiseHardError+13c
805ea21c 837dfc00 cmp dword ptr [ebp-0x4],0x0

SYMBOL_STACK_INDEX: 3

FOLLOWUP_NAME: MachineOwner

SYMBOL_NAME: nt!ExRaiseHardError+13c

MODULE_NAME: nt

IMAGE_NAME: ntoskrnl.exe

DEBUG_FLR_IMAGE_TIMESTAMP: 3ea80977

STACK_COMMAND: kb

BUCKET_ID: 0xc0000218_nt!ExRaiseHardError+13c

Followup: MachineOwner

```

## 참조 ##

* [DMP - 마이크로소프트](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

