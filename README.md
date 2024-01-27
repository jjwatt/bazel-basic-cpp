# Basic Bazel C++ Starter repo

Keep the main branch at "modern" best practices (as best we
can tell from an outsider's perspective).

Start with content from the [Bazel Tutorial: Build a C++ Project]
(https://bazel.build/start/cpp) and split the stages of
that tutorial. `main` may stay at `stage1` of that tutorial.


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
