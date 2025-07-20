cmake_minimum_required(VERSION 3.10)
project(hello VERSION 1.0 LANGUAGES C)

# 直接指明源文件路径
add_executable(hello src/main.c)

# 安装规则
install(TARGETS hello DESTINATION bin)