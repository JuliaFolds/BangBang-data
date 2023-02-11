# Benchmark result

* Pull request commit: [`52875c4b8d61e65fce17954d461e6ee730c0b851`](https://github.com/JuliaFolds/BangBang.jl/commit/52875c4b8d61e65fce17954d461e6ee730c0b851)
* Pull request: <https://github.com/JuliaFolds/BangBang.jl/pull/202> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmarks:
    - Target: 11 Feb 2023 - 01:21
    - Baseline: 11 Feb 2023 - 01:23
* Package commits:
    - Target: b56a63
    - Baseline: d70a19
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

| ID                                                          | time ratio                   | memory ratio                 |
|-------------------------------------------------------------|------------------------------|------------------------------|
| `["dataframes", "Categorical"]`                             | 0.76 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append"]`
- `["dataframes"]`

## Julia versioninfo

### Target
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1031-azure #38-Ubuntu SMP Mon Jan 9 12:49:59 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz      25306 s          2 s       1398 s      41991 s          0 s
       #2  2793 MHz      12676 s          0 s       1440 s      54521 s          0 s
       
  Memory: 6.781219482421875 GB (3340.375 MB free)
  Uptime: 691.0 sec
  Load Avg:  1.041015625  0.8095703125  0.4208984375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake-avx512)
```

### Baseline
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1031-azure #38-Ubuntu SMP Mon Jan 9 12:49:59 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz      28820 s          2 s       1723 s      51008 s          0 s
       #2  2793 MHz      21904 s          0 s       1708 s      57905 s          0 s
       
  Memory: 6.781219482421875 GB (3319.43359375 MB free)
  Uptime: 820.0 sec
  Load Avg:  1.0029296875  0.8798828125  0.4990234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake-avx512)
```

---
# Target result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 11 Feb 2023 - 1:21
* Package commit: b56a63
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

| ID                                                                                          | time            | GC time   | memory          | allocations |
|---------------------------------------------------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                      |  12.011 ns (5%) |           |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                       | 487.799 μs (5%) |           |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                                 |  12.011 ns (5%) |           |                 |             |
| `["collectors", :(:comp => "filter"), :(:impl => "base")]`                                  |  34.600 μs (5%) |           | 128.66 KiB (1%) |          14 |
| `["collectors", :(:comp => "filter"), :(:impl => "coll")]`                                  |  37.400 μs (5%) |           | 284.81 KiB (1%) |        5012 |
| `["collectors", :(:comp => "filter"), :(:impl => "nonexpanding")]`                          |  33.000 μs (5%) |           | 312.75 KiB (1%) |        5005 |
| `["collectors", :(:comp => "filter"), :(:impl => "vec")]`                                   |  34.800 μs (5%) |           | 128.59 KiB (1%) |          13 |
| `["collectors", :(:comp => "map"), :(:impl => "coll")]`                                     |   4.867 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "man")]`                                      |   4.533 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "safe_coll")]`                                |  12.300 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "vec")]`                                      |  63.000 μs (5%) |           | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                             | 433.915 ms (5%) | 51.235 ms | 804.14 MiB (1%) |     4024332 |
| `["dataframes", "Int-Int"]`                                                                 |   1.096 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                             |   1.413 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                          |   1.422 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                           |   1.367 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :empty)]`     |  23.000 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :equal)]`     |  12.700 μs (5%) |           |                 |             |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :half)]`      |  19.300 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :+), :(:desttype => :widen), :(:destkeys => :empty)]`          |  23.700 μs (5%) |           |  92.31 KiB (1%) |          18 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :empty)]` |  23.100 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :equal)]` |  11.800 μs (5%) |           |                 |             |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :half)]`  |  18.700 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :right), :(:desttype => :widen), :(:destkeys => :empty)]`      |  23.400 μs (5%) |           |  92.31 KiB (1%) |          18 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append"]`
- `["collectors", :(:comp => "filter")]`
- `["collectors", :(:comp => "map")]`
- `["dataframes"]`
- `["mergewith", :(:combine => :+), :(:desttype => :compatible)]`
- `["mergewith", :(:combine => :+), :(:desttype => :widen)]`
- `["mergewith", :(:combine => :right), :(:desttype => :compatible)]`
- `["mergewith", :(:combine => :right), :(:desttype => :widen)]`

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1031-azure #38-Ubuntu SMP Mon Jan 9 12:49:59 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz      25306 s          2 s       1398 s      41991 s          0 s
       #2  2793 MHz      12676 s          0 s       1440 s      54521 s          0 s
       
  Memory: 6.781219482421875 GB (3340.375 MB free)
  Uptime: 691.0 sec
  Load Avg:  1.041015625  0.8095703125  0.4208984375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake-avx512)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 11 Feb 2023 - 1:23
