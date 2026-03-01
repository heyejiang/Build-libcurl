# libcurl for MSVC

Pre-built libcurl binaries for Windows with MSVC.

## Version 8.18.0

## Features
- OpenSSL support
- SSH support (libssh2)
- HTTP/2 support (nghttp2)
- Public Suffix List (PSL)

## Architectures
- x64 (64-bit)
- x86 (32-bit)

## Library Files
- libcurl.lib (static library)
- libcurl_imp.lib (import library for DLL)
- libssl.lib
- libcrypto.lib
- libssh2.lib

## System Libraries Required
- crypt32.lib
- bcrypt.lib (for OpenSSL)
- user32.lib (for OpenSSL)

## Static Build
- Use: libcurl.lib + all dependency libs
- Define: `CURL_STATICLIB`
- Example: `target_link_libraries(your_target libcurl libssl libcrypto libssh2 crypt32 bcrypt user32)`

## Dynamic Build
- Use: libcurl_imp.lib
- DLLs in bin/ folder
- Example: `target_link_libraries(your_target libcurl_imp)`

## Downloads

### Static Libraries
- [x64](libcurl-8.18.0-x64-static.zip)

### Shared Libraries
- [x64](libcurl-8.18.0-x64-shared.zip)
