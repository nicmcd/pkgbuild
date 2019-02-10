licenses(["notice"])

cc_library(
  name = "lib",
  srcs = glob(["*.c"]),
  hdrs = glob(["*.h"]),
  copts = [
    "-w",
    "-Dverbosity=-1"
  ],
  includes = ["."],
  visibility = ["//visibility:public"],
)
