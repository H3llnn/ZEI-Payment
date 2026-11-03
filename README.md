<div align="center">

# ZΞI Payment

### Pembayaran masuk. Akses terbuka.

Runtime penjualan akses untuk ekosistem **ZΞI Project**.

![Python](https://img.shields.io/badge/Python-3.12%2B-8B5CF6?style=flat-square)
[![GPL-3.0](https://img.shields.io/badge/License-GPL--3.0-22D3EE?style=flat-square)](LICENSE)

[Gate](https://github.com/H3llnn/ZEI-Gate) · [ForceSubs](https://github.com/H3llnn/ZEI-ForceSubs) · [Userbot](https://github.com/H3llnn/ZEI-Userbot)

</div>

## Yang ditangani runtime ini

- QRIS langsung di chat dan pemeriksaan pembayaran.
- Penjualan akses satuan dan gabungan dengan harga sendiri.
- Pesanan, riwayat pembelian berhasil, dan notifikasi owner.
- Link undangan per tujuan, sekali pakai hingga digunakan.
- Pengaturan akses, foto, deskripsi, admin, dan broadcast.
- Integrasi Saweria sederhana serta webhook opsional untuk instalasi yang membutuhkannya.

| Modul | Tugas |
| :--- | :--- |
| `payment_ui.py` | Pengaturan dan alur pembeli |
| `payment_store.py` | Pesanan dan akses melalui database Gate |
| `payment_service.py` | Verifikasi, pengiriman akses, dan cleanup |
| `saweria.py` | Integrasi penyedia pembayaran |
| `payment_webhook.py` | Endpoint webhook opsional |

## Memasang

Letakkan **ZEI-Gate**, **ZEI-ForceSubs**, **ZEI-Payment**, dan **ZEI-Userbot** berdampingan. Jalankan `python install.py` dari Gate. Buat bot Payment melalui bot induk, lalu atur melalui `/setting` bot anak.

Ini paket runtime, bukan bot induk kedua. Store, token, izin, dan enkripsi dikelola Gate. ForceSubs tetap menjadi dependensi untuk melayani link konten lama pada bot hasil migrasi. Mode sederhana menggunakan username Saweria; HTTPS Mini App adalah kebutuhan terpisah dari webhook pembayaran.

## Pengujian dan pembaruan

CI menjalankan tes integrasi Gate dengan seluruh runtime terpasang. Tes otomatis menggunakan pembayaran tiruan. Lakukan uji pembayaran dan bergabung nyata sebelum membuka penjualan setelah deployment.

[Struktur empat repo](https://github.com/H3llnn/ZEI-Gate/blob/main/docs/RUNTIME-SPLIT.md) · [Panduan update](https://github.com/H3llnn/ZEI-Gate/blob/main/docs/UPDATE-GUIDE.md)

## Lisensi

GPL-3.0. Kode diekstrak dari ZEI-Gate; riwayat sumber sebelumnya tersedia di repo Gate. Lisensi dan atribusi sumber tetap dipertahankan dalam [LICENSE](LICENSE) dan [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

**ZΞI PROJECT** · Maintained by **Zeisss**
