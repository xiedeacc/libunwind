workspace(name = "libunwind")

load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository", "new_git_repository")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "bazel_skylib",
    sha256 = "de9d2cedea7103d20c93a5cc7763099728206bd5088342d0009315913a592cc0",
    strip_prefix = "bazel-skylib-1.4.2",
    urls = [
        "https://github.com/bazelbuild/bazel-skylib/archive/refs/tags/1.4.2.tar.gz",
    ],
)

http_archive(
    name = "platforms",
    sha256 = "1626b708a06989c2365f3101c9c937153e03ee39faaaeab98a2c204e9d015a0d",
    strip_prefix = "platforms-0.0.6",
    urls = [
        "https://github.com/bazelbuild/platforms/archive/refs/tags/0.0.6.tar.gz",
    ],
)

http_archive(
    name = "bazel_gazelle",
    sha256 = "f795b82792edeb03a7a060a908bc2cfc9702273b1387479fb99d208e83a3d7ad",
    strip_prefix = "bazel-gazelle-0.32.0",
    urls = [
        "https://github.com/bazelbuild/bazel-gazelle/archive/refs/tags/v0.32.0.tar.gz",
    ],
)

http_archive(
    name = "rules_cc",
    sha256 = "ae46b722a8b8e9b62170f83bfb040cbf12adb732144e689985a66b26410a7d6f",
    strip_prefix = "rules_cc-0.0.8",
    urls = [
        "https://github.com/bazelbuild/rules_cc/archive/refs/tags/0.0.8.tar.gz",
    ],
)

http_archive(
    name = "rules_foreign_cc",
    sha256 = "2a4d07cd64b0719b39a7c12218a3e507672b82a97b98c6a89d38565894cf7c51",
    strip_prefix = "rules_foreign_cc-0.9.0",
    urls = [
        "https://github.com/bazelbuild/rules_foreign_cc/archive/refs/tags/0.9.0.tar.gz",
    ],
)

http_archive(
    name = "rules_proto",
    sha256 = "dc3fb206a2cb3441b485eb1e423165b231235a1ea9b031b4433cf7bc1fa460dd",
    strip_prefix = "rules_proto-5.3.0-21.7",
    urls = [
        "https://github.com/bazelbuild/rules_proto/archive/refs/tags/5.3.0-21.7.tar.gz",
    ],
)

http_archive(
    name = "rules_perl",
    sha256 = "391edb08802860ba733d402c6376cfe1002b598b90d2240d9d302ecce2289a64",
    strip_prefix = "rules_perl-7f10dada09fcba1dc79a6a91da2facc25e72bd7d",
    urls = [
        "https://github.com/bazelbuild/rules_perl/archive/7f10dada09fcba1dc79a6a91da2facc25e72bd7d.tar.gz",
    ],
)

http_archive(
    name = "rules_python",
    sha256 = "94750828b18044533e98a129003b6a68001204038dc4749f40b195b24c38f49f",
    strip_prefix = "rules_python-0.24.0",
    urls = [
        "https://github.com/bazelbuild/rules_python/archive/refs/tags/0.24.0.tar.gz",
    ],
)

http_archive(
    name = "rules_java",
    sha256 = "c1b830ba7671557990b3d4de32fbb814d5bf652ddce83c0161710f7c1d8150f4",
    strip_prefix = "rules_java-6.2.2",
    urls = [
        "https://github.com/bazelbuild/rules_java/archive/refs/tags/6.2.2.tar.gz",
    ],
)

http_archive(
    name = "build_bazel_rules_swift",
    sha256 = "104b16612b1084918d58083b3ee2f6521eb202b4502019870da7351d10a4777f",
    strip_prefix = "rules_swift-1.9.1",
    urls = [
        "https://github.com/bazelbuild/rules_swift/archive/refs/tags/1.9.1.tar.gz",
    ],
)

http_archive(
    name = "build_bazel_rules_apple",
    sha256 = "d6735ed25754dbcb4fce38e6d72c55b55f6afa91408e0b72f1357640b88bb49c",
    strip_prefix = "rules_apple-2.5.0",
    urls = [
        "https://github.com/bazelbuild/rules_apple/archive/refs/tags/2.5.0.tar.gz",
    ],
)

http_archive(
    name = "build_bazel_apple_support",
    sha256 = "c02a8c902f405e5ea12b815f426fbe429bc39a2628b290e50703d956d40f5542",
    strip_prefix = "apple_support-1.8.0",
    urls = [
        "https://github.com/bazelbuild/apple_support/archive/refs/tags/1.8.0.tar.gz",
    ],
)

