# <img src="https://github.com/maxng07/ted/blob/master/mi.png"> TED-GUI 
TED-GUI is an extension of the TED program (https://github.com/maxng07/ted) with a Web Application GUI. The HTML and Javascript provides the frontend User interface and interacts with TED binary in WebAssembly/WASM to encipher or decipher the Input text. The crypto operation happens locally within the web broswer sandbox. TED-GUI with the TED binary WebAssembly/WASM is also capable of performing field encryption for any data inputs in a HTML. More details below and in the <a href="https://github.com/maxng07/ted-gui/wiki"> Wiki </a> Page.

TED-GUI offers a Web based Graphical interface for user to input the parameters, and TED WASM will perform the crypto function either for enciper or decipher. The provided html and js is the web frontend that interacts with wasm. You can build your own html and use the provided wasm to perform encipher/decipher operations too.

TED-GUI with the html and js is able to support encipher/decipher of both single-byte and double-byte language with the current release. Verified and tested languages includes: English, Bahasa, Simplified Chinese, Japanese and Thai, representing both single and double byte language. Please feel free to report any languages that is not able to be encipher/decipher. If you intend to build your own html and use the wasm binary file, you can perform an encodeURI/decodeURI for double byte language. The ted wasm binary has the same logic as the ted binary and accept the same CLI inputs and one additional for text.

<b>Usage: </b></br>
You can download the html, js and wasm and run it with your own web servers or web storage. Some browsers like firefox supports allowing or disabling CORS, this will allow wasm to be completely loaded without a web server by accessing the html. It is also possible to build a local lightweight web server for the html and wasm to run locally, an option is to use <a href="https://github.com/maxng07/Lightweight-Web-Server"> LWS - Lightweight Web Server </a>. LWS will be able to set wasm as Application/WASM in the Content Type in the HTTP header. Some web browsers like Firefox will not load if this is not set correctly.

Download the 3 files from <a href="https://github.com/maxng07/ted-gui/releases"> here </a><br>
<p>
Tutorials are <a href="https://github.com/maxng07/ted-gui/tree/master/graphics"> here </a>
<p>

I have also written up an Overview of how TED-GUI works, the information allowing you to build your own HTML and WebApp, utilising ted-wb wasm. Be sure to check out the <a href="https://github.com/maxng07/ted-gui/wiki"> Wiki </a> Page.
<p>
 
Graphical view of accessing TED-GUI off LWS, notice that html, js and wasm is loaded off the server. Each Text Encipher/Decipher is handle locally within the browser by TED wasm, nothing is send to the server despite loading off LWS.
<img src="https://github.com/maxng07/Lightweight-Web-Server/blob/master/graphics/webserver2.png"> <p>
<img src="https://github.com/maxng07/Lightweight-Web-Server/blob/master/graphics/webserver.png">

<p>
<h2> Additional Use-Case </h2>
<h3>Field Encryption for Sensitive and Confidential data</h3>
Using TED WASM for Field Encryption of sensitive data or confidential data in forms before POSTING it in HTTPS/TLS to Content Distribution Network or the Origin Server. Data such as Credit card details commonly needed for payment, Personal identifiable number can remain encrypted at rest, until the Application that handles it, decrypts the data. A good example would be Credit Card details for payment. Typically a user's credit card details will be send back in HTTPS/TLS, an encrypted tunnel in transit. Data may go through several intermediaries like reverse proxy (CDN), gateway, loadbalancer before reaching the Origin Server for storage and later processing. All these through the Internet Peering. In the example below, Credit Card Details are send to the local wasm binary for encryption and the return encrypted data output is then send back to the Payment Gateway or Server ensuring the User's Credit Card details are encrypted at rest and storage in addition to HTTPS/TLS transit. Only the processing application with the right keys can decipher the data.
<p>

 <img src="https://github.com/maxng07/ted-gui/blob/master/doc/field_encryption/cc1.jpg">
<p>
<h2>Licensing </h2>
All RIGHTS RESERVED.

TED-GUI also uses a GO package for AES-GCMSIV which has a copyright license as part of BoringSSL. The copyright notice as is below

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
