project(1 CXX)

set(1_PUBLIC_INCLUDE_DIRS
  ${CMAKE_SOURCE_DIR}/include
  CACHE INTERNAL "1 public include directories"
)

set(main_SRCS
  main.cpp
)

include_directories(
  ${1_PUBLIC_INCLUDE_DIRS}
)

add_executable(hello ${main_SRCS})
target_link_libraries(hello ${Hello_SHARED_LIB})
