{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "LZ - Lzip Compressed File Format",
  "description":"Learn about LZ file format and APIs that can create and open LZ files.",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-19"
}

## What is an LZ file?

A file with .lz extension is a compressed archive file created with Lzip, which is a free command-line tool for compression. It supports concatenation to compress support files. LZ files have media type application/lzip and support higher compression rations than [BZ2](/compression/bz2). LZ are based on the LZMA (Lempel-Ziv-Markov chain) algorithm and include a 32-bit CRC checksum and ident bytes for checking the integrity of the file.

## LZMA Compressed Format

The LZMA compressed format consists of a compressed stream of bits that is encoded using adaptive binary range coder. The stream is divided into packets. Each packet describes either a single byte or an LZ77 sequence. The length and distance of each packet is implicitly or explicitly encoded.

The seven types of packets are as follow ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Packed code (bit sequence)	|Packet name	|Packet description|
---|---|---|
|0 + byteCode|	LIT|	A single byte encoded using an adaptive binary range coder.|
|1+0 + len + dist|	MATCH|	A typical LZ77 sequence describing sequence length and distance.|
|1+1+0+0|	SHORTREP|	A one-byte LZ77 sequence. Distance is equal to the last used LZ77 distance.|
|1+1+0+1 + len|	LONGREP[0]|	An LZ77 sequence. Distance is equal to the last used LZ77 distance.|
|1+1+1+0 + len|	LONGREP[1]|	An LZ77 sequence. Distance is equal to the second last used LZ77 distance.|
|1+1+1+1+0 + len|	LONGREP[2]|	An LZ77 sequence. Distance is equal to the third last used LZ77 distance.|
|1+1+1+1+1 + len|	LONGREP[3]|	An LZ77 sequence. Distance is equal to the fourth last used LZ77 distance.|


## References

* [LZMA - Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://en.wikipedia.org/wiki/Lzip)
