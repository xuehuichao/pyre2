cc_binary(
    name = "_re2.so",
    srcs = ["_re2.cc"],
    deps = ["@re2//:re2"],
    linkstatic=0,
    linkshared=1,
    copts= ["-I/usr/include/python2.7"],
    linkopts=["-lpython2.7"]
)

py_library(
    name = "re2",
    srcs = ["re2.py"],
    data = [
        ":_re2.so"
    ],
    visibility = ["//visibility:public"],
)
