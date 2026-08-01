# MANIFEST

Catatan build artefak .ex5 di repo ini.

| Item | Nilai |
|---|---|
| Waktu build | `2026-08-01 23:48:27 +07:00` |
| Source repo | https://github.com/handi425/TVC.git |
| Source commit | `62bebdedf24b44293d9fce3cacba978ba4202c9d` (main) |
| Compiler | MetaEditor64.exe `5.0.0.6090` |
| Terminal | terminal64.exe `5.0.0.6090` |
| Hasil compile | 11/11 file, **0 errors** |

Semua source `.mq5` dalam keadaan bersih (tanpa modifikasi lokal) pada commit di atas.

## Checksum SHA256

| File | Bytes | SHA256 |
|---|---:|---|
| `Experts/EntryAjaib.ex5` | 136014 | `e8afd172d1742d890869577b7dedadc6992e7721317c0068a6ee56b54cf77fa8` |
| `Experts/EntryAjaibLite.ex5` | 97524 | `ab73ae0f05ccd380119623c413389bdd20e1df195f100bad66841d0dcec2ae5d` |
| `Experts/HarmonicTelegramScannerEA.ex5` | 123758 | `a1e1f968ecc92d725e3f031995788c94fcbb628381d069abe669929894205d4e` |
| `Indicators/Candle Time.ex5` | 13620 | `f3b1d0e7c0874748de2e09492c409d491ed1640d20fa20d1874ccc1fdf92d8db` |
| `Indicators/EAL_MA3.ex5` | 20742 | `c5dc14dda37dc1d6b8313254c756039a1256b75ae93ac890017e7637c9822d94` |
| `Indicators/FiboZone_Pro.ex5` | 40322 | `d0030ded2e533248ca6ab6ea7160f1b16e1b8fa0e4c9126b65c3d159a63abb77` |
| `Indicators/MA Ribbon.ex5` | 24534 | `e7fcffcb9980afdd0be20b917a1aa433e37ed2884125475bf56f017eba8e55c5` |
| `Indicators/Manual Harmonic Patterns TP SL.ex5` | 57242 | `8a5f557fdbfbad47bdfec846f90d3661262949a8e2ad1295d74844450e62791c` |
| `Indicators/RSI Divergence.ex5` | 32072 | `cf907e19de3478b4d33c2705ad5ecf17d3bd244ba041928b8234f1e6926dc169` |
| `Indicators/Stochastic_Divergence.ex5` | 29846 | `816469a8bac739f4f298295a0696194a5f6f4dd03e897e2e1739c0f1908eac7e` |
| `Indicators/TVC Volume Pro.ex5` | 32812 | `11a4e770574e6bf6a0d5be319ae3ac91eb87d536381deebffe9532eeb558614d` |

## Peringatan compiler

`EntryAjaibLite.mq5` menghasilkan 2 warning (non-blocking):

```
EntryAjaibLite.mq5(1727,4) : warning 83: return value of 'OrderCalcProfit' should be checked
EntryAjaibLite.mq5(1728,4) : warning 83: return value of 'OrderCalcProfit' should be checked
```

File lain: 0 errors, 0 warnings.

## Dependency eksternal

`HarmonicTelegramScannerEA.mq5` meng-include `..\Indicators\HarmonicFinder\HPFMatcher.mqh`
beserta 13 `.mqh` HarmonicFinder lain. **File-file ini tidak ada di repo source TVC** —
diambil dari data folder MT5 saat build:

```
%APPDATA%\MetaQuotes\Terminal\94C2289E5A5E455C2C90A42B6584638F\MQL5\Indicators\HarmonicFinder\
```

Selama `.mqh` tersebut belum di-commit ke repo TVC, build EA ini **tidak reproducible**
di mesin lain.

