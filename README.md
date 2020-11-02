
cmake -S . -B build
cmake --build build

./build/main


OSD_Host::InternetAddress() segfaults, because gethostbyname(Hostname()) returns a null pointer


