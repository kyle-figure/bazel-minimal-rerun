This repository shows a minimal working example of building [Rerun](https://www.rerun.io/) using Bazel and the `cmake` rule from `rules_foreign_cc`.

1. Open repo inside dev container
2. Build minimal C++ example: `bazel build //...`

Compatibility:

The Rerun 0.20.0 release updates C++ Arrow to 18.0.0, which has a build error when built through `rules_foreign_cc`.
Hence, this repo is stuck on 0.19.1 as the latest working Rerun version until a patch for C++ Arrow can be created.
