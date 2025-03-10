cmake_minimum_required(VERSION 3.31.0)

project("learn compiler"
    VERSION 0.0.1
    LANGUAGES C CXX
)

#================================================================
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)

set(LIBRARY_OUTPUT_PATH ${CMAKE_LIBRARY_OUTPUT_DIRECTORY})
set(INCLUDE_OUTPUT_DIR ${CMAKE_BINARY_DIR}/include)

#================================================================
include(cmake/CPM.cmake)

# add cpm download directory
set(CPM_SOURCE_CACHE ${CMAKE_BINARY_DIR}/third-party)

# add gtest and gmock library
include(cmake/CPM.cmake)
cpmaddpackage(
    NAME googletest
    GITHUB_REPOSITORY google/googletest
    GIT_TAG v1.15.2
    VERSION 1.15.2
    OPTIONS
    "INSTALL_GTEST OFF"
    "gtest_force_shared_crt"
)

# add format library
cpmaddpackage(
    NAME fmt
    GITHUB_REPOSITORY fmtlib/fmt
    GIT_TAG 11.0.2
    VERSION 11.0.2
    OPTION
    "FMT_HEADER_ONLY=ON"
)

#================================================================
set(DEFAULT_LIBS
    fmt::fmt
)

#================================================================
add_subdirectory(MyFirstFrontend)
