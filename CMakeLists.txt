cmake_minimum_required(VERSION 2.8.3)
project(serial)
include_directories(
  include
  src
)
set(SERIAL_SOURCES
  src/serial.cc
  include/serial/serial.h
  include/serial/v8stdint.h
  src/impl/unix.cc
  src/impl/list_ports/list_ports_linux.cc
)
add_library(serial ${SERIAL_SOURCES})
target_link_libraries(serial rt)
