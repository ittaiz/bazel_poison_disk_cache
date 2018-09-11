workspace(name = "foo")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
rules_scala_version="ff3eb9b852eaa5923208d7f197c8053f5c0b4a8c" # update this as needed
rules_scala_version_sha256="fb25860e3e03938f73ae4ba6e2feb1dc422dd5b8b2abf21de87aade3450c1851"
http_archive(
             name = "io_bazel_rules_scala",
             url = "https://github.com/bazelbuild/rules_scala/archive/%s.zip"%rules_scala_version,
             type = "zip",
             strip_prefix= "rules_scala-%s" % rules_scala_version,
             #sha256 = rules_scala_version_sha256,
)


load("@bazel_tools//tools/build_defs/repo:git.bzl","git_repository")

load("@io_bazel_rules_scala//scala:scala.bzl", "scala_repositories")
scala_repositories()

load("@io_bazel_rules_scala//scala:toolchains.bzl", "scala_register_toolchains")
scala_register_toolchains()

