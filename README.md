# OCCT segfault proof of concept

OSD_Host::InternetAddress() segfaults, because gethostbyname(Hostname()) returns a null pointer

# POC
```
#include <OSD_Host.hxx>

int main() {
  OSD_Host host;
  auto a = host.InternetAddress();
}
// that's all it takes
```


# Build Instructions
```
cmake -S . -B build
cmake --build build

./build/main
```