* Package commit: d70a19
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

| ID                                                                                          | time            | GC time   | memory          | allocations |
|---------------------------------------------------------------------------------------------|----------------:|----------:|----------------:|------------:|
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                      |  12.411 ns (5%) |           |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                       | 482.599 μs (5%) |           |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                                 |  12.411 ns (5%) |           |                 |             |
| `["collectors", :(:comp => "filter"), :(:impl => "base")]`                                  |  33.600 μs (5%) |           | 128.66 KiB (1%) |          14 |
| `["collectors", :(:comp => "filter"), :(:impl => "coll")]`                                  |  37.900 μs (5%) |           | 284.81 KiB (1%) |        5012 |
| `["collectors", :(:comp => "filter"), :(:impl => "nonexpanding")]`                          |  34.700 μs (5%) |           | 312.75 KiB (1%) |        5005 |
| `["collectors", :(:comp => "filter"), :(:impl => "vec")]`                                   |  34.100 μs (5%) |           | 128.59 KiB (1%) |          13 |
| `["collectors", :(:comp => "map"), :(:impl => "coll")]`                                     |   5.200 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "man")]`                                      |   4.200 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "safe_coll")]`                                |   9.200 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "vec")]`                                      |  62.899 μs (5%) |           | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                             | 574.495 ms (5%) | 68.821 ms | 909.14 MiB (1%) |     5335052 |
| `["dataframes", "Int-Int"]`                                                                 |   1.090 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                             |   1.436 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                          |   1.411 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                           |   1.373 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :empty)]`     |  23.399 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :equal)]`     |  12.600 μs (5%) |           |                 |             |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :half)]`      |  19.300 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :+), :(:desttype => :widen), :(:destkeys => :empty)]`          |  23.900 μs (5%) |           |  92.31 KiB (1%) |          18 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :empty)]` |  23.500 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :equal)]` |  11.700 μs (5%) |           |                 |             |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :half)]`  |  19.100 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :right), :(:desttype => :widen), :(:destkeys => :empty)]`      |  23.800 μs (5%) |           |  92.31 KiB (1%) |          18 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["append"]`
- `["collectors", :(:comp => "filter")]`
- `["collectors", :(:comp => "map")]`
- `["dataframes"]`
- `["mergewith", :(:combine => :+), :(:desttype => :compatible)]`
- `["mergewith", :(:combine => :+), :(:desttype => :widen)]`
- `["mergewith", :(:combine => :right), :(:desttype => :compatible)]`
- `["mergewith", :(:combine => :right), :(:desttype => :widen)]`

## Julia versioninfo
```
Julia Version 1.4.2
Commit 44fa15b150* (2020-05-23 18:35 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 22.04.1 LTS
  uname: Linux 5.15.0-1031-azure #38-Ubuntu SMP Mon Jan 9 12:49:59 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz: 
              speed         user         nice          sys         idle          irq
       #1  2793 MHz      28820 s          2 s       1723 s      51008 s          0 s
       #2  2793 MHz      21904 s          0 s       1708 s      57905 s          0 s
       
  Memory: 6.781219482421875 GB (3319.43359375 MB free)
  Uptime: 820.0 sec
  Load Avg:  1.0029296875  0.8798828125  0.4990234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake-avx512)
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
    Address sizes:                   46 bits physical, 48 bits virtual
    Byte Order:                      Little Endian
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Vendor ID:                       GenuineIntel
    Model name:                      Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz
    CPU family:                      6
    Model:                           106
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        6
    BogoMIPS:                        5586.88
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       96 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2.5 MiB (2 instances)
    L3 cache:                        48 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Not affected
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8370C CPU @ 2.80GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :UnknownIntel                                           |
| Model              | Family: 0x06, Model: 0x6a, Stepping: 0x06, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading hardware capability detected          |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (48, 1280, 49152) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

