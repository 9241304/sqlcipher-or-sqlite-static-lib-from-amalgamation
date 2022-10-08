cmake_minimum_required(VERSION 3.15)

if (LIB_TYPE STREQUAL sqlite)

elseif (LIB_TYPE STREQUAL sqlcipher)
	add_compile_definitions(SQLITE_HAS_CODEC)
else()
	message(FATAL_ERROR "LIB_TYPE is not defined")
endif()

project(${LIB_TYPE} C)

#add_compile_definitions(SQLITE_ENABLE_COLUMN_METADATA)

add_library($LIB_TYPE STATIC sqlite3.c)