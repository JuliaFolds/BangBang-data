# Benchmark result

* Pull request commit: [`de4d402b73e5b8f46c68372d6c3b0a8d4d82828d`](https://github.com/JuliaFolds/BangBang.jl/commit/de4d402b73e5b8f46c68372d6c3b0a8d4d82828d)
* Pull request: <https://github.com/JuliaFolds/BangBang.jl/pull/202> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmarks:
    - Target: 7 Jul 2021 - 01:03
    - Baseline: 7 Jul 2021 - 01:06
* Package commits:
    - Target: 49c4c8
    - Baseline: a10491
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
| `["collectors", ":comp => \"map\"", ":impl => \"coll\""]`                                | 0.63 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["collectors", ":comp => \"map\"", ":impl => \"man\""]`                                 | 0.62 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["dataframes", "Categorical"]`                                                          | 0.93 (5%) :white_check_mark: | 0.98 (1%) :white_check_mark: |
| `["dataframes", "String-String"]`                                                        | 0.95 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["mergewith", ":combine => :right", ":desttype => :widen", ":destkeys => :empty"]`      |                1.07 (5%) :x: |                   1.00 (1%)  |

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
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz       7383 s         21 s       1418 s      33970 s          0 s
       #2  2397 MHz      31946 s          6 s       1560 s       9768 s          0 s
       
  Memory: 6.790924072265625 GB (3424.52734375 MB free)
  Uptime: 437.0 sec
  Load Avg:  1.0  0.84130859375  0.43896484375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, haswell)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 20.04.2 LTS
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      18644 s         21 s       1797 s      37388 s          0 s
       #2  2397 MHz      35451 s          6 s       1780 s      21082 s          0 s
       
  Memory: 6.790924072265625 GB (3509.9453125 MB free)
  Uptime: 587.0 sec
  Load Avg:  1.0078125  0.9208984375  0.53466796875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 7 Jul 2021 - 1:3
* Package commit: 49c4c8
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
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                   |  11.900 ns (5%) |           |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                    | 496.624 μs (5%) |           |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                              |  11.900 ns (5%) |           |                 |             |
| `["collectors", ":comp => \"filter\"", ":impl => \"base\""]`                             |  42.102 μs (5%) |           | 128.66 KiB (1%) |          14 |
| `["collectors", ":comp => \"filter\"", ":impl => \"coll\""]`                             |  50.002 μs (5%) |           | 284.81 KiB (1%) |        5012 |
| `["collectors", ":comp => \"filter\"", ":impl => \"nonexpanding\""]`                     |  51.503 μs (5%) |           | 312.75 KiB (1%) |        5005 |
| `["collectors", ":comp => \"filter\"", ":impl => \"vec\""]`                              |  44.002 μs (5%) |           | 128.59 KiB (1%) |          13 |
| `["collectors", ":comp => \"map\"", ":impl => \"coll\""]`                                |   5.300 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"man\""]`                                 |   5.100 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"safe_coll\""]`                           |  10.200 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"vec\""]`                                 |  77.604 μs (5%) |           | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                          | 640.602 ms (5%) | 91.239 ms | 889.14 MiB (1%) |     4925452 |
| `["dataframes", "Int-Int"]`                                                              |   1.098 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                          |   1.527 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                       |   1.547 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                        |   1.466 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :empty"]`     |  47.002 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :equal"]`     |  22.201 μs (5%) |           |                 |             |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :half"]`      |  37.901 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :+", ":desttype => :widen", ":destkeys => :empty"]`          |  43.303 μs (5%) |           |  92.31 KiB (1%) |          18 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :empty"]` |  47.302 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :equal"]` |  21.301 μs (5%) |           |                 |             |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :half"]`  |  37.701 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :right", ":desttype => :widen", ":destkeys => :empty"]`      |  48.103 μs (5%) |           |  92.31 KiB (1%) |          18 |

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
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz       7383 s         21 s       1418 s      33970 s          0 s
       #2  2397 MHz      31946 s          6 s       1560 s       9768 s          0 s
       
  Memory: 6.790924072265625 GB (3424.52734375 MB free)
  Uptime: 437.0 sec
  Load Avg:  1.0  0.84130859375  0.43896484375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 7 Jul 2021 - 1:6
* Package commit: a10491
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
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                   |  11.900 ns (5%) |           |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                    | 486.623 μs (5%) |           |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                              |  11.900 ns (5%) |           |                 |             |
| `["collectors", ":comp => \"filter\"", ":impl => \"base\""]`                             |  42.002 μs (5%) |           | 128.66 KiB (1%) |          14 |
| `["collectors", ":comp => \"filter\"", ":impl => \"coll\""]`                             |  51.102 μs (5%) |           | 284.81 KiB (1%) |        5012 |
| `["collectors", ":comp => \"filter\"", ":impl => \"nonexpanding\""]`                     |  52.802 μs (5%) |           | 312.75 KiB (1%) |        5005 |
| `["collectors", ":comp => \"filter\"", ":impl => \"vec\""]`                              |  43.302 μs (5%) |           | 128.59 KiB (1%) |          13 |
| `["collectors", ":comp => \"map\"", ":impl => \"coll\""]`                                |   8.400 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"man\""]`                                 |   8.201 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"safe_coll\""]`                           |  10.201 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", ":comp => \"map\"", ":impl => \"vec\""]`                                 |  80.404 μs (5%) |           | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                          | 691.332 ms (5%) | 87.687 ms | 909.14 MiB (1%) |     5335052 |
| `["dataframes", "Int-Int"]`                                                              |   1.107 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                          |   1.467 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                       |   1.491 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                        |   1.547 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :empty"]`     |  48.502 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :equal"]`     |  22.301 μs (5%) |           |                 |             |
| `["mergewith", ":combine => :+", ":desttype => :compatible", ":destkeys => :half"]`      |  38.702 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :+", ":desttype => :widen", ":destkeys => :empty"]`          |  44.302 μs (5%) |           |  92.31 KiB (1%) |          18 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :empty"]` |  48.102 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :equal"]` |  21.501 μs (5%) |           |                 |             |
| `["mergewith", ":combine => :right", ":desttype => :compatible", ":destkeys => :half"]`  |  39.102 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", ":combine => :right", ":desttype => :widen", ":destkeys => :empty"]`      |  44.802 μs (5%) |           |  92.31 KiB (1%) |          18 |

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
  uname: Linux 5.8.0-1036-azure #38~20.04.1-Ubuntu SMP Thu Jun 17 14:14:18 UTC 2021 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      18644 s         21 s       1797 s      37388 s          0 s
       #2  2397 MHz      35451 s          6 s       1780 s      21082 s          0 s
       
  Memory: 6.790924072265625 GB (3509.9453125 MB free)
  Uptime: 587.0 sec
  Load Avg:  1.0078125  0.9208984375  0.53466796875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, haswell)
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
    Model:                           63
    Model name:                      Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz
    Stepping:                        2
    CPU MHz:                         2397.221
    BogoMIPS:                        4794.44
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB
    L1i cache:                       64 KiB
    L2 cache:                        512 KiB
    L3 cache:                        30 MiB
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Full generic retpoline, STIBP disabled, RSB filling
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Not affected
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm invpcid_single pti fsgsbase bmi1 avx2 smep bmi2 erms invpcid xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Haswell                                                |
| Model              | Family: 0x06, Model: 0x3f, Stepping: 0x02, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 30720) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

