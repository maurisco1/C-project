import PackageDescription
//paste here later
let package = Package(
    name: "whisper",
    platforms: [
        .macOS(.v12),
        .iOS(.v14),
        .watchOS(.v4),
        .tvOS(.v14)
    ],
    products: [
        .library(name: "whisper", targets: ["whisper"]),
    ],
    targets: [
        .target(
            name: "whisper",
            path: ".",
            exclude: [
               "bindings",
               "cmake",
               "coreml",
               "examples",
               "extra",
               "models",
               "samples",
               "tests",
               "CMakeLists.txt",
               "ggml-cuda.cu",
               "ggml-cuda.h",
               "Makefile"
            ],
            sources: [
                "ggml.c",
                "whisper.cpp",
                "ggml-alloc.c",
                "ggml-backend.c",
                "ggml-quants.c",
                "ggml-metal.m"
            ],
//i like to code


      cmake_minimum_required( VERSION 2.6 )
project( algorithm )

include_directories( "include" )
include_directories( "." )
if( MSVC )
	include_directories( "msvc" )
endif()
file( GLOB APP_SOURCES src/*.cpp )
SET( CMAKE_CXX_FLAGS  "${CMAKE_CXX_FLAGS} /FI\"msvc/alg_vs.h\"" ) 
message( ${CMAKE_CXX_FLAGS} )
foreach( appsourcefile ${APP_SOURCES} )
	get_filename_component( demo_name ${appsourcefile} NAME_WE )
	add_executable( ${demo_name} ${appsourcefile} )
endforeach( appsourcefile ${APP_SOURCES} )
