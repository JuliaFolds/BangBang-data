# Benchmark result

* Pull request commit: [`ad8e2d09ab6a3abd2dd9c5a447d8da2bd00c8f99`](https://github.com/JuliaFolds/BangBang.jl/commit/ad8e2d09ab6a3abd2dd9c5a447d8da2bd00c8f99)
* Pull request: <https://github.com/JuliaFolds/BangBang.jl/pull/202> (Update */Manifest.toml)

# Judge result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmarks:
    - Target: 30 Jun 2023 - 01:34
    - Baseline: 30 Jun 2023 - 01:36
* Package commits:
    - Target: 03591f
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
| `["dataframes", "Categorical"]`                             | 0.74 (5%) :white_check_mark: | 0.88 (1%) :white_check_mark: |
| `["dataframes", "Int-Int"]`                                 |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["dataframes", "Missing-String"]`                          |                1.08 (5%) :x: |                   1.00 (1%)  |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1040-azure #47-Ubuntu SMP Thu Jun 1 19:38:24 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      31469 s          1 s       1879 s      18493 s          0 s
       #2  2593 MHz      11208 s          1 s       2089 s      38427 s          0 s
       
  Memory: 6.7694854736328125 GB (3236.45703125 MB free)
  Uptime: 523.0 sec
  Load Avg:  1.0  0.88623046875  0.4970703125
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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1040-azure #47-Ubuntu SMP Thu Jun 1 19:38:24 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      41967 s          1 s       2185 s      22173 s          0 s
       #2  2593 MHz      14997 s          1 s       2507 s      48673 s          0 s
       
  Memory: 6.7694854736328125 GB (3289.3046875 MB free)
  Uptime: 669.0 sec
  Load Avg:  1.0224609375  0.94873046875  0.58056640625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 30 Jun 2023 - 1:34
* Package commit: 03591f
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
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                      |  11.311 ns (5%) |           |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                       | 506.413 μs (5%) |           |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                                 |  11.311 ns (5%) |           |                 |             |
| `["collectors", :(:comp => "filter"), :(:impl => "base")]`                                  |  38.601 μs (5%) |           | 128.66 KiB (1%) |          14 |
| `["collectors", :(:comp => "filter"), :(:impl => "coll")]`                                  |  46.801 μs (5%) |           | 284.81 KiB (1%) |        5012 |
| `["collectors", :(:comp => "filter"), :(:impl => "nonexpanding")]`                          |  46.501 μs (5%) |           | 312.75 KiB (1%) |        5005 |
| `["collectors", :(:comp => "filter"), :(:impl => "vec")]`                                   |  40.701 μs (5%) |           | 128.59 KiB (1%) |          13 |
| `["collectors", :(:comp => "map"), :(:impl => "coll")]`                                     |   8.200 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "man")]`                                      |   8.000 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "safe_coll")]`                                |  11.400 μs (5%) |           |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "vec")]`                                      |  70.602 μs (5%) |           | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                             | 508.446 ms (5%) | 76.804 ms | 804.14 MiB (1%) |     4024332 |
| `["dataframes", "Int-Int"]`                                                                 |   1.326 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                             |   1.687 ms (5%) |           | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                          |   1.733 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                           |   1.658 ms (5%) |           | 160.27 KiB (1%) |       10252 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :empty)]`     |  44.101 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :equal)]`     |  24.500 μs (5%) |           |                 |             |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :half)]`      |  39.801 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :+), :(:desttype => :widen), :(:destkeys => :empty)]`          |  42.200 μs (5%) |           |  92.31 KiB (1%) |          18 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :empty)]` |  42.201 μs (5%) |           |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :equal)]` |  21.600 μs (5%) |           |                 |             |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :half)]`  |  37.901 μs (5%) |           |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :right), :(:desttype => :widen), :(:destkeys => :empty)]`      |  42.201 μs (5%) |           |  92.31 KiB (1%) |          18 |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1040-azure #47-Ubuntu SMP Thu Jun 1 19:38:24 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      31469 s          1 s       1879 s      18493 s          0 s
       #2  2593 MHz      11208 s          1 s       2089 s      38427 s          0 s
       
  Memory: 6.7694854736328125 GB (3236.45703125 MB free)
  Uptime: 523.0 sec
  Load Avg:  1.0  0.88623046875  0.4970703125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-8.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/BangBang.jl/BangBang.jl*

## Job Properties
* Time of benchmark: 30 Jun 2023 - 1:36
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

