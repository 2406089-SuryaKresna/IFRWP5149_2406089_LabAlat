<!-- Deskripsi Skenario -->

Sistem Informasi Akademik

Skenario tugas:
Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap
pengajuan menjalankan validasi KRS yang memeriksa kelengkapan,
prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil,
sistem menyimpan pengajuan berstatus menunggu persetujuan dosen
wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih
mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS
dan memberikan catatan keputusan.

<!-- ID Kebutuhan -->

|ID     |                             Kebutuhan tugas                             |
|-------|-------------------------------------------------------------------------|
|SIA-R01|                  Mahasiswa dapat melihat jadwal kuliah                  |
|SIA-R02|              Admin akademik dapat mengelola jadwal kuliah               |
|SIA-R03|                     Mahasiswa dapat mengajukan KRS                      |
|SIA-R04|             Sistem memvalidasi KRS sebagai bagian pengajuan             |
|SIA-R05|Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan|
|SIA-R06|        Dosen wali dapat memproses persetujuan atau penolakan KRS        |

<!-- Batas dan Asumsi -->

• Pengguna telah terautentikasi.

• Data mata kuliah, prasyarat, dan jadwal tersedia.

• Validasi gagal menyebabkan pengajuan belum berhasil tersimpan.

• Unduh bukti tidak menjadi syarat keberhasilan pengajuan.

• KRS tersimpan belum berarti disetujui.

• Pembayaran, pengisian nilai, dan implementasi basis data berada di luar
tugas.
<!-- Tabel Identifikasi akotr -->
|Aktor         |                            Tujuan_Terhadap_Sistem                            |
|--------------|------------------------------------------------------------------------------|
|Mahasiswa     |         Mengajukan KRS,Memilih mata kuliah,mengunduh bukti pengajuan         |
|Dosen_wali    |Memeriksa pengajuan KRS,Menyetujui atau menolak KRS,serta memberikan keputusan|
|Admin_Akademik|                Menambah,Mengubah,dan mengelola jadwal kuliah                 |

<!-- Susunan katalog uses case -->

|ID      |Nama_use_case         |     Peran_dalam_model     |
|--------|----------------------|---------------------------|
|SIA-UC03|Ajukan KRS            |  Fungsi utama mahasiswa   |
|SIA-UC04|Validasi KRS          | Perilaku yang disertakan  |
|SIA-UC05|Unduh bukti pengajuan | Tambahan bersyarat  UC03  |
|SIA-UC06|Proses persetujuan KRS|  Fungsi utama dosen wali  |
|SIA-UC07|Lihat jadwal kuliah   |  Fungsi utama mahasiswa   |
|SIA-UC08|Kelola jadwal kuliah  |Fungsi utama admin akademik|

<!-- include -->
SIA-UC05 <-include-> SIA-UC04
alasan: validasi wajib dilakukan setiap kali mahasiswa mengajukan KRS
<!-- Extend -->
SIA-UC05 <-Extend-> SIA-UC03
Extension point: unduk bukti pengajuan
alasan:Pengunduhan bukti hanya dilakukan mahasisawa memilih opsi unduh saat konfirmasi pengunduhan