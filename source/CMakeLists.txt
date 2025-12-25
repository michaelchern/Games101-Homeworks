set(SOURCE_ROOT_DIR "${HOMEWORK_ROOT_DIR}/source")
set(THIRD_PARTY_DIR "${SOURCE_ROOT_DIR}/third_party")

if(CMAKE_CXX_COMPILER_ID STREQUAL "MSVC")
    add_compile_options("/MP")
    #set_property(DIRECTORY ${CMAKE_SOURCE_DIR} PROPERTY VS_STARTUP_PROJECT PiccoloEditor)
endif()

add_subdirectory(third_party)
add_subdirectory(assignment1)