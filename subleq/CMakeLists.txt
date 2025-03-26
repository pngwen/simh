## subleq simulator
##
## This is an automagically generated file. Do NOT EDIT.
## Any changes you make will be overwritten!!
##
## Make changes to the SIMH top-level makefile and then run the
## "cmake/generate.py" script to regenerate these files.
##
##     cd cmake; python -m generate --help
##
## ------------------------------------------------------------

if (HAVE_UNITY_FRAMEWORK AND EXISTS "${CMAKE_CURRENT_SOURCE_DIR}/unit-tests/CMakeLists.txt")
  add_subdirectory(unit-tests)
endif ()

add_simulator(subleq
    SOURCES
        subleq_sys.c
        subleq_cpu.c
    INCLUDES
        ${CMAKE_CURRENT_SOURCE_DIR}
    LABEL subleq
    PKG_FAMILY default_family
    TEST subleq)
