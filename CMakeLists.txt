cmake_minimum_required(VERSION 3.10)

# set the project name
project(mcquote_bot)

include_directories("telebot/include" "mcquote/include")
add_subdirectory("telebot")
add_subdirectory("mcquote")

add_executable(ishlun-bot src/echobot.c)

target_link_libraries(ishlun-bot mcquote telebot pthread)
