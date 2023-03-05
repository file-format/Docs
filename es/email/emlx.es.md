{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - Formato de archivo de correo de Apple",
  "description":"Obtenga información sobre el formato de archivo EMLX y las API que pueden crear y abrir archivos EMLX",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo EMLX?

Apple implementa y desarrolla el formato de archivo EMLX. La aplicación Apple Mail utiliza el formato de archivo EMLX para exportar los correos electrónicos. También hay otras aplicaciones que pueden abrir los archivos EMLX y convertirlos a otros formatos de archivo.

## Breve historia del formato de archivo EMLX

El sistema operativo Mac OS X adoptó el programa de correo electrónico existente, NeXTMail, creado por NeXT como parte del sistema operativo NeXTSTEP. Apple, después de adquirir NeXT, mejoró sus características y se convirtió en la aplicación de correo electrónico Apple Mail que ahora se usa como cliente de correo predeterminado. Los correos electrónicos exportados a través de Apple Mail se guardan directamente como archivos EMLX. Además, es el cliente de correo predeterminado para archivos EMLX cuando alguien los abre haciendo doble clic en Mac OS.

## Formato de archivo EMLX

Los archivos EMLx son archivos simples basados en texto que se pueden abrir en cualquier editor de texto como el Bloc de notas. La estructura del archivo EMLX consta de tres partes:

* Un recuento de bytes para el mensaje: longitud del mensaje en sí, escrito en ASCII en decimal, terminado en 0x0a
* El mensaje en sí
* Mensaje de metadatos en forma de plist XML

Estos se pueden explicar mejor con la ayuda del siguiente correo electrónico de muestra extraído de Apple Mail como EMLX y abierto en un editor de texto.

### Ejemplo de EMLX

```
875       
X-Spam-Checker-Version: SpamAssassin 3.3.2 (2011-06-06) on ******.*********.***
X-Spam-Level:
X-Spam-Status: No, score#-3.2 required#4.2 tests#BAYES_00,RP_MATCHES_RCVD,
        SPF_PASS,TVD_SPACE_RATIO autolearn#ham version#3.3.2
Received: from [127.0.0.1](******.*********.*** [***.**.**.**])
        by ******.*********.*** (8.14.5/8.14.5) with ESMTP id r2TN8m4U099571
        for <****@*********.***>; Fri, 29 Mar 2013 19:08:48 -0400 (EDT)
        (envelope-from ****@*********.***)
Subject: very simple
From: Sender <****@*********.***>
Content-Type: text/plain; charset#us-ascii
Message-Id: <4E83618E-BB56-404F-8595-87352648ADC7@*********.***>
Date: Fri, 29 Mar 2013 19:09:06 -0400
To: Reciever <****@*********.***>
Content-Transfer-Encoding: 7bit
Mime-Version: 1.0 (Apple Message framework v1283)
X-Mailer: Apple Mail (2.1283)

message Foo
--
Sender
http://www.la-grange.net/karl/

<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version#"1.0">
<dict>
        <key>date-sent</key>
        <real>1364598546</real>
        <key>flags</key>
        <integer>8590195713</integer>
        <key>original-mailbox</key>
        <string>imap://********@127.0.0.1:11143/mail/2013/03</string>
        <key>remote-id</key>
        <string>41147</string>
        <key>subject</key>
        <string>very simple</string>
</dict>
</plist>
```

En este ejemplo, el 875 muestra la longitud total del mensaje. Los metadatos del mensaje se incluyen en el<plist> Las etiquetas y las banderas se describen a continuación:

|Campo|Descripción|Valor
---|---|---|
|0|leer|1 << 0
|1|borrado|1 << 1
|2|respondido|1 << 2
|3|cifrado|1 << 3
|4|marcado|1 << 4
|5|reciente|1 << 5
|6|borrador|1 << 6
|7|inicial (ya no se usa)|1 << 7
|8|reenviado|1 << 8
|9|redireccionado|1 << 9
|10-15|recuento de archivos adjuntos|3F << 10 (6 bits)
|16-22|nivel de prioridad|7F << 16 (7 bits)
|23|firmado|1 << 23
|24|es basura|1 << 24
|25|no es basura|1 << 25
|26-28|tamaño de fuente delta|7 << 26 (3 bits)
|29|nivel de correo no deseado registrado|1 << 29
|30|resaltar texto en toc|1 << 30
|31|(sin usar)|

## Ver también ##

* [EML](/es/correo electrónico/eml/)
* [Mensaje](/es/correo electrónico/mensaje/)

