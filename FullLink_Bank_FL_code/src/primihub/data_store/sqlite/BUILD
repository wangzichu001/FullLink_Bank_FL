package(default_visibility = ["//visibility:public",],)
cc_library(
    name = "sqlite_driver",
    hdrs = ["sqlite_driver.h"],
    srcs = ["sqlite_driver.cc"],
    deps = [
        "//src/primihub/data_store:base_driver",
        "//src/primihub/util:util_lib",
        "@arrow",
        "@com_github_sqlite_wrapper//:sqlite_wrapper",
        "@nlohmann_json",
    ],
)