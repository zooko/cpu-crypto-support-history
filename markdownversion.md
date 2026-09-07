**✓** = this change added, or substantially improved, support in that column. **Blank** = nothing new for that column in that change (support may already have existed). Blank-year rows are just the calendar passing. Click a note number for detail, or ignore them entirely.

| Year | Arch | Note | SIMD | SHA-256 | SHA-3 | SHA-512 | AES | SM3/SM4 |
|:----:|:----:|:----:|:----:|:-------:|:-----:|:-------:|:---:|:-------:|
| 2010 | x86  | [^1^]  |   |   |   |   | ✓ |   |
| 2011 | Arm  | [^2^]  |   | ✓ |   |   | ✓ |   |
| 2012 |      |       |   |   |   |   |   |   |
| 2013 | x86  | [^3]  | ✓ |   |   |   |   |   |
|      | x86  | [^4]  |   | ✓ |   |   |   |   |
|      | Arm  | [^3^]  |   | ✓ |   |   | ✓ |   |
| 2014 |      |       |   |   |   |   |   |   |
| 2015 |      |       |   |   |   |   |   |   |
| 2016 | x86  | [^6]  |   | ✓ |   |   |   |   |
|      | x86  | [^7]  | ✓ |   |   |   |   |   |
|      | Arm  | [^8]  |   |   | ✓ | ✓ |   | ✓ |
|      | Arm  | [^9]  | ✓ |   |   |   |   |   |
| 2017 | x86  | [^4^] | ✓ |   |   |   |   |   |
|      | x86  | [^11] |   | ✓ |   |   |   |   |
| 2018 |      |       |   |   |   |   |   |   |
| 2019 | x86  | [^12] | ✓ | ✓ |   |   | ✓ |   |
|      | x86  | [^13] | ✓ |   |   |   |   |   |
|      | Arm  | [^14] |   |   | ✓ |   | ✓ | ✓ |
| 2020 | Arm  | [^5^] | ✓ |   |   |   |   |   |
| 2021 |      |       |   |   |   |   |   |   |
| 2022 | x86  | [^16] | ✓ |   |   |   |   |   |
| 2023 |      |       |   |   |   |   |   |   |
| 2024 | x86  | [^17] | ✓ |   |   |   |   |   |
|      | x86  | [^6^] |   |   |   | ✓ |   | ✓ |

*Selected milestones, 2010–2024. "SIMD ✓" ≈ a doubling of vector width or vector execution width, or a new scalable-vector architecture. Specifications may describe optional features and precede hardware by years. Vendor and product names are in the notes.*

[^1]: **Intel Westmere** — AES-NI (and PCLMULQDQ) shipped. First x86 algorithm-specific crypto instructions.
[^2]: **Arm — Armv8-A specified**, with an optional crypto extension: SHA-1, SHA-256, AES, polynomial multiply, all on 128-bit NEON registers. No hardware yet.
[^7^]: **Intel Haswell** — AVX2: integer SIMD widened 128 → 256 bits. Also BMI2 (`RORX`), handy for scalar ARX code.
[^8^]: **Intel — SHA Extensions specified** (SHA-1, SHA-256): `SHA256RNDS2`, `SHA256MSG1`, `SHA256MSG2` on 128-bit XMM registers. One hash per register set, not four lanes. No hardware yet.
[^3^]: **Apple A7** — first widely shipped Armv8-A CPU with the crypto extension (SHA-256, SHA-1, AES).
[^9^]: **Intel Goldmont (Apollo Lake)** — first hardware with SHA Extensions. An Atom-class part, not Core; mainstream Core CPUs would wait until 2019.
[^7]: **Intel Knights Landing (Xeon Phi)** — AVX-512F: 512-bit vectors, 32 vector registers, packed 32-bit rotates, ternary logic.
[^8]: **Arm — Armv8.2-A crypto additions specified**: SHA-512, SHA-3/Keccak helpers, SM3, SM4. No new SHA-256 operations.
[^10^]: **Arm — SVE announced**: scalable vectors, 128–2048 bits per implementation. No crypto-specific operations.
[^4^]: **Intel Skylake-SP / -X / -W** — AVX-512 reaches Xeon and HEDT. Note the gap: neither client Skylake (2015) nor these server parts had SHA Extensions, while the cheaper Goldmont parts did.
[^11^]: **AMD Zen** — first AMD implementation of SHA Extensions. Vector execution was 128 bits wide.
[^12^]: **Intel Ice Lake** — first Core CPU with both AVX-512 and SHA Extensions; VAES / VPCLMULQDQ / GFNI widen AES-family work to 512 bits. SHA-256 instructions stay 128-bit.
[^13]: **AMD Zen 2** — vector execution datapaths widened 128 → 256 bits. No AVX-512.
[^14]: **Arm — SVE2 announced (2019), Armv9-A (2021)**: optional scalable-vector AES, SHA-3 and SM4 operations. No scalable-vector SHA-256.
[^5^]: **Fujitsu A64FX** — first widely deployed 512-bit SVE hardware (Fugaku).
[^16]: **AMD Zen 4** — AVX-512 ISA (32 registers, rotates, ternary logic) executed on 256-bit datapaths.
[^17]: **AMD Zen 5 (desktop/server)** — vector execution datapaths widened 256 → 512 bits. Mobile variants are narrower.
[^6^]: **Intel Lunar Lake / Arrow Lake** — SHA-512, SM3, SM4 instructions. No new SHA-256 instructions; no AVX-512 exposed.

*(If your renderer lacks footnote support, the `[^n]` markers still read as plain note numbers.)*
