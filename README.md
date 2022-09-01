# nelua-gamercade

[Gamercade](https://gamercade.io/) bindings for [nelua](https://nelua.io/) language.

## Development and issue tracking

**The upstream development of this project is done at Codeberg**: https://codeberg.org/Andre-LA/nelua-gamercade

The issue tracking is done at github: https://github.com/Andre-LA/nelua-gamercade/issues

## Setup

First, of course, [install nelua](https://nelua.io/installing/).

You'll need a C compiler that generates an `.wasm` binary, for that, you should [install WASI-SDK](https://github.com/WebAssembly/wasi-sdk/#install).

> The important part is declaring the `CC` variable that points to the WASI's clang.

## Usage

Compile your nelua source code using `CC` variable as the C compiler:

```sh
# use nelua --help to get a better understanding about these flags:
$ nelua examples/pong.nelua -r --cc "$CC" -o build/pong.wasm
```

> --cc changes the C compiler, -r makes a release build (optional, but recommended), you propably want to use -o in order to make the wasm file easily accessible.

Then, follow [Gamercade's guide](https://github.com/gamercade-io/gamercade_console/#bundling-a-game-with-the-editor---how-to-create-a-gcrom-file) in order to
build and run the `gcrom` file.

## License

This projects is licensed under Zlib license.

