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
        "include/compiler.h",
        "include/config.h",
        "include/dwarf.h",
        "include/libunwind-coredump.h",
        "include/libunwind_i.h",
        "include/libunwind-x86_64.h",
        "include/libunwind-common.h",
        "include/libunwind-dynamic.h",
        "include/libunwind.h",
        "include/mempool.h",
    ] + glob(
        [
            "include/tdep-x86_64/*.h",
            "include/tdep/*.h",
        ],
        exclude = [
        ],
    ),
    copts = [
        "-DHAVE_CONFIG_H",
        "-D_GNU_SOURCE",
        "-DNO_FRAME_POINTER",
        "-fno-common",
        "-Wno-cpp",
    ],
    includes = [
        "include",
        "include/tdep",
        "include/tdep-x86_64",
        "src",
    ],
    visibility = ["//visibility:public"],
    deps = [
        ":elf64",
    ],
)

cc_library(
    name = "unwind-ptrace",
    srcs = [
    ] + glob(
        [
            "src/ptrace/**/*.c",
            "src/ptrace/*.h",
        ],
        exclude = [
        ],
    ),
    hdrs = [
        "include/compiler.h",
        "include/config.h",
        "include/dwarf.h",
        "include/libunwind-ptrace.h",
        "include/libunwind.h",
        "include/libunwind-common.h",
        "include/libunwind-x86_64.h",
        "include/libunwind-dynamic.h",
        "include/libunwind_i.h",
        "include/mempool.h",
    ] + glob(
        [
            "include/tdep-x86_64/*.h",
            "include/tdep/*.h",
        ],
        exclude = [
        ],
    ),
    copts = [
        "-DHAVE_CONFIG_H",
        "-D_GNU_SOURCE",
        "-DNO_FRAME_POINTER",
        "-fno-common",
        "-Wno-cpp",
    ],
    includes = [
        "include",
        "include/tdep",
        "include/tdep-x86_64",
        "src",
    ],
    visibility = ["//visibility:public"],
    deps = [
        ":elf64",
    ],
)

cc_library(
    name = "unwind-setjmp",
    srcs = [
    ] + glob(
        [
            "src/setjmp/**/*.c",
            "src/setjmp/**/*.h",
        ],
        exclude = [
        ],
    ),
    hdrs = [
        "include/compiler.h",
        "include/config.h",
        "include/dwarf.h",
        "include/libunwind.h",
        "include/libunwind-common.h",
        "include/libunwind_i.h",
        "include/libunwind-x86_64.h",
        "include/libunwind-dynamic.h",
        "include/mempool.h",
    ] + glob(
        [
            "include/tdep-x86_64/*.h",
            "include/tdep/*.h",
        ],
        exclude = [
        ],
    ),
    copts = [
        "-DHAVE_CONFIG_H",
        "-D_GNU_SOURCE",
        "-DNO_FRAME_POINTER",
        "-fno-common",
        "-Wno-cpp",
    ],
    includes = [
        "include",
        "include/tdep",
        "include/tdep-x86_64",
        "src",
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
        "src/x86_64/setcontext.S",
        "src/x86_64/longjmp.S",
        "src/x86_64/getcontext.S",
    ] + glob(
        [
            "src/unwind/**/*.c",
            "src/unwind/**/*.h",
            "src/ptrace/**/*.c",
            "src/ptrace/*.h",
            "src/mi/**/*.c",
            "src/dwarf/**/*.c",
            "src/x86_64/**/*.c",
            "src/x86_64/**/*.h",
        ],
        exclude = [
            "src/dwarf/**/G*.c",
            "src/mi/**/G*.c",
            "src/x86_64/**/G*.c",
            "src/x86_64/Los-solaris.c",
            "src/x86_64/Los-freebsd.c",
        ],
    ),
    hdrs = [
        "include/compiler.h",
        "include/config.h",
        "include/dwarf-eh.h",
        "include/dwarf.h",
        "include/dwarf_i.h",
        "include/libunwind_i.h",
        "include/libunwind.h",
        "include/libunwind-x86_64.h",
        "include/libunwind-common.h",
        "include/libunwind-dynamic.h",
        "include/mempool.h",
        "include/remote.h",
        "include/unwind.h",
    ] + glob(
        [
            "include/tdep-x86_64/*.h",
            "include/tdep/*.h",
            "src/mi/**/G*.c",
            "src/dwarf/**/G*.c",
            "src/x86_64/**/G*.c",
            "src/x86_64/Los-solaris.c",
            "src/x86_64/Los-freebsd.c",
        ],
        exclude = [
        ],
    ),
    copts = [
        "-DHAVE_CONFIG_H",
        "-D_GNU_SOURCE",
        "-DNO_FRAME_POINTER",
        "-fno-common",
        "-Iexternal/zlib",
        "-Wno-cpp",
    ],
    includes = [
        "include",
        "include/tdep",
        "include/tdep-x86_64",
        "src",
    ],
    visibility = ["//visibility:public"],
    deps = [
        ":elf64",
        ":unwind-coredump",
        ":unwind-ptrace",
        ":unwind-setjmp",
        "@zlib",
    ],
    alwayslink = True,
)
