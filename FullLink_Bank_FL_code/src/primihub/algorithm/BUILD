package(default_visibility = ["//visibility:public"])

config_setting(
    name = "aarch64",
    values = {"define": "cpu_arch=aarch64"},
)

config_setting(
    name = "x86_64",
    values = {"define": "cpu_arch=x86_64"},
)
config_setting(
    name = "darwin_x86_64",
    values = {"define": "cpu_arch=darwin_x86_64"},
)

cc_library(
    name = "algorithm_lib",
    srcs = glob([
        "aby3ML.cc",
        "linear_model_gen.cc",
        "logistic.cc",
        "logistic_plain.cc",
        "plainML.cc",
        "falcon_lenet.cc",
        "arithmetic.cc",
        # "src/primihub/executor/express.cc",
        # "src/primihub/operator/aby3_operator.cc",
        "missing_val_processing.cc",
    ]),
    hdrs = glob([
        "base.h",
        "aby3ML.h",
        "linear_model_gen.h",
        "logistic.h",
        "logistic_plain.h",
        "plainML.h",
        "regression.h",
        "falcon_lenet.h",
        "arithmetic.h",
        "missing_val_processing.h",
    ]),
    linkstatic = False,
    deps = [
        # ":eigen",
        "//src/primihub/common:common_lib",
        "//src/primihub/protocol:protocol_aby3_lib",
         "//src/primihub/protocol:protocol_falcon_lib",
        "//src/primihub/data_store:data_store_lib",
        "//src/primihub/util:model_util_lib",
        "//src/primihub/util:util_lib",
        "//src/primihub/service:dataset_service",
        "//src/primihub/executor:mpc_express_executor",
        "//src/primihub/data_store:data_store_util",
        "//src/primihub/util/crypto:crypto_lib",
    ],
)

cc_library(
    name = "cryptflow2_algorithm_lib",
    srcs = glob([
        "cryptflow2_maxpool.cc",
    ]),
    hdrs = glob([
        "base.h",
        "cryptflow2_maxpool.h",
    ]),
    copts = select({
        ":x86_64": ["-maes", "-mrdseed", "-mavx2"],
        ":aarch64": [],
        "//conditions:default": [],
    }),
    deps = [
        "//src/primihub/common:common_lib",
        "//src/primihub/data_store:data_store_lib",
        "//src/primihub/service:dataset_service",
        "//src/primihub/protocol:protocol_cryptflow2_ot_lib",
        "//src/primihub/util/network:network_lib",
        "//src/primihub/util:instruction_check_util",
    ],
)