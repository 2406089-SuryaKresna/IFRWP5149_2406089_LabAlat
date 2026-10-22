<!-- Use case deskripsi utama -->

 Elemen | Deskripsi |
|---|---|
| ID dan nama | **SIA-UC05 — Unduh bukti pengajuan KRS** |
| Sumber kebutuhan | SIA-R05 |
| Tujuan | Memberikan bukti pengajuan KRS yang telah tersimpan kepada mahasiswa yang memilih mengunduhnya. |
| Aktor utama | Mahasiswa |
| Aktor pendukung | Sistem Informasi Akademik |
| Pemicu | Pada konfirmasi pengajuan, mahasiswa memilih opsi unduh bukti. |
| Prasyarat | Pengajuan KRS berhasil tersimpan dan konfirmasi/bukti pengajuan tersedia. |
| Relasi | **«extend» SIA-UC03 — Ajukan KRS.** Arah panah pada diagram: SIA-UC05 → SIA-UC03. |
| Extension point | **Bukti pengajuan tersedia**, pada konfirmasi setelah pengajuan berhasil tersimpan. |
| Kondisi | **[mahasiswa memilih mengunduh bukti]** |
| Pascakondisi berhasil | Bukti pengajuan disiapkan dan tersedia untuk diunduh mahasiswa; pengajuan tetap berstatus menunggu persetujuan dosen wali. |
| Pascakondisi gagal | Pengajuan tetap tersimpan; sistem memberi tahu bahwa bukti tidak dapat disiapkan/diunduh. Kegagalan unduh tidak membatalkan pengajuan. |