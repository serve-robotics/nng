
# Make a library from the shared elements, they are somewhat spread out and disorganized,
# but they are able to be collected into a single module to be shared by each test
cc_library(
    name = "convey_tests",
    srcs = ["convey.c", "compat_testutil.c"],
    hdrs = glob(["convey.h", "*.h"]),
    visibility = ["//visibility:public"],
    deps = ["//:nng"],
)

cc_test(
    name = "aio",
    srcs = ["aio.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "base64",
    srcs = ["base64.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "bufsz",
    srcs = ["bufsz.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "bus",
    srcs = ["bus.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "compat_block",
    srcs = ["compat_block.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "compat_bug777",
    srcs = ["compat_bug777.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "compat_bus",
    srcs = ["compat_bus.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "compat_cmsg",
    srcs = ["compat_cmsg.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "compat_device",
    srcs = ["compat_device.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "compat_iovec",
    srcs = ["compat_iovec.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "compat_msg",
    srcs = ["compat_msg.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "compat_options",
    srcs = ["compat_options.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "compat_pair",
    srcs = ["compat_pair.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "compat_pipeline",
    srcs = ["compat_pipeline.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "compat_poll",
    srcs = ["compat_poll.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "compat_reqrep",
    srcs = ["compat_reqrep.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "compat_reqttl",
    srcs = ["compat_reqttl.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "compat_shutdown",
    srcs = ["compat_shutdown.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "compat_survey",
    srcs = ["compat_survey.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "compat_surveyttl",
    srcs = ["compat_surveyttl.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "compat_tcp",
    srcs = ["compat_tcp.c"],
    deps = [":convey_tests"]
)

# Disabled because we aren't building this right now
#cc_test(
#    name = "compat_ws",
#    srcs = ["compat_ws.c"],
#    deps = [":convey_tests"]
#)

cc_test(
    name = "cplusplus_pair",
    srcs = ["cplusplus_pair.cc"],
    deps = [":convey_tests"]
)

cc_test(
    name = "device",
    srcs = ["device.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "errors",
    srcs = ["errors.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "files",
    srcs = ["files.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "httpclient",
    srcs = ["httpclient.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "httpserver",
    srcs = ["httpserver.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "idhash",
    srcs = ["idhash.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "inproc",
    srcs = ["inproc.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "ipc",
    srcs = ["ipc.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "ipcperms",
    srcs = ["ipcperms.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "ipcsupp",
    srcs = ["ipcsupp.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "ipcwinsec",
    srcs = ["ipcwinsec.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "list",
    srcs = ["list.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "message",
    srcs = ["message.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "multistress",
    srcs = ["multistress.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "nonblock",
    srcs = ["nonblock.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "options",
    srcs = ["options.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "pair1",
    srcs = ["pair1.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "pipe",
    srcs = ["pipe.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "pipeline",
    srcs = ["pipeline.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "platform",
    srcs = ["platform.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "pollfd",
    srcs = ["pollfd.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "pubsub",
    srcs = ["pubsub.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "reconnect",
    srcs = ["reconnect.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "reqctx",
    srcs = ["reqctx.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "reqpoll",
    srcs = ["reqpoll.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "reqrep",
    srcs = ["reqrep.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "reqstress",
    srcs = ["reqstress.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "resolv",
    srcs = ["resolv.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "respondpoll",
    srcs = ["respondpoll.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "scalability",
    srcs = ["scalability.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "set_recvmaxsize",
    srcs = ["set_recvmaxsize.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "sha1",
    srcs = ["sha1.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "sock",
    srcs = ["sock.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "stats",
    srcs = ["stats.c"],
    deps = [":convey_tests"]
)

# Ignoring stubs since using actual websocket lib
#cc_test(
#    name = "stubs",
#    srcs = ["stubs.c"],
#    deps = [":convey_tests"]
#)

cc_test(
    name = "survey",
    srcs = ["survey.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "surveyctx",
    srcs = ["surveyctx.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "surveypoll",
    srcs = ["surveypoll.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "synch",
    srcs = ["synch.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "tcp",
    srcs = ["tcp.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "tcp6",
    srcs = ["tcp6.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "tcpsupp",
    srcs = ["tcpsupp.c"],
    deps = [":convey_tests"]
)

# Disabled, so removing
#cc_test(
#    name = "tls",
#    srcs = ["tls.c"],
#    deps = [":convey_tests"]
#)

cc_test(
    name = "transport",
    srcs = ["transport.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "udp",
    srcs = ["udp.c"],
    deps = [":convey_tests"]
)

cc_test(
    name = "url",
    srcs = ["url.c"],
    deps = [":convey_tests"]
)

# Broken, we don't need it so removing for now
#cc_test(
#    name = "ws",
#    srcs = ["ws.c"],
#    deps = [":convey_tests"]
#)

# Ignoring wss and zt tests
