CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

ADD_SUBDIRECTORY(googletest)


SET(CMAKE_CXX_STANDARD 11)


ADD_EXECUTABLE(test
        unit_test.cpp
	Attack.cpp
	Attack.hpp
	Entity.hpp
	Entity.cpp
	GameState.cpp
	GameState.hpp
	Terminal.cpp
	Terminal.hpp	
)

ADD_EXECUTABLE(game
	Attack.cpp
	Entity.cpp
	GameState.cpp
	Terminal.cpp
	main.cpp
)

TARGET_LINK_LIBRARIES(test gtest)
TARGET_COMPILE_DEFINITIONS(test PRIVATE gtest_disable_pthreads=ON)
