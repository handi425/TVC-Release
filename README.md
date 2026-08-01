# TVC-Compiled

Repository distribusi **binary saja** untuk EA dan Indicator TVC.
Hanya berisi file `.ex5` hasil compile — tidak ada source `.mq5`/`.mqh` di sini.

Source code ada di repo terpisah: <https://github.com/handi425/TVC.git>

## Isi

### Experts/ → salin ke `MQL5\Experts\`

| File | Keterangan |
|---|---|
| `EntryAjaib.ex5` | Panel entry manual multi-layer (grid + martingale, trailing, basket TP) |
| `EntryAjaibLite.ex5` | Versi ringkas untuk backtest manual (Visual Mode) |
| `HarmonicTelegramScannerEA.ex5` | Scanner harmonic pattern + notifikasi Telegram |

### Indicators/ → salin ke `MQL5\Indicators\`

| File | Keterangan |
|---|---|
| `EAL_MA3.ex5` | 3 Moving Average berwarna, pendamping EntryAjaibLite |
| `Candle Time.ex5` | Hitung mundur waktu candle |
| `FiboZone_Pro.ex5` | Fibonacci zone + order block |
| `MA Ribbon.ex5` | Ribbon multi-MA |
| `Manual Harmonic Patterns TP SL.ex5` | Harmonic pattern manual dengan TP/SL |
| `RSI Divergence.ex5` | Deteksi divergence RSI |
| `Stochastic_Divergence.ex5` | Deteksi divergence Stochastic |
| `TVC Volume Pro.ex5` | Analisis volume |

## Cara pasang

1. Di MT5: **File → Open Data Folder**
2. Masuk ke folder `MQL5`
3. Salin isi `Experts/` ke `MQL5\Experts\`, dan isi `Indicators/` ke `MQL5\Indicators\`
4. Di MT5 tekan **Ctrl+M** (Navigator) → klik kanan → **Refresh**

Tidak perlu compile ulang. File `.ex5` langsung jalan.

> **Catatan:** `.ex5` MT5 tidak portabel lintas build terminal yang terlalu jauh.
> Kalau MT5 Anda jauh lebih baru dari build compiler di [MANIFEST.md](MANIFEST.md),
> compile ulang dari source.

## Verifikasi integritas

Checksum SHA256 setiap file tercatat di [MANIFEST.md](MANIFEST.md), lengkap dengan
commit source yang dipakai saat build.

```powershell
Get-FileHash .\Experts\EntryAjaib.ex5 -Algorithm SHA256
```

## Build ulang

Repo ini tidak punya toolchain sendiri — ia murni artefak. Untuk regenerasi,
compile source dari repo TVC dengan MetaEditor:

```powershell
& "<path>\MetaEditor64.exe" /compile:"<file>.mq5" /inc:"<DataFolder>\MQL5" /log:"build.log"
```

`/inc:` harus menunjuk ke root `MQL5`, **bukan** ke `MQL5\Include`
(MetaEditor menambahkan `Include\` sendiri).
