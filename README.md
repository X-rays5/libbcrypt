# libbcrypt
A c++ wrapper around bcrypt password hashing

## How to use

```CMake
add_subdirectory(vendor/libbcrypt)

add_executable(example src/main.cpp)

target_include_directories(example PRIVATE vendor/libbcrypt/include)
target_link_libraries(example PRIVATE libbcrypt)
```

## How to use this

Here an example how to use this wrapper class (you can find a slightly edited example in src/ subdirectory)

```cpp
#include <bcrypt/BCrypt.hpp>
#include <iostream>

int main(){
	std::string password = "test";
	std::string hash = BCrypt::generateHash(password);

	std::cout << BCrypt::validatePassword(password,hash) << std::endl;
	std::cout << BCrypt::validatePassword("test1",hash) << std::endl;

	return 0;
}
```
