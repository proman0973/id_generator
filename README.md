# german_passport_generator
Library to generate german passport serial as described in https://de.wikipedia.org/wiki/Ausweisnummer

This is useful for several situations such as bypassing age restrictions (which i don't recommend) or for staying anonymous when such information is needed.

Note:
I'm not responsible for possible harm or damage caused by the usage of this library since this is for educational use only

![alt text](id.jpg)
Original image source: https://upload.wikimedia.org/wikipedia/commons/0/04/Muster_des_Personalausweises_RS.jpg

# Example usage
*CMakeLists.txt*
```
cmake_minimum_required(VERSION 3.10)
project(example_project)

set(CMAKE_CXX_STANDARD 17)

add_executable(example_project example.cpp)
target_include_directories(example_project id_generator)
```

*example.cpp*
```
#include <iostream>

#include <id_generator.h>

int main(int argc, char* argv[]) {
    // Erika Mustermann example
    auto id = id_generator("T002", "640812", "201031");
    
    std::cout << "Generated id:\n" << id.to_string();
}
```

*Program output*
```
Generated id:
IDD<<T00207CEG6<<<<<<<<<<<<<<<
6408125<2010315D<<<<<<<<<<<<<8
```
