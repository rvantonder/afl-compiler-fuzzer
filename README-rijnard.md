If on fresh install

```
sudo xcodebuild -license accept
```

Install solidity system deps

```
brew update
brew upgrade
brew tap ethereum/ethereum
brew install solidity
```


```
git clone https://github.com/ethereum/solidity.git
mkdir build
cd build
```

```
cmake .. -DCMAKE_C_COMPILER=/Users/rvt/agroce-afl-compiler-fuzzer/afl-clang -DCMAKE_CXX_COMPILER=/Users/rvt/agroce-afl-compiler-fuzzer/afl-clang++
```

```
make solfuzzer
```


---

Running

```
./afl-fuzz-compiler -d -i sol-programs -o sol-crashes -- ~/solidity/build/test/tools/solfuzzer
```

(`-d` skips deterministic stuff)