| ID                                                                                          | time            | GC time    | memory          | allocations |
|---------------------------------------------------------------------------------------------|----------------:|-----------:|----------------:|------------:|
| `["append", "append!!(::SVector, ::SingletonVector)"]`                                      |  11.712 ns (5%) |            |                 |             |
| `["append", "append!!(::Vector, ::SingletonVector)"]`                                       | 508.805 μs (5%) |            |                 |             |
| `["append", "append!!(Empty(SVector), ::SingletonVector)"]`                                 |  11.712 ns (5%) |            |                 |             |
| `["collectors", :(:comp => "filter"), :(:impl => "base")]`                                  |  39.801 μs (5%) |            | 128.66 KiB (1%) |          14 |
| `["collectors", :(:comp => "filter"), :(:impl => "coll")]`                                  |  51.501 μs (5%) |            | 284.81 KiB (1%) |        5012 |
| `["collectors", :(:comp => "filter"), :(:impl => "nonexpanding")]`                          |  41.001 μs (5%) |            | 312.75 KiB (1%) |        5005 |
| `["collectors", :(:comp => "filter"), :(:impl => "vec")]`                                   |  38.201 μs (5%) |            | 128.59 KiB (1%) |          13 |
| `["collectors", :(:comp => "map"), :(:impl => "coll")]`                                     |   9.901 μs (5%) |            |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "man")]`                                      |   9.300 μs (5%) |            |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "safe_coll")]`                                |  10.300 μs (5%) |            |  78.20 KiB (1%) |           2 |
| `["collectors", :(:comp => "map"), :(:impl => "vec")]`                                      |  74.701 μs (5%) |            | 256.64 KiB (1%) |          14 |
| `["dataframes", "Categorical"]`                                                             | 684.756 ms (5%) | 115.721 ms | 909.14 MiB (1%) |     5335052 |
| `["dataframes", "Int-Int"]`                                                                 |   1.232 ms (5%) |            | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-Int"]`                                                             |   1.644 ms (5%) |            | 160.23 KiB (1%) |       10251 |
| `["dataframes", "Missing-String"]`                                                          |   1.610 ms (5%) |            | 160.27 KiB (1%) |       10252 |
| `["dataframes", "String-String"]`                                                           |   1.692 ms (5%) |            | 160.27 KiB (1%) |       10252 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :empty)]`     |  38.801 μs (5%) |            |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :equal)]`     |  21.800 μs (5%) |            |                 |             |
| `["mergewith", :(:combine => :+), :(:desttype => :compatible), :(:destkeys => :half)]`      |  38.001 μs (5%) |            |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :+), :(:desttype => :widen), :(:destkeys => :empty)]`          |  44.101 μs (5%) |            |  92.31 KiB (1%) |          18 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :empty)]` |  37.400 μs (5%) |            |  91.72 KiB (1%) |          14 |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :equal)]` |  18.800 μs (5%) |            |                 |             |
| `["mergewith", :(:combine => :right), :(:desttype => :compatible), :(:destkeys => :half)]`  |  34.300 μs (5%) |            |  68.34 KiB (1%) |           5 |
| `["mergewith", :(:combine => :right), :(:desttype => :widen), :(:destkeys => :empty)]`      |  36.501 μs (5%) |            |  92.31 KiB (1%) |          18 |

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
      Ubuntu 22.04.2 LTS
  uname: Linux 5.15.0-1040-azure #47-Ubuntu SMP Thu Jun 1 19:38:24 UTC 2023 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2593 MHz      41967 s          1 s       2185 s      22173 s          0 s
       #2  2593 MHz      14997 s          1 s       2507 s      48673 s          0 s
       
  Memory: 6.7694854736328125 GB (3289.3046875 MB free)
  Uptime: 669.0 sec
  Load Avg:  1.0224609375  0.94873046875  0.58056640625
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
    Address sizes:                   46 bits physical, 48 bits virtual
    Byte Order:                      Little Endian
    CPU(s):                          2
    On-line CPU(s) list:             0,1
    Vendor ID:                       GenuineIntel
    Model name:                      Intel(R) Xeon(R) Platinum 8272CL CPU @ 2.60GHz
    CPU family:                      6
    Model:                           85
    Thread(s) per core:              1
    Core(s) per socket:              2
    Socket(s):                       1
    Stepping:                        7
    BogoMIPS:                        5187.81
    Flags:                           fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    Hypervisor vendor:               Microsoft
    Virtualization type:             full
    L1d cache:                       64 KiB (2 instances)
    L1i cache:                       64 KiB (2 instances)
    L2 cache:                        2 MiB (2 instances)
    L3 cache:                        35.8 MiB (1 instance)
    NUMA node(s):                    1
    NUMA node0 CPU(s):               0,1
    Vulnerability Itlb multihit:     KVM: Mitigation: VMX unsupported
    Vulnerability L1tf:              Mitigation; PTE Inversion
    Vulnerability Mds:               Mitigation; Clear CPU buffers; SMT Host state unknown
    Vulnerability Meltdown:          Mitigation; PTI
    Vulnerability Mmio stale data:   Vulnerable: Clear CPU buffers attempted, no microcode; SMT Host state unknown
    Vulnerability Retbleed:          Vulnerable
    Vulnerability Spec store bypass: Vulnerable
    Vulnerability Spectre v1:        Mitigation; usercopy/swapgs barriers and __user pointer sanitization
    Vulnerability Spectre v2:        Mitigation; Retpolines, STIBP disabled, RSB filling, PBRSB-eIBRS Not affected
    Vulnerability Srbds:             Not affected
    Vulnerability Tsx async abort:   Mitigation; Clear CPU buffers; SMT Host state unknown
    

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

