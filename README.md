# ted-gui
TED-GUI is an extension of the TED program (https://github.com/maxng07/ted) with a Web Application GUI. HTML and Javascript is the frontend UI and interacts with TED binary in WebAssembly/WASM to encipher or decipher the Input text. The crypto operations happens locally within the broswer sandbox.

TED-GUI offers a Web based Graphical interface for user to input the parameters, and TED WASM will perform the crypto function either for enciper or decipher. The provided html and js is the web frontend that interacts with wasm. You can build your own html and use the provided wasm to perform encipher/decipher operations too.

TED-GUI with the html and js is able to support encipher/decipher of both single-byte and double-byte language with the current release. If you intend to build your own html and use the wasm binary file, you can perform an encodeURI/decodeURI for double byte language. The ted wasm binary has the same logic as the ted binary and accept the same CLI inputs and one additional for text.

<b>Usage: </b></br>
You can download the html, js and wasm and run it with your own web servers or web storage. Some browsers like firefox supports allowing or disabling CORS, this will allow wasm to be completely loaded without a web server. It is also possible to build a local lightweight web server for the html and wasm to run locally.

Download the 3 files from <a href="https://github.com/maxng07/ted-gui/releases"> here </a><br>
<p>
  Tutorials are <a href="https://github.com/maxng07/ted-gui/tree/master/graphics"> here </a>
