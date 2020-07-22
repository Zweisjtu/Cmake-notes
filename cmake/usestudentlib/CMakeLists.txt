cmake_minimum_required(VERSION 2.8.9)
project (TestLibrary)

#设置共享库
set ( PROJECT_LINK_LIBS libtestStudent.so )
link_directories(~/Documents/backup/extras/cmake/studentlib_shared/build )

#设置静态库
#set ( PROJECT_LINK_LIBS libtestStudent.a )
#link_directories( ~/exploringBB/extras/cmake/studentlib_static/build )

#添加头文件的目录
include_directories(~/Documents/backup/extras/cmake/studentlib_shared/include)

#添加可执行程序生成命令
add_executable(libtest libtest.cpp)
#将可执行文件链接到库上
target_link_libraries(libtest ${PROJECT_LINK_LIBS} )