http_archive(
    name = "io_bazel_rules_docker",
    sha256 = "91844808532e5ce316b3c010929493c0244f3d37593afd6de04f71821d5136d9",
    strip_prefix = "rules_docker-0.25.0",
    urls = [
        "https://github.com/bazelbuild/rules_docker/archive/refs/tags/v0.25.0.tar.gz",
    ],
)

http_archive(
    name = "io_bazel_rules_go",
    sha256 = "12c67b212c865b884a180bd02e573c7a58c60bc2a7fb095475e24dccd9ee28f8",
    strip_prefix = "rules_go-0.41.0",
    urls = [
        "https://github.com/bazelbuild/rules_go/archive/refs/tags/v0.41.0.tar.gz",
    ],
)

http_archive(
    name = "rules_pkg",
    sha256 = "360c23a88ceaf7f051abc99e2e6048cf7fe5d9af792690576554a88b2013612d",
    strip_prefix = "rules_pkg-0.9.1",
    url = "https://github.com/bazelbuild/rules_pkg/archive/refs/tags/0.9.1.tar.gz",
)

http_archive(
    name = "rules_jvm_external",
    sha256 = "f36441aa876c4f6427bfb2d1f2d723b48e9d930b62662bf723ddfb8fc80f0140",
    strip_prefix = "rules_jvm_external-5.3",
    urls = ["https://github.com/bazelbuild/rules_jvm_external/archive/5.3.tar.gz"],
)

http_archive(
    name = "com_grail_bazel_compdb",
    sha256 = "4c8a45853a4239faa34a3f09d3b8dd0bc69e3674b1bf6bbfbb53c1ff18eea3c3",
    strip_prefix = "bazel-compilation-database-bc8a4da42f39b13fc298428837bf2a87e5bcd704",
    urls = [
        "https://github.com/grailbio/bazel-compilation-database/archive/bc8a4da42f39b13fc298428837bf2a87e5bcd704.tar.gz",
    ],
)

http_archive(
    name = "cpplint",
    build_file = "//bazel:cpplint.BUILD",
    sha256 = "ddc50661b62103376675d6e4bcaa85745fa523343c3d93a1f774685005f9afb3",
    strip_prefix = "cpplint-7b88b68187e3516540fab3caa900988d2179ed24",
    urls = [
        "https://github.com/cpplint/cpplint/archive/7b88b68187e3516540fab3caa900988d2179ed24.tar.gz",
    ],
)

http_archive(
    name = "lzma",
    sha256 = "e684e1c3652f5ce760930d5073ae867243578d6ad056aef4072d6d02316b9f6a",
    strip_prefix = "xz-515d98d55120baca0ebd55563a993ba5b102b38b",
    urls = [
        "https://github.com/xiedeacc/xz/archive/515d98d55120baca0ebd55563a993ba5b102b38b.tar.gz",
    ],
)

http_archive(
    name = "zlib",
    sha256 = "6fbf43f4658bc6048f3f4beca2f7cf7cbfc9ad1380335208875866d279b41528",
    strip_prefix = "zlib-ff644470d69a58407f49eaaa6236faef6786000a",
    urls = [
        "https://github.com/xiedeacc/zlib/archive/ff644470d69a58407f49eaaa6236faef6786000a.tar.gz",
    ],
)

load("@bazel_skylib//lib:versions.bzl", "versions")

versions.check("5.2.0")

load("@rules_foreign_cc//foreign_cc:repositories.bzl", "rules_foreign_cc_dependencies")
load("@rules_proto//proto:repositories.bzl", "rules_proto_dependencies", "rules_proto_toolchains")
load("@rules_perl//perl:deps.bzl", "perl_register_toolchains")
load("@io_bazel_rules_go//go:deps.bzl", "go_register_toolchains", "go_rules_dependencies")
load("@rules_pkg//:deps.bzl", "rules_pkg_dependencies")
load("@com_grail_bazel_compdb//:deps.bzl", "bazel_compdb_deps")

rules_foreign_cc_dependencies()

rules_proto_dependencies()

rules_proto_toolchains()

perl_register_toolchains()

go_rules_dependencies()

go_register_toolchains(version = "1.18")

rules_pkg_dependencies()

bazel_compdb_deps()
