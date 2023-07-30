cc_library(
    name = "elf64",
    srcs = [
        "src/elf64.h",
        "src/elfxx.h",
    ],
    hdrs = [
        "src/elfxx.c",
    ],
    deps = [
        "@lzma",
    ],
)

cc_library(
    name = "unwind-coredump",
    srcs = [
        "include/compiler.h",
        "include/config.h",
        "include/mempool.h",
        "include/libunwind_i.h",
        "include/dwarf.h",
    ] + glob(
        [
            "src/coredump/**/*.c",
            "src/coredump/**/*.h",
        ],
        exclude = [
            "src/coredump/_UCD_access_reg_freebsd.c",
            "src/coredump/_UCD_get_mapinfo_generic.c",
        ],
    ),
    hdrs = [
        "include/libunwind-x86_64.h",
        "include/libunwind-coredump.h",
        "include/libunwind-common.h",
        "include/libunwind-dynamic.h",
        "include/libunwind.h",
    ] + glob(
        [
            "include/tdep-x86_64/*.h",
            "include/tdep/*.h",
        ],
        exclude = [
        ],
    ),
    copts = [
        "-fno-common",
        "-Wno-cpp",
    ],
    includes = [
        "include",
        "include/tdep",
        "include/tdep-x86_64",
        "src",
    ],
    local_defines = [
        "HAVE_CONFIG_H",
        "_GNU_SOURCE",
        "NO_FRAME_POINTER",
    ],
    visibility = ["//visibility:public"],
    deps = [
        ":elf64",
    ],
)

cc_library(
    name = "unwind-ptrace",
    srcs = [
        "include/compiler.h",
        "include/libunwind_i.h",
        "include/mempool.h",
        "include/config.h",
        "include/dwarf.h",
    ] + glob(
        [
            "src/ptrace/**/*.c",
            "src/ptrace/*.h",
        ],
        exclude = [
        ],
    ),
    hdrs = [
        "include/libunwind-ptrace.h",
        "include/libunwind.h",
        "include/libunwind-common.h",
        "include/libunwind-x86_64.h",
        "include/libunwind-dynamic.h",
    ] + glob(
        [
            "include/tdep-x86_64/*.h",
            "include/tdep/*.h",
        ],
        exclude = [
        ],
    ),
    copts = [
        "-fno-common",
        "-Wno-cpp",
    ],
    includes = [
        "include",
        "include/tdep",
        "include/tdep-x86_64",
        "src",
    ],
    local_defines = [
        "HAVE_CONFIG_H",
        "_GNU_SOURCE",
        "NO_FRAME_POINTER",
    ],
    visibility = ["//visibility:public"],
    deps = [
        ":elf64",
    ],
)

cc_library(
    name = "unwind-setjmp",
    srcs = [
        "include/compiler.h",
        "include/config.h",
        "include/dwarf.h",
        "include/mempool.h",
        "include/libunwind_i.h",
    ] + glob(
        [
            "src/setjmp/**/*.c",
            "src/setjmp/**/*.h",
        ],
        exclude = [
        ],
    ),
    hdrs = [
        "include/libunwind.h",
        "include/libunwind-common.h",
        "include/libunwind-x86_64.h",
        "include/libunwind-dynamic.h",
    ] + glob(
        [
            "include/tdep-x86_64/*.h",
            "include/tdep/*.h",
        ],
        exclude = [
        ],
    ),
    copts = [
        "-fno-common",
        "-Wno-cpp",
    ],
    includes = [
        "include",
        "include/tdep",
        "include/tdep-x86_64",
        "src",
    ],
    local_defines = [
        "HAVE_CONFIG_H",
        "_GNU_SOURCE",
        "NO_FRAME_POINTER",
    ],
    visibility = ["//visibility:public"],
    deps = [
        ":elf64",
    ],
)

cc_library(
    name = "unwind",
    srcs = [
        "src/dl-iterate-phdr.c",
        "src/os-linux.h",
        "src/os-linux.c",
        "src/x86_64/siglongjmp.S",
        "src/elf64.h",
        "src/elfxx.c",
        "src/elfxx.h",
        "src/x86_64/setcontext.S",
        "include/compiler.h",
        "include/config.h",
        "include/dwarf-eh.h",
        "include/mempool.h",
        "include/remote.h",
        "include/dwarf.h",
        "include/dwarf_i.h",
        "include/libunwind_i.h",
        "src/x86_64/longjmp.S",
        "src/x86_64/getcontext.S",
    ] + glob(
        [
            "src/unwind/**/*.c",
            "src/unwind/**/*.h",
            "src/mi/**/*.c",
            "src/dwarf/**/*.c",
            "src/x86_64/**/*.c",
            "src/x86_64/**/*.h",
        ],
        exclude = [
            "src/x86_64/Los-solaris.c",
            "src/x86_64/Los-freebsd.c",
            "src/x86_64/G*.c",
            "src/dwarf/G*.c",
            "src/mi/G*.c",
        ],
    ),
    hdrs = [
        "include/libunwind.h",
        "include/libunwind-x86_64.h",
        "include/libunwind-common.h",
        "include/libunwind-dynamic.h",
        "include/unwind.h",
    ] + glob(
        [
            "include/tdep-x86_64/*.h",
            "include/tdep/*.h",
            "src/x86_64/G*.c",
            "src/mi/G*.c",
            "src/dwarf/G*.c",
        ],
        exclude = [
            "src/x86_64/Gos-freebsd.c",
        ],
    ),
    copts = [
        "-fno-common",
        "-Iexternal/zlib",
        "-Wno-cpp",
    ],
    includes = [
        "include",
        "include/tdep",
        "include/tdep-x86_64",
        "src",
        "src/dwarf",
        "src/mi",
    ],
    local_defines = [
        "HAVE_CONFIG_H",
        "_GNU_SOURCE",
        "NO_FRAME_POINTER",
    ],
    visibility = ["//visibility:public"],
    deps = [
        ":unwind-coredump",
        ":unwind-ptrace",
        ":unwind-setjmp",
        "@lzma",
        "@zlib",
    ],
    alwayslink = True,
)
