# ted-gui
TED-GUI is an extension of TED program with a Web Application GUI. HTML and Javascript is the frontend UI and interacts with TED binary in WebAssembly/WASM to encipher or decipher the Input text. The crypto operations happens locally within the broswer sandbox.

TED-GUI offers a Web based Graphical interface for user to input the parameters, and TED WASM will perform the crypto function either for enciper or decipher. The provided html and js is the web frontend that interacts with wasm. 

<b>Usage: </b></br>
You can download the html, js and wasm and run it with your own web servers or web storage. Some browsers like firefox supports allowing or disabling CORS, this will allow wasm to be completely loaded without a web server. It is also possible to build a local lightweigh web server for the html and wasm to run locally.
