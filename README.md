# TED-GUI
TED-GUI is an extension of the TED program (https://github.com/maxng07/ted) with a Web Application GUI. HTML and Javascript is the frontend UI and interacts with TED binary in WebAssembly/WASM to encipher or decipher the Input text. The crypto operations happens locally within the broswer sandbox.

TED-GUI offers a Web based Graphical interface for user to input the parameters, and TED WASM will perform the crypto function either for enciper or decipher. The provided html and js is the web frontend that interacts with wasm. You can build your own html and use the provided wasm to perform encipher/decipher operations too.

TED-GUI with the html and js is able to support encipher/decipher of both single-byte and double-byte language with the current release. Verified and tested languages includes: English, Bahasa, Simplified Chinese, Japanese and Thai, representing both single and double byte language. Please feel free to report any languages that is not able to be encipher/decipher. If you intend to build your own html and use the wasm binary file, you can perform an encodeURI/decodeURI for double byte language. The ted wasm binary has the same logic as the ted binary and accept the same CLI inputs and one additional for text.

<b>Usage: </b></br>
You can download the html, js and wasm and run it with your own web servers or web storage. Some browsers like firefox supports allowing or disabling CORS, this will allow wasm to be completely loaded without a web server. It is also possible to build a local lightweight web server for the html and wasm to run locally.

Download the 3 files from <a href="https://github.com/maxng07/ted-gui/releases"> here </a><br>
<p>
  Tutorials are <a href="https://github.com/maxng07/ted-gui/tree/master/graphics"> here </a>
<p>
#Licensing
All RIGHTS RESERVED.

Filecrypt uses a GO package for AES-GCMSIV which has a copyright license as part of BoringSSL. The copyright notice as is below

/* Copyright (c) 2017, Google Inc. *

    This code was written to support development of BoringSSL and thus is
    considered part of BoringSSL and under the same license.
    Permission to use, copy, modify, and/or distribute this software for any
    purpose with or without fee is hereby granted, provided that the above
    copyright notice and this permission notice appear in all copies.
    THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
    WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
    MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY
    SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
    WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN ACTION
    OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF OR IN
    CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE. */
