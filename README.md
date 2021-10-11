# LLFI-Tutorial-Pathfinder

1. Compile pathfinder.cpp to readable IR:
```
clang++ -emit-llvm -S *.cpp
```

2. Instrument IR-level codes to readable IR:
```
instrument --readable pathfinder.ll
```

3. Profile: run a fault-free IR:
```
profile ./llfi/pathfinder-profiling.exe 1000 10
```

4. Fault Injection: run a fault-injected IR:
```
injectfault ./llfi/pathfinder-faultinjection.exe 1000 10
```
