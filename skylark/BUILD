licenses(["notice"])  # Apache 2.0

package(default_visibility = ["//visibility:public"])

load("@bazel_skylib//:skylark_library.bzl", "skylark_library")
load("//skylark:skylark.bzl", "skylark_doc")
load("//skylark:skydoc.bzl", "skydoc")

skylark_library(
    name = "skydoc_lib",
    srcs = ["skydoc.bzl"],
    deps = [
        "@bazel_skylib//:skylark_library",
    ],
)

skylark_doc(
    name = "skylark-docs",
    srcs = ["skylark.bzl"],
    overview = False,
    strip_prefix = "skylark",
    deps = [":skylark"],
)

skydoc(
    name = "skydoc_doc",
    target_file = ":skydoc.bzl",
    deps = [":skydoc_lib"],
    rule_names = ["skydoc"],
    out = "skydoc_doc.md",
)
