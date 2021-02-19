licenses(["notice"])

cc_library(
    name = "zlib_internal",
    srcs = glob(["*.c"]),
    hdrs = glob(["*.h"]),
    copts = [
        "-w",
        "-Dverbosity=-1"
    ],
    includes = ["."],
    visibility = ["//visibility:private"],
)

cc_library(
    name = "zlib",
    hdrs = ["zlib.h"],
    deps = [":zlib_internal"],
    copts = [
        "-w",
        "-Dverbosity=-1"
    ],
    includes = ["."],
    include_prefix = "zlib",
    visibility = ["//visibility:public"],
)
