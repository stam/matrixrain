# matrixrain

A Quil sketch designed to animate the green rain from the movie "The Matrix".

## Installation

Prerequisites:

- [JVM](https://www.oracle.com/technetwork/java/javase/downloads/index.html) installed
- [Leiningen](https://leiningen.org) installed

In a terminal:

``` bash
git clone <this repo>
cd matrixrain
```

## Usage

Run `lein figwheel` in your terminal. Wait for a while until you see
`Successfully compiled "resources/public/js/main.js"`. Open
[localhost:3449](http://localhost:3449) in your browser. The REPL in your
terminal is now connected to your browser. (You can test this by sending this
form: `(js/alert "Hello World!")` ). All the forms you enter in the REPL will be
compiled on the fly, send to the browser, evaluated in the browser and the
result will show up back in your terminal. You're fully connected to your
program in the browser.

You can use this while developing your sketch. Whenever you save your source
files the browser will automatically refresh everything, providing you with
quick feedback. For more information about Figwheel, check the [Figwheel
repository on GitHub](https://github.com/bhauman/lein-figwheel).

You can stop the REPL (and the connection with the browser) by evaluating this:
`:repl/quit`

## Publishing

Run `lein do clean, cljsbuild once optimized`.
This will compile your code and run Google Closure Compiler with advanced
optimizations. Take `resources/public/index.html` and
`resources/public/js/main.js` and upload them to server of your choice.

## License

Use the code the way you want at your own risk. It is not copyrighted.
