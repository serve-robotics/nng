# Currently ignoring tls, tls/mbedtls and transport/zerotier directories
# since we have no plans to need support for those features

# Currently, this supports darwin and linux platforms only. Windows support
# and all other other linux flavors have been removed for now since they
# are not applicable to us.

# The platform specific defines are a best effort stab at which define flags
# need to be passed to the compiler. The flags were identified by running cmake
# and looking at the default Makefile flags that were generated on MacOS and
# Ubuntu 16.04.

# Platform posix_* includes are listed explicitly because select() statements
# are not allowed within glob's =\

cc_library(
    name = "nng",
    srcs = glob(
        [
            "src/nng.c",
            "src/compat/nanomsg/*.c",
            "src/core/*.c",
            "src/platform/posix/posix_alloc.c",
            "src/platform/posix/posix_atomic.c",
            "src/platform/posix/posix_clock.c",
            "src/platform/posix/posix_config.c",
            "src/platform/posix/posix_debug.c",
            "src/platform/posix/posix_file.c",
            "src/platform/posix/posix_ipcconn.c",
            "src/platform/posix/posix_ipcdial.c",
            "src/platform/posix/posix_ipclisten.c",
            "src/platform/posix/posix_pipe.c",
            "src/platform/posix/posix_rand.c",
            "src/platform/posix/posix_resolv_gai.c",
            "src/platform/posix/posix_sockaddr.c",
            "src/platform/posix/posix_tcpconn.c",
            "src/platform/posix/posix_tcpdial.c",
            "src/platform/posix/posix_tcplisten.c",
            "src/platform/posix/posix_thread.c",
            "src/platform/posix/posix_udp.c",
            "src/platform/posix/posix_rand*.c",
            "src/protocol/**/*.c",
            "src/supplemental/base64/*.c",
            "src/supplemental/http/*.c",
            "src/supplemental/sha1/*.c",
            "src/supplemental/tcp/*.c",
            "src/supplemental/util/*.c",
            "src/supplemental/tls/*.c",
            "src/supplemental/tls/none/*.c",  # specifically "none"
            "src/supplemental/websocket/websocket.c",
            "src/transport/inproc/*.c",
            "src/transport/ipc/*.c",
            "src/transport/tcp/*.c",
            "src/transport/tls/*.c",
            "src/transport/ws/*.c",
        ],
        exclude = ["src/**/*_test.c"],
    ) + select({
        "@bazel_tools//src/conditions:darwin": ["src/platform/posix/posix_pollq_kqueue.c"],
        "//conditions:default": ["src/platform/posix/posix_pollq_epoll.c"],
    }),
    hdrs = glob(
        [
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
            "src/supplemental/sha1/sha1.c",
            "tests/*.h",
        ],
        exclude = ["include/nng/transport/zerotier/*.h"],
    ),
    defines = [
        "NNG_ENABLE_STATS",
        "NNG_HAVE_ALLOCA=1",
        "NNG_HAVE_BACKTRACE=1",
        "NNG_HAVE_BUS0",
        "NNG_HAVE_FLOCK=1",
        "NNG_HAVE_MSG_CONTROL=1",
        "NNG_HAVE_PAIR0",
        "NNG_HAVE_PAIR1",
        "NNG_HAVE_PUB0",
        "NNG_HAVE_PULL0",
        "NNG_HAVE_PUSH0",
        "NNG_HAVE_REP0",
        "NNG_HAVE_REQ0",
        "NNG_HAVE_RESPONDENT0",
        "NNG_HAVE_SEMAPHORE_PTHREAD=1",
        "NNG_HAVE_STDATOMIC=1",
        "NNG_HAVE_STRCASECMP=1",
        "NNG_HAVE_STRNCASECMP=1",
        "NNG_HAVE_STRNLEN=1",
        "NNG_HAVE_SUB0",
        "NNG_HAVE_SURVEYOR0",
        "NNG_HAVE_UNIX_SOCKETS=1",
        "NNG_HIDDEN_VISIBILITY",
        "NNG_LITTLE_ENDIAN",
        "NNG_PLATFORM_POSIX",
        "NNG_PRIVATE",
        "NNG_STATIC_LIB",
        "NNG_SUPP_HTTP",
        "NNG_TRANSPORT_INPROC",
        "NNG_TRANSPORT_IPC",
        "NNG_TRANSPORT_TCP",
        "_GNU_SOURCE",
        "_POSIX_PTHREAD_SEMANTICS",
        "_REENTRANT",
        "_THREAD_SAFE",
    ] + select({
        "@bazel_tools//src/conditions:darwin": [
            "NNG_HAVE_GETPEEREID=1",  # MacOS specific
            "NNG_HAVE_KQUEUE=1",  # MacOS specific
            "NNG_HAVE_LOCALPEERCRED=1",  # MacOS specific
            "NNG_HAVE_LOCKF=1",  # MacOS specific
            "NNG_HAVE_STRLCAT=1",  # MacOS specific
            "NNG_HAVE_STRLCPY=1",  # MacOS specific
            "NNG_PLATFORM_DARWIN",  # MacOS specific
            "NNG_USE_ARC4_RANDOM",  # MacOS specific
            "NNG_USE_CLOCKID=CLOCK_REALTIME",  # MacOS specific
        ],
        "//conditions:default": [
            "NNG_HAVE_CLOCK_GETTIME=1",  # Linux specific
            "NNG_HAVE_EPOLL=1",  # Linux specific
            "NNG_HAVE_EPOLL_CREATE1=1",  # Linux specific
            "NNG_HAVE_EVENTFD=1",  # Linux specific
            "NNG_HAVE_LIBNSL=1",  # Linux specific
            "NNG_HAVE_LOCKF=1",  # Linux specific
            "NNG_HAVE_SOPEERCRED=1",  # Linux specific
            "NNG_PLATFORM_LINUX",  # Linux specific
            "NNG_USE_EVENTFD",  # Linux specific
        ],
    }),
    includes = [
        "include",
        "src",
        "tests",
    ],
    linkopts = ["-pthread"],
    visibility = ["//visibility:public"],
)
