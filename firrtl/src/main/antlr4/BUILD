package(default_visibility = ["//visibility:public"])

load("@rules_antlr//antlr:antlr4.bzl", "antlr4")

antlr4(
    name = "firrtl_antlr4_srcs",
    srcs = ["FIRRTL.g4"],
    no_listener = False,
    package = "firrtl.antlr",
    visitor = True,
    deps = [
        "//src/main/java:LexerHelper",
        "@antlr3_runtime//jar",
        "@antlr4_runtime//jar",
        "@antlr4_tool//jar",
        "@javax_json//jar",
        "@stringtemplate4//jar",
    ],
)

java_library(
    name = "firrtl_antlr4_java_lib",
    srcs = [":firrtl_antlr4_srcs"],
    deps = [
        "//src/main/java:LexerHelper",
        "@antlr4_runtime//jar",
    ],
)

