# Benchmark result

* Pull request commit: [`2de63551edb287d49ceecd8368e81d63ddc14c96`](https://github.com/JuliaFolds/BangBang.jl/commit/2de63551edb287d49ceecd8368e81d63ddc14c96)
* Pull request: <https://github.com/JuliaFolds/BangBang.jl/pull/202> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmarks:
    - Target: 24 Apr 2021 - 01:09
    - Baseline: 24 Apr 2021 - 01:11
* Package commits:
    - Target: 7ad654
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

| ID                                                                                       | time ratio                   | memory ratio |
|------------------------------------------------------------------------------------------|------------------------------|--------------|
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                   | 0.91 (5%) :white_check_mark: |   1.00 (1%)  |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                    | 0.86 (5%) :white_check_mark: |   1.00 (1%)  |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                              | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["collectors", ":comp => \"filter\"", ":impl => \"base\""]`                             | 0.93 (5%) :white_check_mark: |   1.00 (1%)  |
| `["collectors", ":comp => \"filter\"", ":impl => \"coll\""]`                             | 0.89 (5%) :white_check_mark: |   1.00 (1%)  |
| `["collectors", ":comp => \"filter\"", ":impl => \"nonexpanding\""]`                     | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["collectors", ":comp => \"filter\"", ":impl => \"vec\""]`                              | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["collectors", ":comp => \"map\"", ":impl => \"coll\""]`                                |                1.07 (5%) :x: |   1.00 (1%)  |
| `["collectors", ":comp => \"map\"", ":impl => \"man\""]`                                 | 0.88 (5%) :white_check_mark: |   1.00 (1%)  |
| `["collectors", ":comp => \"map\"", ":impl => \"safe_coll\""]`                           | 0.89 (5%) :white_check_mark: |   1.00 (1%)  |
| `["collectors", ":comp => \"map\"", ":impl => \"vec\""]`                                 | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["dataframes", "Categorical"]`                                                          | 0.80 (5%) :white_check_mark: |   1.00 (1%)  |
| `["dataframes", "Int-Int"]`                                                              | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["dataframes", "Missing-Int"]`                                                          | 0.89 (5%) :white_check_mark: |   1.00 (1%)  |
| `["dataframes", "Missing-String"]`                                                       | 0.89 (5%) :white_check_mark: |   1.00 (1%)  |
| `["dataframes", "String-String"]`                                                        | 0.87 (5%) :white_check_mark: |   1.00 (1%)  |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :empty"]`     | 0.81 (5%) :white_check_mark: |   1.00 (1%)  |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :equal"]`     | 0.82 (5%) :white_check_mark: |   1.00 (1%)  |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :half"]`      | 0.87 (5%) :white_check_mark: |   1.00 (1%)  |
| `["mergewith", ":combine => :+", ":desttype => :widen", ":destkeys => :empty"]`          | 0.79 (5%) :white_check_mark: |   1.00 (1%)  |
| `["mergewith", ":combine => :right", ":desttype => :widen", ":destkeys => :empty"]`      | 0.83 (5%) :white_check_mark: |   1.00 (1%)  |

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
  uname: Linux 5.4.0-1046-azure #48-Ubuntu SMP Tue Apr 13 07:18:42 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       6600 s          8 s       1146 s      54674 s          0 s
       #2  2593 MHz      27305 s          9 s       1386 s      34135 s          0 s
       
  Memory: 6.791343688964844 GB (3449.8515625 MB free)
  Uptime: 632.0 sec
  Load Avg:  1.05126953125  0.74853515625  0.36474609375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.4.0-1046-azure #48-Ubuntu SMP Tue Apr 13 07:18:42 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      16555 s          8 s       1538 s      57856 s          0 s
       #2  2593 MHz      30542 s          9 s       1589 s      44213 s          0 s
       
  Memory: 6.791343688964844 GB (3456.71875 MB free)
  Uptime: 767.0 sec
  Load Avg:  1.02392578125  0.85791015625  0.46142578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 24 Apr 2021 - 1:9
* Package commit: 7ad654
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
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                   |  10.310 ns (5%) |           |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                    | 430.908 μs (5%) |           |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                              |  10.000 ns (5%) |           |                 |             |
| `["collectors", ":comp => \"filter\"", ":impl => \"base\""]`                             |  35.801 μs (5%) |           | 128.66 KiB (1%) |          14 |
| `["collectors", ":comp => \"filter\"", ":impl => \"coll\""]`                             |  44.601 μs (5%) |           | 284.81 KiB (1%) |        5012 |
| `["collectors", ":comp => \"filter\"", ":impl => \"nonexpanding\""]`                     |  38.301 μs (5%) |           | 312.75 KiB (1%) |        5005 |
| `["collectors", ":comp => \"filter\"", ":impl => \"vec\""]`                              |  35.900 μs (5%) |           | 128.59 KiB (1%) |          13 |
| `["collectors", ":comp => \"map\"", ":impl => \"coll\""]`                                |   8.800 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"man\""]`                                 |   7.600 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"safe_coll\""]`                           |  10.400 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"vec\""]`                                 |  66.002 μs (5%) |           | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                          | 502.050 ms (5%) | 77.045 ms | 909.14 MiB (1%) |     5335052 |
| `["dataframes", "Int-Int"]`                                                              |   1.071 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                          |   1.499 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                       |   1.325 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                        |   1.293 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :empty"]`     |  34.900 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :equal"]`     |  18.801 μs (5%) |           |                 |             |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :half"]`      |  33.500 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :+", ":desttype => :widen", ":destkeys => :empty"]`          |  34.101 μs (5%) |           |  92.31 KiB (1%) |          18 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :empty"]` |  37.300 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :equal"]` |  18.701 μs (5%) |           |                 |             |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :half"]`  |  34.001 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :right", ":desttype => :widen", ":destkeys => :empty"]`      |  34.801 μs (5%) |           |  92.31 KiB (1%) |          18 |

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
  uname: Linux 5.4.0-1046-azure #48-Ubuntu SMP Tue Apr 13 07:18:42 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz       6600 s          8 s       1146 s      54674 s          0 s
       #2  2593 MHz      27305 s          9 s       1386 s      34135 s          0 s
       
  Memory: 6.791343688964844 GB (3449.8515625 MB free)
  Uptime: 632.0 sec
  Load Avg:  1.05126953125  0.74853515625  0.36474609375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 24 Apr 2021 - 1:11
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

| ID                                                                                       | time            | GC time   | memory          | allocations |
|------------------------------------------------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                   |  11.311 ns (5%) |           |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                    | 502.607 μs (5%) |           |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                              |  11.300 ns (5%) |           |                 |             |
| `["collectors", ":comp => \"filter\"", ":impl => \"base\""]`                             |  38.701 μs (5%) |           | 128.66 KiB (1%) |          14 |
| `["collectors", ":comp => \"filter\"", ":impl => \"coll\""]`                             |  50.301 μs (5%) |           | 284.81 KiB (1%) |        5012 |
| `["collectors", ":comp => \"filter\"", ":impl => \"nonexpanding\""]`                     |  43.701 μs (5%) |           | 312.75 KiB (1%) |        5005 |
| `["collectors", ":comp => \"filter\"", ":impl => \"vec\""]`                              |  39.200 μs (5%) |           | 128.59 KiB (1%) |          13 |
| `["collectors", ":comp => \"map\"", ":impl => \"coll\""]`                                |   8.200 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"man\""]`                                 |   8.600 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"safe_coll\""]`                           |  11.701 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"vec\""]`                                 |  72.001 μs (5%) |           | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                          | 628.658 ms (5%) | 88.749 ms | 909.14 MiB (1%) |     5335052 |
| `["dataframes", "Int-Int"]`                                                              |   1.169 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                          |   1.682 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                       |   1.493 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                        |   1.486 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :empty"]`     |  43.201 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :equal"]`     |  23.000 μs (5%) |           |                 |             |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :half"]`      |  38.701 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :+", ":desttype => :widen", ":destkeys => :empty"]`          |  43.101 μs (5%) |           |  92.31 KiB (1%) |          18 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :empty"]` |  36.001 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :equal"]` |  18.400 μs (5%) |           |                 |             |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :half"]`  |  33.300 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :right", ":desttype => :widen", ":destkeys => :empty"]`      |  41.900 μs (5%) |           |  92.31 KiB (1%) |          18 |

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
  uname: Linux 5.4.0-1046-azure #48-Ubuntu SMP Tue Apr 13 07:18:42 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      16555 s          8 s       1538 s      57856 s          0 s
       #2  2593 MHz      30542 s          9 s       1589 s      44213 s          0 s
       
  Memory: 6.791343688964844 GB (3456.71875 MB free)
  Uptime: 767.0 sec
  Load Avg:  1.02392578125  0.85791015625  0.46142578125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
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
    Model:                           85
    Model name:                      Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    Stepping:                        7
    CPU MHz:                         2593.906
    BogoMIPS:                        5187.81
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        2 MiB
    L3 cache:                        35.8 MiB
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
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz          |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x07, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

