package(default_visibility = ["//visibility:public"])

cc_library(
    name = "dcurl",
    copts = [
        "-O3",
        "-msse2",
        "-DENABLE_SSE",
    ],
    linkopts = ["-lpthread"],
    srcs = ["src/%s" % x for x in [
        "common.c",
        "constants.c",
        "curl.c",
        "dcurl.c",
        "implcontext.c",
        "pow_sse.c",
        "trinary.c",
    ]],
    hdrs = ["src/%s" % x for x in [
        "curl.h",
        "common.h",
        "constants.h",
        "cpu-utils.h",
        "dcurl.h",
        "implcontext.h",
        "list.h",
        "pow_sse.h",
        "trinary.h",
    ]],
    strip_include_prefix = "src",
)
