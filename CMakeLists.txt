cmake_minimum_required(VERSION 3.5)


project(occt_segfault)

add_executable(main main.cpp)

target_compile_features(main PRIVATE cxx_std_17)

# find and link occt
find_package(OpenCASCADE REQUIRED)
message(STATUS "OpenCASCADE v${OpenCASCADE_VERSION} found")

target_include_directories(main
  PRIVATE
    ${OpenCASCADE_INCLUDE_DIR}
)

target_link_libraries(main
  "TKernel"
)
