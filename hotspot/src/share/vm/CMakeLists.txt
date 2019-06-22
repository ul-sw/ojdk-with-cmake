set(CMAKE_INCLUDE_CURRENT_DIR ON)

include_directories(".")

add_definitions(-DTARGET_COMPILER_gcc)
add_definitions(-DTARGET_ARCH_x86)
add_definitions(-DTARGET_OS_ARCH_linux_x86)
add_definitions(-DCC_INTERP)
add_definitions(-DUSELABELS)

aux_source_directory(../../cpu/x86/vm cpu_x86_vm)
aux_source_directory(../../os/linux/vm os_linux_vm)
aux_source_directory(../../os_cpu/linux_x86/vm os_cpu_linux_x86_vm)

aux_source_directory(adlc SHARE_VM_ADLC)
aux_source_directory(asm SHARE_VM_ASM)
aux_source_directory(c1 SHARE_VM_C1)
aux_source_directory(ci SHARE_VM_CI)
aux_source_directory(classfile SHARE_VM_CLASSFILE)
aux_source_directory(code SHARE_VM_CODE)
aux_source_directory(compiler SHARE_VM_COMPILER)
aux_source_directory(gc_implementation SHARE_VM_GC_IMPLEMENTATION)
aux_source_directory(gc_interface SHARE_VM_GC_INTERFACE)
aux_source_directory(interpreter SHARE_VM_INTERPETER)
aux_source_directory(libadt SHARE_VM_LIBADT)
aux_source_directory(memory SHARE_VM_MEMORY)
aux_source_directory(oops SHARE_VM_OOPS)
aux_source_directory(opto SHARE_VM_OPTO)
aux_source_directory(precompiled SHARE_VM_PRECOMPILED)
aux_source_directory(prims SHARE_VM_PRIMS)
aux_source_directory(runtime SHARE_VM_RUNTIME)
aux_source_directory(services SHARE_VM_SERVICES)
aux_source_directory(shark SHARE_VM_SHARK)
aux_source_directory(trace SHARE_VM_TRACE)
aux_source_directory(utilities SHARE_VM_UTILITIES)


add_library(VM
        ${cpu_x86_vm}
        ${os_linux_vm}
        ${os_cpu_linux_x86_vm}
        ${SHARE_VM_ADLC}
        ${SHARE_VM_ASM}
        ${SHARE_VM_C1}
        ${SHARE_VM_CI}
        ${SHARE_VM_CLASSFILE}
        ${SHARE_VM_CODE}
        ${SHARE_VM_COMPILER}
        ${SHARE_VM_GC_IMPLEMENTATION}
        ${SHARE_VM_GC_INTERFACE}
        ${SHARE_VM_INTERPETER}
        ${SHARE_VM_LIBADT}
        ${SHARE_VM_MEMORY}
        ${SHARE_VM_OOPS}
        ${SHARE_VM_OPTO}
        ${SHARE_VM_PRECOMPILED}
        ${SHARE_VM_PRIMS}
        ${SHARE_VM_RUNTIME}
        ${SHARE_VM_SERVICES}
        ${SHARE_VM_SHARK}
        ${SHARE_VM_TRACE}
        ${SHARE_VM_UTILITIES}
        ../../../../main.cpp)

