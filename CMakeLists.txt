cmake_minimum_required(VERSION 3.0.0)
project(GAME VERSION 0.1.0)

set(SFML_DIR "./lib/SFML/lib/cmake/SFML")

set(SOURCE_FILES
        src/main.cpp
        src/components/component.cc
        src/components/texture.cc
        src/components/controller/controller.cc
        src/components/controller/playerController.cc
        src/components/entities/testPlayer.cc
        src/world.cc
        src/states/playState.cc
        src/states/stateMachine.cc
        src/helpers/textureHandler.cc
        src/map/tileMap.cc
        src/components/hitbox.cc
        src/structures/quadtree.cc
        )


find_package(SFML 2.5.1 COMPONENTS graphics audio window REQUIRED)
add_executable(game ${SOURCE_FILES})
target_link_libraries(game sfml-graphics sfml-audio sfml-window)
