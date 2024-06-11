cmake_minimum_required(VERSION 3.8)
project(simodel_win64) #项目名称

set(SOURCE_FILE
	code/libsimodel_ert_shrlib_rtw/libsimodel.c
)
# 依赖的头文件
include_directories(
	${PROJECT_SOURCE_DIR}/R2021a/simulink/include/
	${PROJECT_SOURCE_DIR}/code/libsimodel_ert_shrlib_rtw/
)

# 设置生成库文件的路径(静态库\动态库都可行)
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR})

MESSAGE("PROJECT_SOURCE_DIR:${PROJECT_SOURCE_DIR}")
MESSAGE("PROJECT_NAME:${PROJECT_NAME}")
MESSAGE("PROJECT_SOURCE_FILE:${SOURCE_FILE}")
MESSAGE("LIBRARY_OUTPUT_PATH:${LIBRARY_OUTPUT_PATH}")

# 生成静态库文件
# add_library(${PROJECT_NAME} STATIC ${SOURCE_FILE})

# 生成动态库文件
add_library(${PROJECT_NAME} SHARED ${SOURCE_FILE})
