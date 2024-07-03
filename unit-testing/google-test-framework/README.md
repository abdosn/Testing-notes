# Download Gtest

## 1. Cmake 

By writing cmake script you may download Gtest every time the cmake command runs -needs an active internet-

```
cmake minimum required(VERSION 3.14)
project (my project) 

set (CHAKE_OO_ FLAGS ) 
#88 it 1s not the best practise but good to know set 
(CMAKE CXX STANDARD 11) 
include (FetehContent) 

FetchContent_Oectore( googtetest /githud .c jLe/googletest/archive/63597a0 leeSbed33e9dt 45400249b40e37994395. 2 ) 

# unzip it and build it and generate static Lib to Link with it 
FetchContent_MokeAvailable(googletest) 

#to enable ctest 
enable_testing() 
# set src files 
set (SRC_FILE Labl_catc.cpp main.cpp) 
set (SRC_TEST lebl_test.cpp) 
add_executable( ‘S(PROJECT_NAME) ‘S{SRC_FILE} ‘$(SRC_TEST) )

## Less /usr/shore/cmake-3,22/Modules/FindGTest .ceake 

target_Link Libraries( 'S(PROJECT_NAME) GTest::gtest # GTest::gtest_main ) 

#gtest_discover tests to let ctest know which test executables in its database 

include(GoogleTest)
Gtest_discover_tests(5(PROJECT_NAME})

```


## 2. System

> for linux

```
$ sudo apt-get install libgtest-dev
$ sudo apt-get install libgmock-dev

```
to make sure that it's installed

```
$ ls /usr/src/googletest/
CmakeLists.txt  googlemock  googletest

$ find /usr/lib -iname "libgtest*"
/usr/lib/x86_64-linux-gnu/libgtest.a
/usr/lib/x86_64-linux-gnu/libgtest_main.a

$ find /usr/lib -iname "libgmock*"
/usr/lib/x86_64-linux-gnu/libgmock.a
/usr/lib/x86_64-linux-gnu/libgmock_main.a

$ ls /usr/include/gtest/gtest.h
/usr/include/gtest/gtest.h

$ ls /usr/include/gmock/gmock.h
/usr/include/gmock/gmock.h


```


## 3. Manually

by using google test github [link](https://github.com/google/googletest)

```
$ git clone https://github.com/google/googletest

$ cd <path-to-repo>

$ mkdir build && cd build/

$ cmake .. 