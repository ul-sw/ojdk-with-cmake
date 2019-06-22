
include_directories(src/share/vm)

include_directories(src/share/vm/precompiled)

include_directories(src/os/linux/vm)

include_directories(src/cpu/x86/vm)

include_directories(src/os_cpu/linux_x86/vm)

aux_source_directory(src/cpu/x86 CPU_X86)

aux_source_directory(src/os/linux OS_LINUX)

aux_source_directory(src/os_cpu/linux_x86 OS_CPU_LINUX_X86)

add_subdirectory(src/share/vm)

