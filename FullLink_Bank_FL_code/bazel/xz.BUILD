package(default_visibility = ["//visibility:public"])

licenses(["notice"])  # public domain

config_setting(
  name = "darwin_arm64",
  values = {
    "cpu": "darwin_arm64"
  }
)


config_setting(
  name = "darwin_x86_64",
  values = {
    "cpu": "darwin_x86_64"
  }
)

cc_library(
    name = "lzma",
    srcs = select ({
        "darwin_arm64": [
            "src/common/tuklib_cpucores.c",
            "src/common/tuklib_physmem.c",
            "src/liblzma/check/check.c",
            "src/liblzma/check/crc32_fast.c",
            "src/liblzma/check/crc32_table.c",
            "src/liblzma/check/crc64_fast.c",
            "src/liblzma/check/crc64_table.c",
            "src/liblzma/check/sha256.c",
            "src/liblzma/common/alone_decoder.c",
            "src/liblzma/common/alone_encoder.c",
            "src/liblzma/common/auto_decoder.c",
            "src/liblzma/common/block_buffer_decoder.c",
            "src/liblzma/common/block_buffer_encoder.c",
            "src/liblzma/common/block_decoder.c",
            "src/liblzma/common/block_encoder.c",
            "src/liblzma/common/block_header_decoder.c",
            "src/liblzma/common/block_header_encoder.c",
            "src/liblzma/common/block_util.c",
            "src/liblzma/common/common.c",
            "src/liblzma/common/easy_buffer_encoder.c",
            "src/liblzma/common/easy_decoder_memusage.c",
            "src/liblzma/common/easy_encoder.c",
            "src/liblzma/common/easy_encoder_memusage.c",
            "src/liblzma/common/easy_preset.c",
            "src/liblzma/common/filter_buffer_decoder.c",
            "src/liblzma/common/filter_buffer_encoder.c",
            "src/liblzma/common/filter_common.c",
            "src/liblzma/common/filter_decoder.c",
            "src/liblzma/common/filter_encoder.c",
            "src/liblzma/common/filter_flags_decoder.c",
            "src/liblzma/common/filter_flags_encoder.c",
            "src/liblzma/common/hardware_cputhreads.c",
            "src/liblzma/common/hardware_physmem.c",
            "src/liblzma/common/index.c",
            "src/liblzma/common/index_decoder.c",
            "src/liblzma/common/index_encoder.c",
            "src/liblzma/common/index_hash.c",
            "src/liblzma/common/outqueue.c",
            "src/liblzma/common/stream_buffer_decoder.c",
            "src/liblzma/common/stream_buffer_encoder.c",
            "src/liblzma/common/stream_decoder.c",
            "src/liblzma/common/stream_encoder.c",
            "src/liblzma/common/stream_encoder_mt.c",
            "src/liblzma/common/stream_flags_common.c",
            "src/liblzma/common/stream_flags_decoder.c",
            "src/liblzma/common/stream_flags_encoder.c",
            "src/liblzma/common/vli_decoder.c",
            "src/liblzma/common/vli_encoder.c",
            "src/liblzma/common/vli_size.c",
            "src/liblzma/delta/delta_common.c",
            "src/liblzma/delta/delta_decoder.c",
            "src/liblzma/delta/delta_encoder.c",
            "src/liblzma/lz/lz_decoder.c",
            # "src/liblzma/lz/lz_encoder.c",      # TODO only for x86 
            # "src/liblzma/lz/lz_encoder_mf.c", // TODO only for x86
            "src/liblzma/lzma/fastpos_table.c",
            "src/liblzma/lzma/lzma2_decoder.c",
            "src/liblzma/lzma/lzma2_encoder.c",
            "src/liblzma/lzma/lzma_decoder.c",
            "src/liblzma/lzma/lzma_encoder.c",
            # "src/liblzma/lzma/lzma_encoder_optimum_fast.c",  // TODO only for x86
            # "src/liblzma/lzma/lzma_encoder_optimum_normal.c",// TODO only for x86 
            "src/liblzma/lzma/lzma_encoder_presets.c",
            "src/liblzma/rangecoder/price_table.c",
            "src/liblzma/simple/arm.c",
            "src/liblzma/simple/armthumb.c",
            "src/liblzma/simple/ia64.c",
            "src/liblzma/simple/powerpc.c",
            "src/liblzma/simple/simple_coder.c",
            "src/liblzma/simple/simple_decoder.c",
            "src/liblzma/simple/simple_encoder.c",
            "src/liblzma/simple/sparc.c",
            "src/liblzma/simple/x86.c",
        ],
        "//conditions:default": [
            "src/common/tuklib_cpucores.c",
            "src/common/tuklib_physmem.c",
            "src/liblzma/check/check.c",
            "src/liblzma/check/crc32_fast.c",
            "src/liblzma/check/crc32_table.c",
            "src/liblzma/check/crc64_fast.c",
            "src/liblzma/check/crc64_table.c",
            "src/liblzma/check/sha256.c",
            "src/liblzma/common/alone_decoder.c",
            "src/liblzma/common/alone_encoder.c",
            "src/liblzma/common/auto_decoder.c",
            "src/liblzma/common/block_buffer_decoder.c",
            "src/liblzma/common/block_buffer_encoder.c",
            "src/liblzma/common/block_decoder.c",
            "src/liblzma/common/block_encoder.c",
            "src/liblzma/common/block_header_decoder.c",
            "src/liblzma/common/block_header_encoder.c",
            "src/liblzma/common/block_util.c",
            "src/liblzma/common/common.c",
            "src/liblzma/common/easy_buffer_encoder.c",
            "src/liblzma/common/easy_decoder_memusage.c",
            "src/liblzma/common/easy_encoder.c",
            "src/liblzma/common/easy_encoder_memusage.c",
            "src/liblzma/common/easy_preset.c",
            "src/liblzma/common/filter_buffer_decoder.c",
            "src/liblzma/common/filter_buffer_encoder.c",
            "src/liblzma/common/filter_common.c",
            "src/liblzma/common/filter_decoder.c",
            "src/liblzma/common/filter_encoder.c",
            "src/liblzma/common/filter_flags_decoder.c",
            "src/liblzma/common/filter_flags_encoder.c",
            "src/liblzma/common/hardware_cputhreads.c",
            "src/liblzma/common/hardware_physmem.c",
            "src/liblzma/common/index.c",
            "src/liblzma/common/index_decoder.c",
            "src/liblzma/common/index_encoder.c",
            "src/liblzma/common/index_hash.c",
            "src/liblzma/common/outqueue.c",
            "src/liblzma/common/stream_buffer_decoder.c",
            "src/liblzma/common/stream_buffer_encoder.c",
            "src/liblzma/common/stream_decoder.c",
            "src/liblzma/common/stream_encoder.c",
            "src/liblzma/common/stream_encoder_mt.c",
            "src/liblzma/common/stream_flags_common.c",
            "src/liblzma/common/stream_flags_decoder.c",
            "src/liblzma/common/stream_flags_encoder.c",
            "src/liblzma/common/vli_decoder.c",
            "src/liblzma/common/vli_encoder.c",
            "src/liblzma/common/vli_size.c",
            "src/liblzma/delta/delta_common.c",
            "src/liblzma/delta/delta_decoder.c",
            "src/liblzma/delta/delta_encoder.c",
            "src/liblzma/lz/lz_decoder.c",
            "src/liblzma/lz/lz_encoder.c",      # TODO only for x86 
            "src/liblzma/lz/lz_encoder_mf.c",  # TODO only for x86
            "src/liblzma/lzma/fastpos_table.c",
            "src/liblzma/lzma/lzma2_decoder.c",
            "src/liblzma/lzma/lzma2_encoder.c",
            "src/liblzma/lzma/lzma_decoder.c",
            "src/liblzma/lzma/lzma_encoder.c",
            "src/liblzma/lzma/lzma_encoder_optimum_fast.c",  # TODO only for x86
            "src/liblzma/lzma/lzma_encoder_optimum_normal.c",# TODO only for x86 
            "src/liblzma/lzma/lzma_encoder_presets.c",
            "src/liblzma/rangecoder/price_table.c",
            "src/liblzma/simple/arm.c",
            "src/liblzma/simple/armthumb.c",
            "src/liblzma/simple/ia64.c",
            "src/liblzma/simple/powerpc.c",
            "src/liblzma/simple/simple_coder.c",
            "src/liblzma/simple/simple_decoder.c",
            "src/liblzma/simple/simple_encoder.c",
            "src/liblzma/simple/sparc.c",
            "src/liblzma/simple/x86.c",
        ]

    }),
    hdrs = glob(["src/**/*.h"]) + ["config.h"],
    copts = select({
        "@bazel_tools//src/conditions:windows": [],
        "//conditions:default": [
            "-std=c99",
        ],
    }),
    defines = [
        "HAVE_CONFIG_H",
        "LZMA_API_STATIC",
    ],
    includes = [
        ".",
        "src",
        "src/common",
        "src/liblzma",
        "src/liblzma/api",
        "src/liblzma/check",
        "src/liblzma/common",
        "src/liblzma/delta",
        "src/liblzma/lz",
        "src/liblzma/lzma",
        "src/liblzma/rangecoder",
        "src/liblzma/simple",
    ],
    linkopts = ["-lpthread"],
    visibility = ["//visibility:public"],
)

