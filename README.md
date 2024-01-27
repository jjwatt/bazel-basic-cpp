# Basic Bazel C++ Starter repo

I want to keep the main branch at "modern" best practices (as best I
can tell from an outsider's perspective). So, I don't think I want to
include dotfiles like .bazeliskrc or .bazelversion directly or even in
the main branch at all. They're confusing. We want the bare minimum,
and it's already a little confusing to have an empty
WORKSPACE.bazel. There's some other way to redirect, but I'll have to
find it in the manual again. I'll update this once I do.

I'll start with content from the [Bazel Tutorial: Build a C++ Project]
(https://bazel.build/start/cpp) and probably even split the stages of
that tutorial into branches to keep this main branch/example as simple
as possible.

## Running

This already works like this. [Install bazelisk](https://bazel.build/install/bazelisk) and start building C++!

```shell
$ bazel build //main:hello-world
jwatt@lasting-damage:~/git/github.com/jjwatt/bazel-basic-cpp$ bazel build //main:hello-world
2024/01/27 12:56:02 Downloading https://releases.bazel.build/7.0.2/release/bazel-7.0.2-linux-x86_64...
Downloading: 55 MB out of 55 MB (100%) 
Extracting Bazel installation...
Starting local Bazel server and connecting to it...
INFO: Analyzed target //main:hello-world (68 packages loaded, 309 targets configured).
INFO: Found 1 target...
Target //main:hello-world up-to-date:
  bazel-bin/main/hello-world
INFO: Elapsed time: 6.629s, Critical Path: 0.27s
INFO: 7 processes: 5 internal, 2 linux-sandbox.
INFO: Build completed successfully, 7 total actions
```

```shell
jwatt@lasting-damage:~/git/github.com/jjwatt/bazel-basic-cpp$ ./bazel-bin/main/hello-world
Hello world
Sat Jan 27 12:56:25 2024
```

```shell
jwatt@lasting-damage:~/git/github.com/jjwatt/bazel-basic-cpp$ file $_
./bazel-bin/main/hello-world: ELF 64-bit LSB executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[xxHash]=a246da035dfbb234, not stripped
```
