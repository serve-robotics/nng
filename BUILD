# Currently ignoring tls/none, tls/mbedtls and transport/zerotier directories
# since we have no plans to need support for those features

cc_library(
    name = "nng",
    srcs = glob([
          "src/nng.c",
          "src/compat/nanomsg/*.c",
          "src/core/*.c",
          "src/platform/posix/*.c",
          "src/protocol/**/*.c",
          "src/supplemental/base64/*.c",
          "src/supplemental/http/*.c",
          "src/supplemental/sha1/*.c",
          "src/supplemental/tcp/*.c",
          "src/supplemental/util/*.c",
          "src/supplemental/tls/*.c",
          "src/supplemental/websocket/websocket.c",
          "src/transport/**/*.c",
      ],
      exclude = ["src/transport/zerotier/*.c"]
    ),
    hdrs = glob([
            "include/nng/nng.h",
            "include/nng/compat/nanomsg/*.h",
            "include/nng/protocol/**/*.h",
            "include/nng/supplemental/**/*.h",
            "include/nng/transport/**/*.h",
            "src/core/*.h",
            "src/platform/posix/*.h",
            "src/supplemental/**/*.h",
            # included because test/list.c depends on including this?
            "src/core/list.c",
            # included because test/idhash.c depends on including this?
            "src/core/idhash.c",
            # included because test/httpclient.c depends on including this?
            "src/supplemental/sha1/sha1.c"
        ],
        exclude = ["include/nng/transport/zerotier/*.h"],
    ),
    includes = [
      "include",
      "src",
    ],
    defines = [
        "NNG_PLATFORM_POSIX",
        "NNG_PLATFORM_DARWIN",
        "NNG_USE_ARC4_RANDOM",
    ],
    visibility = ["//visibility:public"],
)
