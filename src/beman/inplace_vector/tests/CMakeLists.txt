# cmake-format: off
# src/beman/inplace_vector/tests/CMakeLists.txt -*-makefile-*-
# SPDX-License-Identifier: Apache-2.0 WITH LLVM-exception
# cmake-format: on

include(GoogleTest)

# Tests
add_executable(beman.inplace_vector.test inplace_vector.test.cpp)

target_link_libraries(beman.inplace_vector.test PRIVATE beman.inplace_vector)

add_test(NAME beman.inplace_vector.test COMMAND beman.inplace_vector.test)

# Tests
add_executable(beman.inplace_vector.gtest inplace_vector.gtest.cpp)
target_link_libraries(beman.inplace_vector.gtest PRIVATE beman.inplace_vector GTest::gtest GTest::gtest_main)
gtest_add_tests(beman.inplace_vector.gtest "" AUTO)
