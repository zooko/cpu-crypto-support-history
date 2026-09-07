**Selected major milestones.** ✓ = added/widened support, or first implementation in that CPU family. — = no new support in that change. SHA-3 includes Keccak-specific helpers.

| Year | Improvement (architecture) | Substantially improved SIMD? | SHA-256 | SHA-512 | SHA-3 | AES | SM3 | SM4 |
|---|---|---|:---:|:---:|:---:|:---:|:---:|:---:|
| 2010 | Westmere AES-NI shipped (x86) | — | — | — | — | ✓ | — | — |
| 2011 / 2013 | Armv8-A specified / Apple A7 shipped (ARM) | — | ✓ | — | — | ✓ | — | — |
| 2013 | Haswell AVX2 shipped (x86) | **128→256-bit integer SIMD** | — | — | — | — | — | — |
| 2013 / 2016 / 2017 | SHA Extensions specified / Intel Goldmont / AMD Zen shipped (x86) | — | ✓ | — | — | — | — | — |
| 2016–2017 | AVX-512: Knights Landing / Skylake Xeon shipped (x86) | **256→512 bits; 16→32 vector registers** | — | — | — | — | — | — |
| 2016 | Armv8.2-A crypto extensions specified (ARM) | — | — | ✓ | ✓ | — | ✓ | ✓ |
| 2016 / 2020 | SVE announced / A64FX systems shipped (ARM) | **Scalable vectors; A64FX implements 512 bits** | — | — | — | — | — | — |
| 2019 | Ice Lake shipped: AVX-512, SHA, VAES (x86) | **512-bit SIMD in this Core generation** | ✓ | — | — | ✓ | — | — |
| 2019 | Zen 2 shipped (x86) | **128→256-bit execution datapaths** | — | — | — | — | — | — |
| 2019–2021 | SVE2 / Armv9 scalable-vector crypto specified (ARM) | No width increase over SVE | — | — | ✓ | ✓ | — | ✓ |
| 2022 | Zen 4 AVX-512 shipped (x86) | **512-bit ISA; 32 registers**, but 256-bit execution | — | — | — | — | — | — |
| 2024 | Full-width Zen 5 shipped, desktop/server (x86) | **256→512-bit execution datapaths** | — | — | — | — | — | — |
| 2024 | Lunar Lake / Arrow Lake crypto additions shipped (x86) | — | — | ✓ | — | — | ✓ | ✓ |

*Specifications do not imply immediate hardware availability; ARM crypto extensions can be optional. “No new support” does not rule out faster execution of existing instructions. Selected timeline ends in 2024.*
