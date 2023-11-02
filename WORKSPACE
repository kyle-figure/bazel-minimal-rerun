workspace(name = "com_github_bazel_minimal_rerun")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_cc",
    sha256 = "eb389b5b74862a3d310ee9d6c63348388223b384ae4423ff0fd286fcd123942d",
    strip_prefix = "rules_cc-0.0.7",
    urls = ["https://github.com/bazelbuild/rules_cc/releases/download/0.0.7/rules_cc-0.0.7.tar.gz"],
)

http_archive(
    name = "rules_foreign_cc",
    sha256 = "2a4d07cd64b0719b39a7c12218a3e507672b82a97b98c6a89d38565894cf7c51",
    strip_prefix = "rules_foreign_cc-0.9.0",
    url = "https://github.com/bazelbuild/rules_foreign_cc/archive/0.9.0.tar.gz",
)

load("@rules_foreign_cc//foreign_cc:repositories.bzl", "rules_foreign_cc_dependencies")

rules_foreign_cc_dependencies()

http_archive(
    name = "rerun",
    build_file = "@//:third_party/rerun/build_file.bazel",
    patch_args = ["-p1"],
    patches = ["@//:third_party/rerun/patches/cmake.patch"],
    sha256 = "3193894a15d2675e0fd8d58a07207776cef0f5214b8495818a42ea04e50616cd",
    strip_prefix = "rerun_cpp_sdk",
    url = "https://github.com/rerun-io/rerun/releases/download/0.10.1/rerun_cpp_sdk.zip",
)
