cmake_minimum_required(VERSION 3.11) # FetchContent is available in 3.11+
project(advance_game)

# Set this to the minimal version you want to support
find_package(raylib CONFIG REQUIRED) # Let CMake search for a raylib-config.cmake

# This is the main part:

add_executable(${PROJECT_NAME}
  advance_game.c
  screens/screen_logo.c
  screens/screen_title.c
  screens/screen_options.c
  screens/screen_gameplay.c
  screens/screen_ending.c
  )

#set(raylib_VERBOSE 1)
target_include_directories(${PROJECT_NAME} PRIVATE ${RAYLIB_INCLUDE_DIRS})
target_link_libraries(${PROJECT_NAME} PRIVATE ${RAYLIB_LIBRARIES})

# That's it! You should have an example executable that you can run. Have fun!
