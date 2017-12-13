# SHA-1 is dead (Crypto, 100 points)

```
SHA-1 is dead http://sha1.pwn.seccon.jp/ Upload two files satisfy following conditions:

    file1 != file2
    SHA1(file1) == SHA1(file2)
    SHA256(file1) <> SHA256(file2)
    2017KiB < sizeof(file1) < 2018KiB
    2017KiB < sizeof(file2) < 2018KiB

    1KiB = 1024 bytes
```

## Writeup

First thing was to look up at google on how to generate to different files with the same SHA-1.

We soon learned about shattered.io[1], a research by the  Cryptology Group at Centrum Wiskunde & Informatica (CWI) and Google, on how it is possible to create a SHA-1 collision.

With this new knowledge and a few more minutes googling, we found this tool ([sha1collider
](https://github.com/nneonneo/sha1collider)) and trough some trial and error we finally got the the right file size.

But you could've simply downloaded the PDF files at shatered.io and added the same byte stream to both files.

## Tools

* [sha1collider](https://github.com/nneonneo/sha1collider)

## Sources

* [1] ["Shattered"](https://shattered.io/)
