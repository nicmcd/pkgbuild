package(default_visibility = ["//visibility:public"])

licenses(["notice"])

cc_library(
    name = "numa_internal",
    srcs = [
        "config.h",
        "libnuma.c",
        "syscall.c",
        "distance.c",
        "affinity.c",
        "affinity.h",
        "sysfs.c",
        "sysfs.h",
        "rtnetlink.c",
        "rtnetlink.h",
        "numaint.h",
        "util.h",
    ],
    hdrs = [
        "numa.h",
        "numacompat1.h",
        "numaif.h",
    ],
    deps = [
        ":versions.ldscript",
    ],
    linkopts = [
        "-Wl,--version-script,$(location versions.ldscript)",
        "-Wl,-init,numa_init",
        "-Wl,-fini,numa_fini",
    ],
    visibility = ["//visibility:private"],
)

cc_library(
    name = "numa",
    hdrs = [
        "numa.h",
        "numacompat1.h",
        "numaif.h",
    ],
    include_prefix = "numa",
    deps = [":numa_internal"],
)
