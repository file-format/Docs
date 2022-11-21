{
  "date" : "2021-06-28",
  "keywords" :[ "file cgi", "apa itu file cgi", "file", "contoh cgi", "ekstensi file cgi", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file CGI dan API yang dapat membuat dan membuka file CGI.",
  "title" :"CGI - File Skrip Antarmuka Gateway Umum",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## Apa itu file CGI?
File CGI dikenal sebagai skrip Common Gateway Interface yang digunakan oleh server web untuk menjalankan program eksternal untuk memproses permintaan pengguna. Skrip yang disimpan dalam file dengan ekstensi .cgi biasanya ditulis dalam bahasa pemrograman C atau Perl. Itu telah diperkenalkan sejak awal Web, ketika pengembang Web ingin menghubungkan database ke server Web mereka. Server yang mendukung gateway umum antara server Web dan database sangat cocok untuk mengeksekusi kode CGI.

## Format File CGI
Skrip CGI digunakan oleh server Web untuk memfasilitasi pemilik untuk mengonfigurasi bagaimana URL akan ditangani. Prosedur ini biasanya dilakukan dengan menandai direktori baru (di mana sebagian besar dokumen berada) sebagai berisi skrip CGI; namanya yang umum dikenal adalah cgi-bin. Misalnya, /usr/local/apache/htdocs/cgi-bin dapat dipilih sebagai direktori CGI di server Web. Ketika browser Web meminta URL yang mengarah ke file di dalam direktori CGI, alih-alih hanya mengirim file itu (/id/usr/local/apache/htdocs/cgi-bin/printenv.pl) ke browser Web, HTTP server mengeksekusi skrip yang ditentukan dan mengembalikan keluaran skrip ke browser Web. Singkatnya, apa pun yang dikirim skrip CGI ke output standar ditransfer ke klien Web alih-alih ditampilkan di terminal jendela.

### Contoh CGI

Berikut skrip CGI yang ditulis dalam Perl yang menunjukkan semua variabel lingkungan yang diteruskan oleh server Web:
```
#!/usr/bin/env perl

=head1 DESCRIPTION

printenv — a CGI program that just prints its environment

=cut
print "Content-Type: text/plain\n\n";

for my $var ( sort keys %ENV ) {
    printf "%s=\"%s\"\n", $var, $ENV{$var};
}
```

Outputnya akan seperti berikut:
```
COMSPEC="C:\Windows\system32\cmd.exe"
DOCUMENT_ROOT="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/htdocs"
GATEWAY_INTERFACE="CGI/1.1"
HOME="/home/SYSTEM"
HTTP_ACCEPT="text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8"
HTTP_ACCEPT_CHARSET="ISO-8859-1,utf-8;q=0.7,*;q=0.7"
HTTP_ACCEPT_ENCODING="gzip, deflate, br"
HTTP_ACCEPT_LANGUAGE="en-us,en;q=0.5"
HTTP_CONNECTION="keep-alive"
HTTP_HOST="example.com"
HTTP_USER_AGENT="Mozilla/5.0 (Windows NT 6.1; WOW64; rv:67.0) Gecko/20100101 Firefox/67.0"
PATH="/home/SYSTEM/bin:/bin:/cygdrive/c/progra~2/php:/cygdrive/c/windows/system32:..."
PATHEXT=".COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC"
PATH_INFO="/foo/bar"
PATH_TRANSLATED="C:\Program Files (x86)\Apache Software Foundation\Apache2.4\htdocs\foo\bar"
QUERY_STRING="var1=value1&var2=with%20percent%20encoding"
REMOTE_ADDR="127.0.0.1"
REMOTE_PORT="63555"
REQUEST_METHOD="GET"
REQUEST_URI="/cgi-bin/printenv.pl/foo/bar?var1=value1&var2=with%20percent%20encoding"
SCRIPT_FILENAME="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/cgi-bin/printenv.pl"
SCRIPT_NAME="/cgi-bin/printenv.pl"
SERVER_ADDR="127.0.0.1"
SERVER_ADMIN="(server admin's email address)"
SERVER_NAME="127.0.0.1"
SERVER_PORT="80"
SERVER_PROTOCOL="HTTP/1.1"
SERVER_SIGNATURE=""
SERVER_SOFTWARE="Apache/2.4.39 (Win32) PHP/7.3.7"
SYSTEMROOT="C:\Windows"
TERM="cygwin"
WINDIR="C:\Windows"
```
## Penggunaan skrip CGI
File CGI yang berisi skrip CGI biasanya digunakan untuk memproses data masukan dari pengguna dan menghasilkan data keluaran yang relevan. Mengimplementasikan wiki adalah salah satu contoh program CGI. Jika agen pengguna mengirimkan permintaan untuk nama entri, server Web menjalankan program CGI. Program CGI mendapatkan sumber halaman entri itu, mengubahnya menjadi HTML, dan mencetak hasilnya. Server Web menerima output dari program CGI dan mengembalikannya ke agen pengguna. Kemudian, jika agen pengguna memanggil fungsi edit dengan mengklik tombol "Edit Halaman", program CGI akan menampilkan textarea HTML atau kontrol pengeditan lainnya dengan konten halaman. Terakhir, jika agen pengguna mengklik tombol "Publikasikan halaman", program CGI mengubah HTML yang diperbarui menjadi sumber halaman entri tersebut dan menyimpannya.



## Referensi

* [Antarmuka Common Gateway - oleh Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

