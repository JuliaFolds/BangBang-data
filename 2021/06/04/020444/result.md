# Benchmark result

* Pull request commit: [`5b5389ede90b6596ec55f2a360418710c9323ea8`](https://github.com/JuliaFolds/BangBang.jl/commit/5b5389ede90b6596ec55f2a360418710c9323ea8)
* Pull request: <https://github.com/JuliaFolds/BangBang.jl/pull/202> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmarks:
    - Target: 4 Jun 2021 - 02:01
    - Baseline: 4 Jun 2021 - 02:04
* Package commits:
    - Target: 8617cd
    - Baseline: eecbf8
* Julia commits:
    - Target: 44fa15
    - Baseline: 44fa15
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: None
    - Baseline: None

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                                                       | time ratio                   | memory ratio                 |
|------------------------------------------------------------------------------------------|------------------------------|------------------------------|
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                   | 0.76 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                    | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                              | 0.78 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collectors", ":comp => \"filter\"", ":impl => \"base\""]`                             |                1.06 (5%) :x: |                   1.00 (1%)  |
| `["collectors", ":comp => \"filter\"", ":impl => \"coll\""]`                             | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collectors", ":comp => \"filter\"", ":impl => \"nonexpanding\""]`                     | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collectors", ":comp => \"filter\"", ":impl => \"vec\""]`                              |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["collectors", ":comp => \"map\"", ":impl => \"coll\""]`                                | 0.90 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collectors", ":comp => \"map\"", ":impl => \"man\""]`                                 |                1.31 (5%) :x: |                   1.00 (1%)  |
| `["collectors", ":comp => \"map\"", ":impl => \"vec\""]`                                 |                1.15 (5%) :x: |                   1.00 (1%)  |
| `["dataframes", "Categorical"]`                                                          | 0.88 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["dataframes", "Missing-Int"]`                                                          | 0.94 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["dataframes", "Missing-String"]`                                                       | 0.93 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["dataframes", "String-String"]`                                                        | 0.91 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :empty"]`     |                1.16 (5%) :x: |                   1.00 (1%)  |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :equal"]`     |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :half"]`      | 0.92 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :empty"]` | 0.85 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :equal"]` | 0.83 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :half"]`  | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append"]`
- `["collectors", ":comp => \"filter\""]`
- `["collectors", ":comp => \"map\""]`
- `["dataframes"]`
- `["mergewith", ":combine => :+", ":desttype => :compatible"]`
- `["mergewith", ":combine => :+", ":desttype => :widen"]`
- `["mergewith", ":combine => :right", ":desttype => :compatible"]`
- `["mergewith", ":combine => :right", ":desttype => :widen"]`

## Julia versioninfo

### Target
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1047-azure #49-Ubuntu SMP Thu Apr 22 14:30:37 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      29429 s         18 s       1681 s      39537 s          0 s
       #2  2294 MHz      10640 s          4 s       1746 s      58372 s          0 s
       
  Memory: 6.791339874267578 GB (3546.67578125 MB free)
  Uptime: 714.0 sec
  Load Avg:  1.05615234375  0.8427734375  0.45458984375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1047-azure #49-Ubuntu SMP Thu Apr 22 14:30:37 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      34021 s         18 s       1972 s      50886 s          0 s
       #2  2294 MHz      21975 s          4 s       2150 s      62869 s          0 s
       
  Memory: 6.791339874267578 GB (3548.609375 MB free)
  Uptime: 877.0 sec
  Load Avg:  1.1318359375  0.94775390625  0.560546875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 4 Jun 2021 - 2:1
