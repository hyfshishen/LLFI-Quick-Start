# LLFI-Quick-Start

0. Change directory to fault injection base
```
# example
cd perInstFI                            # per-Instruction FI
cd randomFI                             # random FI
```

1. Compile sqrt.c to readable IR:
```
clang -emit-llvm -S *.c
```

2. Instrument IR-level codes to readable IR:
```
instrument --readable sqrt.ll
```

3. Profile: run a fault-free IR:
```
profile ./llfi/sqrt-profiling.exe
```

4. Fault Injection: run a fault-injected IR:
```
injectfault ./llfi/sqrt-faultinjection.exe
```
5. Analyze FI results:
```
python3 measure.py
```
