#
# CMakeLists.txt for yast2/ruby-bindings/tests/ruby
#

ENABLE_TESTING()

FILE(GLOB Tests "*_test.rb")

foreach(test ${Tests})
    ADD_TEST(${test}   ruby -C ${CMAKE_CURRENT_SOURCE_DIR} ${test})
endforeach(test)