* Package commit: 8617cd
* Julia commit: 44fa15
* Julia command flags: None
* Environment variables: None

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                                                       | time            | GC time   | memory          | allocations |
|------------------------------------------------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                   |   9.700 ns (5%) |           |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                    | 407.700 μs (5%) |           |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                              |   9.700 ns (5%) |           |                 |             |
| `["collectors", ":comp => \"filter\"", ":impl => \"base\""]`                             |  40.600 μs (5%) |           | 128.66 KiB (1%) |          14 |
| `["collectors", ":comp => \"filter\"", ":impl => \"coll\""]`                             |  44.400 μs (5%) |           | 284.81 KiB (1%) |        5012 |
| `["collectors", ":comp => \"filter\"", ":impl => \"nonexpanding\""]`                     |  42.000 μs (5%) |           | 312.75 KiB (1%) |        5005 |
| `["collectors", ":comp => \"filter\"", ":impl => \"vec\""]`                              |  44.600 μs (5%) |           | 128.59 KiB (1%) |          13 |
| `["collectors", ":comp => \"map\"", ":impl => \"coll\""]`                                |   5.333 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"man\""]`                                 |   6.660 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"safe_coll\""]`                           |   9.400 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"vec\""]`                                 |  72.600 μs (5%) |           | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                          | 680.324 ms (5%) | 94.405 ms | 889.14 MiB (1%) |     4925452 |
| `["dataframes", "Int-Int"]`                                                              | 973.601 μs (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                          |   1.318 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                       |   1.365 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                        |   1.285 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :empty"]`     |  45.600 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :equal"]`     |  18.800 μs (5%) |           |                 |             |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :half"]`      |  34.200 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :+", ":desttype => :widen", ":destkeys => :empty"]`          |  42.700 μs (5%) |           |  92.31 KiB (1%) |          18 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :empty"]` |  41.500 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :equal"]` |  16.600 μs (5%) |           |                 |             |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :half"]`  |  29.400 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :right", ":desttype => :widen", ":destkeys => :empty"]`      |  48.400 μs (5%) |           |  92.31 KiB (1%) |          18 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append"]`
- `["collectors", ":comp => \"filter\""]`
- `["collectors", ":comp => \"map\""]`
- `["dataframes"]`
- `["mergewith", ":combine => :+", ":desttype => :compatible"]`
- `["mergewith", ":combine => :+", ":desttype => :widen"]`
- `["mergewith", ":combine => :right", ":desttype => :compatible"]`
- `["mergewith", ":combine => :right", ":desttype => :widen"]`

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1047-azure #49-Ubuntu SMP Thu Apr 22 14:30:37 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      29429 s         18 s       1681 s      39537 s          0 s
       #2  2294 MHz      10640 s          4 s       1746 s      58372 s          0 s
       
  Memory: 6.791339874267578 GB (3546.67578125 MB free)
  Uptime: 714.0 sec
  Load Avg:  1.05615234375  0.8427734375  0.45458984375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 4 Jun 2021 - 2:4
* Package commit: eecbf8
* Julia commit: 44fa15
* Julia command flags: None
* Environment variables: None

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                                                       | time            | GC time    | memory          | allocations |
|------------------------------------------------------------------------------------------|----------------:|-----------:|----------------:|------------:|
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                   |  12.800 ns (5%) |            |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                    | 442.600 μs (5%) |            |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                              |  12.400 ns (5%) |            |                 |             |
| `["collectors", ":comp => \"filter\"", ":impl => \"base\""]`                             |  38.300 μs (5%) |            | 128.66 KiB (1%) |          14 |
| `["collectors", ":comp => \"filter\"", ":impl => \"coll\""]`                             |  47.699 μs (5%) |            | 284.81 KiB (1%) |        5012 |
| `["collectors", ":comp => \"filter\"", ":impl => \"nonexpanding\""]`                     |  48.100 μs (5%) |            | 312.75 KiB (1%) |        5005 |
| `["collectors", ":comp => \"filter\"", ":impl => \"vec\""]`                              |  41.500 μs (5%) |            | 128.59 KiB (1%) |          13 |
| `["collectors", ":comp => \"map\"", ":impl => \"coll\""]`                                |   5.900 μs (5%) |            |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"man\""]`                                 |   5.100 μs (5%) |            |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"safe_coll\""]`                           |   9.600 μs (5%) |            |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"vec\""]`                                 |  63.300 μs (5%) |            | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                          | 776.717 ms (5%) | 100.325 ms | 909.14 MiB (1%) |     5335052 |
| `["dataframes", "Int-Int"]`                                                              | 972.401 μs (5%) |            | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                          |   1.399 ms (5%) |            | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                       |   1.473 ms (5%) |            | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                        |   1.404 ms (5%) |            | 160.27 KiB (1%) |       10252 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :empty"]`     |  39.200 μs (5%) |            |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :equal"]`     |  17.600 μs (5%) |            |                 |             |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :half"]`      |  37.100 μs (5%) |            |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :+", ":desttype => :widen", ":destkeys => :empty"]`          |  44.500 μs (5%) |            |  92.31 KiB (1%) |          18 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :empty"]` |  48.700 μs (5%) |            |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :equal"]` |  19.900 μs (5%) |            |                 |             |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :half"]`  |  33.800 μs (5%) |            |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :right", ":desttype => :widen", ":destkeys => :empty"]`      |  47.101 μs (5%) |            |  92.31 KiB (1%) |          18 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append"]`
- `["collectors", ":comp => \"filter\""]`
- `["collectors", ":comp => \"map\""]`
- `["dataframes"]`
- `["mergewith", ":combine => :+", ":desttype => :compatible"]`
- `["mergewith", ":combine => :+", ":desttype => :widen"]`
- `["mergewith", ":combine => :right", ":desttype => :compatible"]`
- `["mergewith", ":combine => :right", ":desttype => :widen"]`

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1047-azure #49-Ubuntu SMP Thu Apr 22 14:30:37 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      34021 s         18 s       1972 s      50886 s          0 s
       #2  2294 MHz      21975 s          4 s       2150 s      62869 s          0 s
       
  Memory: 6.791339874267578 GB (3548.609375 MB free)
  Uptime: 877.0 sec
  Load Avg:  1.1318359375  0.94775390625  0.560546875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, broadwell)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:                    x86_64
    CPU op-mode(s):                  32-bit, 64-bit
    Byte Order:                      Little Endian
    Address sizes:                   46 bits physical, 48 bits virtual
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    NUMA node(s):                    1
    Vendor ID:                       GenuineIntel
    CPU family:                      6
    Model:                           79
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:                        1
    CPU MHz:                         2294.686
    BogoMIPS:                        4589.37
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        50 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Vulnerable
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

