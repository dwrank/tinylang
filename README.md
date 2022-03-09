# tinylang
Advanced C and C++ Compiling

## Build LLVM
```
git clone https://github.com/llvm/llvm-project.git
mkdir build
cd build

cmake -G Ninja -DCMAKE_BUID_TYPE=RELEASE \
-DCMAKE_INSTALL_PREFIX=../llvm-12 \
-DLLVM_TARGETS_TO_BUILD="X86" \
-DLLVM_ENABLE_ASSERTIONS=ON \
../llvm-project/llvm

ninja && ninja install
```

## Build tinylang
```
cd ..
git clone git@github.com:dwrank/tinylang.git
mkdir build-tinylang
cd build-tinylang

cmake -G Ninja -DCMAKE_BUID_TYPE=RELEASE \
-DCMAKE_INSTALL_PREFIX=../tinylang \
-DLLVM_DIR=../llvm-12/lib/cmake/llvm \
-DLLVM_TARGETS_TO_BUILD="X86" \
-DLLVM_ENABLE_ASSERTIONS=ON \
../tinylang

ninja && ninja-install
```
