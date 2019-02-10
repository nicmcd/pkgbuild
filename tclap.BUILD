licenses(["notice"])

cc_library(
  name = "lib",
  hdrs = glob(["include/**/*.h"]),
  copts = [
    "-fexceptions",
  ],
  defines = [
    "HAVE_LONG_LONG=1",
    "HAVE_SSTREAM=1",
  ],
  includes = [
    "include",
  ],
  features = ["-parse_headers"],
  visibility = ["//visibility:public"],
)
