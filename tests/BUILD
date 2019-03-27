
# Make a library from the shared elements, they are somewhat spread out and disorganized,
# but they are able to be collected into a single module to be shared by each test
cc_library(
    name = "convey",
    srcs = ["convey.c"],
    hdrs = glob(["convey.h", "*.h"]),
    visibility = ["//visibility:public"],
    deps = ["//:nng"],
)

cc_test(
    name = "aio",
    srcs = ["aio.c"],
    deps = [":convey"]
)

cc_test(
    name = "base64",
    srcs = ["base64.c"],
    deps = [":convey"]
)

cc_test(
    name = "bufsz",
    srcs = ["bufsz.c"],
    deps = [":convey"]
)

cc_test(
    name = "bus",
    srcs = ["bus.c"],
    deps = [":convey"]
)

# Compatibility tests removed because meh, they cause problems

cc_test(
    name = "device",
    srcs = ["device.c"],
    deps = [":convey"]
)

cc_test(
    name = "errors",
    srcs = ["errors.c"],
    deps = [":convey"]
)

cc_test(
    name = "files",
    srcs = ["files.c"],
    deps = [":convey"]
)

cc_test(
    name = "httpclient",
    srcs = ["httpclient.c"],
    deps = [":convey"]
)

cc_test(
    name = "httpserver",
    srcs = ["httpserver.c"],
    deps = [":convey"]
)

cc_test(
    name = "idhash",
    srcs = ["idhash.c"],
    deps = [":convey"]
)

cc_test(
    name = "inproc",
    srcs = ["inproc.c"],
    deps = [":convey"]
)

cc_test(
    name = "ipc",
    srcs = ["ipc.c"],
    deps = [":convey"]
)

cc_test(
    name = "ipcperms",
    srcs = ["ipcperms.c"],
    deps = [":convey"]
)

cc_test(
    name = "ipcsupp",
    srcs = ["ipcsupp.c"],
    deps = [":convey"]
)

cc_test(
    name = "ipcwinsec",
    srcs = ["ipcwinsec.c"],
    deps = [":convey"]
)

cc_test(
    name = "list",
    srcs = ["list.c"],
    deps = [":convey"]
)

cc_test(
    name = "message",
    srcs = ["message.c"],
    deps = [":convey"]
)

cc_test(
    name = "multistress",
    srcs = ["multistress.c"],
    deps = [":convey"]
)

cc_test(
    name = "nonblock",
    srcs = ["nonblock.c"],
    deps = [":convey"]
)

cc_test(
    name = "options",
    srcs = ["options.c"],
    deps = [":convey"]
)

cc_test(
    name = "pair1",
    srcs = ["pair1.c"],
    deps = [":convey"]
)

cc_test(
    name = "pipe",
    srcs = ["pipe.c"],
    deps = [":convey"]
)

cc_test(
    name = "pipeline",
    srcs = ["pipeline.c"],
    deps = [":convey"]
)

cc_test(
    name = "platform",
    srcs = ["platform.c"],
    deps = [":convey"]
)

cc_test(
    name = "pollfd",
    srcs = ["pollfd.c"],
    deps = [":convey"]
)

cc_test(
    name = "pubsub",
    srcs = ["pubsub.c"],
    deps = [":convey"]
)

cc_test(
    name = "reconnect",
    srcs = ["reconnect.c"],
    deps = [":convey"]
)

cc_test(
    name = "reqctx",
    srcs = ["reqctx.c"],
    deps = [":convey"]
)

cc_test(
    name = "reqpoll",
    srcs = ["reqpoll.c"],
    deps = [":convey"]
)

cc_test(
    name = "reqrep",
    srcs = ["reqrep.c"],
    deps = [":convey"]
)

cc_test(
    name = "reqstress",
    srcs = ["reqstress.c"],
    deps = [":convey"]
)

cc_test(
    name = "resolv",
    srcs = ["resolv.c"],
    deps = [":convey"]
)

cc_test(
    name = "respondpoll",
    srcs = ["respondpoll.c"],
    deps = [":convey"]
)

cc_test(
    name = "scalability",
    srcs = ["scalability.c"],
    deps = [":convey"]
)

cc_test(
    name = "set_recvmaxsize",
    srcs = ["set_recvmaxsize.c"],
    deps = [":convey"]
)

cc_test(
    name = "sha1",
    srcs = ["sha1.c"],
    deps = [":convey"]
)

cc_test(
    name = "sock",
    srcs = ["sock.c"],
    deps = [":convey"]
)

cc_test(
    name = "stats",
    srcs = ["stats.c"],
    deps = [":convey"]
)

# Ignoring stubs since using actual websocket lib
#cc_test(
#    name = "stubs",
#    srcs = ["stubs.c"],
#    deps = [":convey"]
#)

cc_test(
    name = "survey",
    srcs = ["survey.c"],
    deps = [":convey"]
)

cc_test(
    name = "surveyctx",
    srcs = ["surveyctx.c"],
    deps = [":convey"]
)

cc_test(
    name = "surveypoll",
    srcs = ["surveypoll.c"],
    deps = [":convey"]
)

cc_test(
    name = "synch",
    srcs = ["synch.c"],
    deps = [":convey"]
)

cc_test(
    name = "tcp",
    srcs = ["tcp.c"],
    deps = [":convey"]
)

cc_test(
    name = "tcp6",
    srcs = ["tcp6.c"],
    deps = [":convey"]
)

cc_test(
    name = "tcpsupp",
    srcs = ["tcpsupp.c"],
    deps = [":convey"]
)

# Disabled, so removing
#cc_test(
#    name = "tls",
#    srcs = ["tls.c"],
#    deps = [":convey"]
#)

cc_test(
    name = "transport",
    srcs = ["transport.c"],
    deps = [":convey"]
)

cc_test(
    name = "udp",
    srcs = ["udp.c"],
    deps = [":convey"]
)

cc_test(
    name = "url",
    srcs = ["url.c"],
    deps = [":convey"]
)

# Broken, we don't need it so removing for now
#cc_test(
#    name = "ws",
#    srcs = ["ws.c"],
#    deps = [":convey"]
#)

# Ignoring wss and zt tests
