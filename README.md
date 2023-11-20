# ccminer for ARM (cortex-a53)

Based on https://github.com/monkins1010/ccminer/tree/ARM

Userland Git and Build Process:
```
sudo apt-get update
sudo apt-get install libcurl4-openssl-dev libssl-dev libjansson-dev automake autotools-dev build-essential -y
sudo apt-get install -y clang-format clang-tidy clang-tools clang clangd libc++-dev libc++1 libc++abi-dev libc++abi1 libclang-dev libclang1 liblldb-dev libllvm-ocaml-dev libomp-dev libomp5 lld lldb llvm-dev llvm-runtime llvm python3-clang
git clone https://github.com/Oink70/CCminer-ARM-optimized.git
cd CCminer-ARM-optimized
chmod +x build.sh
chmod +x configure.sh
chmod +x autogen.sh
CXX=clang++ CC=clang build.sh
```
Termux Git and Build Process:
```
pkg update -y
pkg upgrade -y
pkg install openssl libjansson automake build-essential clang lld curl git binutils
git clone https://github.com/uncharted9898/CCminer-ARM-optimized.git
cp /data/data/com.termux/files/usr/include/linux/sysctl.h /data/data/com.termux/files/usr/include/sys
cd CCminer-ARM-optimized
chmod +x build.sh
chmod +x configure.sh
chmod +x autogen.sh
CXX=clang++ CC=clang ./build.sh
```

For specific details on installing clang-16 on your current OS, check: https://apt.llvm.org/
