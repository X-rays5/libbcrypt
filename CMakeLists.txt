cmake_minimum_required(VERSION 3.20)
project(libbcrypt)
add_library(libbcrypt STATIC src/bcrypt.c  src/crypt_blowfish.c  src/crypt_gensalt.c  src/wrapper.c  include/bcrypt/bcrypt.h  include/bcrypt/BCrypt.hpp  include/bcrypt/crypt.h  include/bcrypt/crypt_blowfish.h  include/bcrypt/crypt_gensalt.h  include/bcrypt/ow-crypt.h  include/bcrypt/winbcrypt.h )
set_property(TARGET libbcrypt PROPERTY C_STANDARD 11)