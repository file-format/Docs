{
"ngày": "2023-06-08",
  "keywords": [
"tệp vmx",
"tệp vmx là gì",
"ví dụ về tệp vmx",
"cách mở tệp vmx",
"tệp vmx chứa gì",
"định dạng của tệp vmx là gì",
"tài liệu",
"phần mở rộng tệp vmx",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Định dạng tệp VMX - Tệp cấu hình máy ảo VMware",
  "description":"Tìm hiểu về định dạng VMX và các API có thể tạo và mở tệp VMX.",
  "linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
      "parent": "settings"
}
},
"lastmod": "2023-06-08"
}

## Tập tin VMX là gì?

Tệp VMX, còn được gọi là tệp cấu hình máy ảo, là một tệp văn bản thuần túy được phần mềm ảo hóa VMware sử dụng để xác định cài đặt và cấu hình của máy ảo (VM). Các tệp VMX chứa thông tin như cấu hình phần cứng của VM, ánh xạ đĩa ảo, cài đặt mạng và các tham số khác.

## Ví dụ về tệp VMX

Đây là một ví dụ về tệp VMX có thể trông như thế nào:

```
# version for configuration
config.version = "8"
# version for virtual machine (Regular version is 4)
virtualHW.version = "7"
# enable vnc
RemoteDisplay.vnc.enabled = "TRUE"
RemoteDisplay.vnc.port = "5900"
VMware, Inc. 3

# type of guest os
guestOS = "linux"
# display name for the VI Client/WebCenter
displayName = "RHEL3"
# scsi controller 0
scsi0.present = "true"
scsi0.virtualDev = "lsilogic"
# scsi hard drive
scsi0:0.present = "true"
scsi0:0.fileName = "/volumes/your-path/passthru.vmdk"
scsi0:0.deviceType = "scsi-hardDisk"
scsi0:0.redo = ""
# IDE CD drive
ide0:0.present ="true"
ide0:0.startConnected = "TRUE"
ide0:0.fileName = "/volumes/your-path/your-iso-image"
ide0:0.deviceType = "cdrom-image"
memsize = "512"
sched.mem.max = "512"
sched.mem.minsize = "512"
sched.swap.derivedName = "/volumes/your-path/passthru-12345.vswp"
svga.vramSize = "16777216"
```

## Tệp VMX chứa gì?

Tệp VMX chứa nhiều cài đặt cấu hình khác nhau cho máy ảo (VM). Dưới đây là một số cài đặt thường thấy trong tệp VMX:

- `.encoding:` Chỉ định mã hóa ký tự được sử dụng trong tệp.
- `config.version:` Cho biết phiên bản của định dạng tệp VMX.
- `virtualHW.version:` Chỉ định phiên bản của phần cứng ảo cho VM.
- `guestOS:` Chỉ định hệ điều hành khách được cài đặt trong VM.
- `memSize:` Xác định lượng bộ nhớ được phân bổ cho VM.
- `displayName:` Đặt tên hiển thị hoặc nhãn cho VM.
- `powerType:` Xác định hành vi nguồn điện cho các hoạt động khác nhau (tắt nguồn, bật nguồn, đặt lại, tạm dừng).
- `floppyX:` Các cài đặt cấu hình liên quan đến ổ đĩa mềm, chẳng hạn như sự hiện diện và ánh xạ tệp.
- `numvcpus:` Chỉ định số lượng CPU ảo được gán cho VM.
- `scsiX:` Cài đặt cấu hình cho bộ điều khiển SCSI và các ổ đĩa ảo được liên kết của chúng.
- `ethernetX:` Cài đặt cấu hình cho bộ điều hợp mạng, bao gồm loại thiết bị ảo, tên mạng và loại địa chỉ.
- `ideX:` Cài đặt cấu hình cho bộ điều khiển IDE và các ổ đĩa ảo được liên kết của chúng.
- `usbX:` Cài đặt cấu hình cho thiết bị USB, chẳng hạn như chi tiết hiện diện và kết nối.
- `sound:` Cài đặt cấu hình cho bộ điều hợp âm thanh ảo.
- `tools.syncTime:` Cho biết liệu đồng bộ hóa thời gian với hệ thống máy chủ có được bật hay không.
- `uuid.bios:` Chỉ định BIOS UUID của VM.
- `uuid.location:` Chỉ định vị trí UUID của VM.

## Làm cách nào để mở tệp VMX?

Không nên mở tệp VMX theo cách thủ công. Khi bạn chạy máy ảo bằng VMware Fusion, phần mềm sẽ tự động tải thông tin từ tệp VMX.

Tuy nhiên, nếu bạn muốn chỉnh sửa thủ công tệp VMX, bạn có thể thực hiện việc đó bằng bất kỳ trình soạn thảo văn bản nào, ví dụ Notepad (Windows) hoặc TextEdit (Mac).

## Định dạng của tệp VMX là gì?

Tệp VMX là một tệp văn bản thuần túy có định dạng cụ thể. Định dạng tuân theo cấu trúc cặp khóa-giá trị trong đó mỗi dòng thể hiện tùy chọn cấu hình riêng biệt.

Định dạng chung của tệp VMX như sau:

```
key1 = value1
key2 = value2
key3 = value3
```

Mỗi dòng bao gồm khóa theo sau là dấu bằng (=) và giá trị tương ứng. Khóa đại diện cho cài đặt cấu hình cụ thể và giá trị đại diện cho giá trị được gán cho cài đặt đó.

Ví dụ: `memSize = "8192"` trong tệp VMX chỉ định rằng giới hạn bộ nhớ Máy ảo là 8192MB RAM.

Định dạng của tệp VMX cũng có thể bao gồm các nhận xét, được biểu thị bằng dấu thăng (#) ở đầu dòng, phần mềm VMware bỏ qua khi phân tích cú pháp tệp. Nhận xét thường được sử dụng để cung cấp thêm thông tin hoặc giải thích cho các cài đặt cụ thể.

## Người giới thiệu
* [Tệp VMX mẫu](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




