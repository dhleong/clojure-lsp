# Building

## GraalVM

Every release, the native binaries (Windows, Linux and MacOS) are compiled with __GraalVM__ and uploaded to Github releases page.

To build a native image with GraalVM:

- Install the GraalVM 22.0.0.2 for Java 11 and set the `GRAALVM_HOME` to the installation dir. 
- Install `native-image` with `$GRAALVM_HOME/bin/gu install native-image`. 
- Unix: Run from `clojure-lsp` project root `make native-cli`
- Windows: `cd cli && ./graalvm/native-windows-compile.bat`. 

The build may take some minutes and the result will be a `./clojure-lsp` native binary.

## Debug / development

Run `make` or `make debug-cli`.

## Jar

### Editor/CLI

Run `make cli-jar` for building the jar to be used with LSP protocol in a editor or CLI.

### JVM API

Run `make lib-jar` for building the jar to be used on JVM via API.