genrule(
    name = "configure",
    outs = ["config.h"],
    cmd = "\n".join([
        "cat <<'EOF' >$@",
        "",
        "#if defined(_MSC_VER)",
        "",
        "#define HAVE_VISIBILITY 0",
        "#define MYTHREAD_VISTA 1",
        "",
        "#elif defined(__APPLE__)",
        "",
        "#define TUKLIB_CPUCORES_SYSCTL 1",
        "#define ENABLE_NLS 1",
        "#define HAVE_CLOCK_GETTIME 1",
        "#define HAVE_DCGETTEXT 1",
        "#define HAVE_DECL_CLOCK_MONOTONIC 1",
        "#define HAVE_DECL_PROGRAM_INVOCATION_NAME 1",
        "#define HAVE_DLFCN_H 1",
        "#define HAVE_FCNTL_H 1",
        "#define HAVE_FUTIMENS 1",
        "#define HAVE_GETOPT_H 1",
        "#define HAVE_GETOPT_LONG 1",
        "#define HAVE_GETTEXT 1",
        "#define HAVE_IMMINTRIN_H 1",
        "#define HAVE_MBRTOWC 1",
        "#define HAVE_MEMORY_H 1",
        "#define HAVE_POSIX_FADVISE 1",
        "#define HAVE_PTHREAD_PRIO_INHERIT 1",
        "#define HAVE_STRINGS_H 1",
        "#define HAVE_SYS_TIME_H 1",
        "#define HAVE_STRUCT_STAT_ST_ATIM_TV_NSEC 1",
        "#define HAVE_SYS_PARAM_H 1",
        "#define HAVE_SYS_STAT_H 1",
        "#define HAVE_SYS_TYPES_H 1",
        "#define HAVE_UINTPTR_T 1",
        "#define HAVE_UNISTD_H 1",
        "#define HAVE_WCWIDTH 1",
        "#define HAVE__MM_MOVEMASK_EPI8 1",
        "#define HAVE_VISIBILITY 0",
        "#define MYTHREAD_POSIX 1",
        "",
        "#define _ALL_SOURCE 1",
        "#define _GNU_SOURCE 1",
        "#define _POSIX_PTHREAD_SEMANTICS 1",
        "#define _TANDEM_SOURCE 1",
        "#define __EXTENSIONS__ 1",
        "",
        "#define _DARWIN_USE_64_BIT_INODE 1",
        "",
        "#else",
        "",
        "#define TUKLIB_CPUCORES_SCHED_GETAFFINITY 1",
        "#define ENABLE_NLS 1",
        "#define HAVE_BSWAP_16 1",
        "#define HAVE_BSWAP_32 1",
        "#define HAVE_BSWAP_64 1",
        "#define HAVE_BYTESWAP_H 1",
        "#define HAVE_CLOCK_GETTIME 1",
        "#define HAVE_DCGETTEXT 1",
        "#define HAVE_DECL_CLOCK_MONOTONIC 1",
        "#define HAVE_DECL_PROGRAM_INVOCATION_NAME 1",
        "#define HAVE_DLFCN_H 1",
        "#define HAVE_FCNTL_H 1",
        "#define HAVE_FUTIMENS 1",
        "#define HAVE_GETOPT_H 1",
        "#define HAVE_GETOPT_LONG 1",
        "#define HAVE_GETTEXT 1",
        "#if defined __x86_64__",
        "#define HAVE_IMMINTRIN_H 1",
        "#endif",
        "#define HAVE_MBRTOWC 1",
        "#define HAVE_MEMORY_H 1",
        "#define HAVE_POSIX_FADVISE 1",
        "#define HAVE_PTHREAD_PRIO_INHERIT 1",
        "#define HAVE_PTHREAD_CONDATTR_SETCLOCK 1",
        "#define HAVE_STRINGS_H 1",
        "#define HAVE_SYS_TIME_H 1",
        "#define HAVE_STRUCT_STAT_ST_ATIM_TV_NSEC 1",
        "#define HAVE_SYS_PARAM_H 1",
        "#define HAVE_SYS_STAT_H 1",
        "#define HAVE_SYS_TYPES_H 1",
        "#define HAVE_UINTPTR_T 1",
        "#define HAVE_UNISTD_H 1",
        "#define HAVE_WCWIDTH 1",
        "#define HAVE__MM_MOVEMASK_EPI8 1",
        "#define HAVE_VISIBILITY 0",
        "#define MYTHREAD_POSIX 1",
        "",
        "#define _ALL_SOURCE 1",
        "#define _GNU_SOURCE 1",
        "#define _POSIX_PTHREAD_SEMANTICS 1",
        "#define _TANDEM_SOURCE 1",
        "#define __EXTENSIONS__ 1",
        "",
        "#endif",
        "",
        "#define ASSUME_RAM 128",
        "#define HAVE_CHECK_CRC32 1",
        "#define HAVE_CHECK_CRC64 1",
        "#define HAVE_CHECK_SHA256 1",
        "#define HAVE_DECODERS 1",
        "#define HAVE_DECODER_ARM 1",
        "#define HAVE_DECODER_ARMTHUMB 1",
        "#define HAVE_DECODER_DELTA 1",
        "#define HAVE_DECODER_IA64 1",
        "#define HAVE_DECODER_LZMA1 1",
        "#define HAVE_DECODER_LZMA2 1",
        "#define HAVE_DECODER_POWERPC 1",
        "#define HAVE_DECODER_SPARC 1",
        "#define HAVE_DECODER_X86 1",
        "#define HAVE_ENCODERS 1",
        "#define HAVE_ENCODER_ARM 1",
        "#define HAVE_ENCODER_ARMTHUMB 1",
        "#define HAVE_ENCODER_DELTA 1",
        "#define HAVE_ENCODER_IA64 1",
        "#define HAVE_ENCODER_LZMA1 1",
        "#define HAVE_ENCODER_LZMA2 1",
        "#define HAVE_ENCODER_POWERPC 1",
        "#define HAVE_ENCODER_SPARC 1",
        "#define HAVE_ENCODER_X86 1",
        "#define HAVE_INTTYPES_H 1",
        "#define HAVE_LIMITS_H 1",
        "#define HAVE_MF_BT2 1",
        "#define HAVE_MF_BT3 1",
        "#define HAVE_MF_BT4 1",
        "#define HAVE_MF_HC3 1",
        "#define HAVE_MF_HC4 1",
        "#define HAVE_STDBOOL_H 1",
        "#define HAVE_STDINT_H 1",
        "#define HAVE_STDLIB_H 1",
        "#define HAVE_STRING_H 1",
        "#define HAVE__BOOL 1",
        "#define LT_OBJDIR \".libs/\"",
        "#define NDEBUG 1",
        "#define PACKAGE \"xz\"",
        "#define PACKAGE_BUGREPORT \"lasse.collin@tukaani.org\"",
        "#define PACKAGE_NAME \"XZ Utils\"",
        "#define PACKAGE_STRING \"XZ Utils 5.2.4\"",
        "#define PACKAGE_TARNAME \"xz\"",
        "#define PACKAGE_URL \"https://tukaani.org/xz/\"",
        "#define PACKAGE_VERSION \"5.2.4\"",
        "#define SIZEOF_SIZE_T 8",
        "#define STDC_HEADERS 1",
        "#define TUKLIB_FAST_UNALIGNED_ACCESS 1",
        "#define TUKLIB_PHYSMEM_SYSCONF 1",
        "#define VERSION \"5.2.4\"",
        "",
        "EOF",
    ]),
)