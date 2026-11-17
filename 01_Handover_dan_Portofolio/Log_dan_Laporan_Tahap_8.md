# Laporan dan log pekerjaan Tahap 8

AI Project Risk Monitoring · PMO Risk Dashboard · 6 November 2026

Laporan kepada Naufal tentang pekerjaan AI. Ini bukan RAID, timesheet, bukti rapat atau penerimaan sponsor.

## Hasil dan status

Paket handover, studi kasus portofolio, materi CV dan interview, runbook, checklist penerimaan, sumber dan hasil historis telah disiapkan. Dokumen inti, dashboard, notebook dan governance tersimpan di Google Drive pada folder proyek yang dibuat untuk tugas ini. Tautan berkas yang diobservasi tersimpan pada indeks Drive dalam paket. Arsip lengkap berhasil diunggah ke Google Drive. Tautan arsip: https://drive.google.com/file/d/1Yp-cu0u76EMkL9NQ32rB0J1BXFO4wR7x/view?usp=drivesdk

Unggah GitHub belum berhasil. Akun naufalzulfikarchandra-cmd terhubung, tetapi daftar repository yang tersedia kosong. Koneksi yang tersedia dapat mengisi repository namun tidak menyediakan pembuatan repository baru. Pemeriksaan jalur browser mencapai login GitHub. User memilih Google melalui formulir login aman, kemudian situs menampilkan Something went wrong. Tidak ada repository, branch atau commit baru yang diklaim. Tidak ada credential yang dibaca atau dimasukkan ke paket.

Tahap 8 secara keseluruhan belum dapat ditutup karena distribusi GitHub dan penerimaan owner masih terbuka. KAN-36, KAN-37 dan KAN-39 berada di In Review. KAN-38 berada di In Progress dengan kendala repository. Seluruh 28 task memiliki 27 In Review dan 1 In Progress pada snapshot setelah perubahan; tidak ada task Done dan angka itu bukan persentase penyelesaian.

## Keluaran yang disusun

| Work package | Keluaran | Status |
|---|---|---|
| T25 KAN-36 | Struktur paket, README, handover, runbook dan checklist | Disusun untuk review owner |
| T26 KAN-37 | Studi kasus dengan masalah, keputusan, kontribusi, hasil dan gap | Disusun untuk review owner |
| T27 KAN-38 | Sumber, notebook, data, hasil, model dan petunjuk reproduksi | Paket siap, distribusi GitHub belum selesai |
| T28 KAN-39 | Poin CV Indonesia dan Inggris, narasi pembuka, demo lima menit dan FAQ | Disusun untuk review dan latihan owner |

Materi menyatakan proyek independen sintetis dan bantuan AI. Tidak membuat jabatan, pengalaman kerja perusahaan, deployment produksi, penghematan biaya atau penurunan keterlambatan yang belum diukur. Tidak mempublikasikan website, mengubah izin berbagi Drive atau memilih lisensi software baru atas nama owner.

## Pembaruan RAID

Workbook mempertahankan empat sheet sumber RAID, Risk_Register, Control_Gates dan Traceability secara semantik, beserta nilai dan formula sebelum perubahan. Overview mendapat penunjuk ke pembaruan terkini tanpa mengganti ringkasan snapshot lama.

Tiga sheet ditambahkan untuk kebutuhan pembaruan: Current_RAID berisi 16 catatan, Gate_Updates berisi empat gate, dan Change_Log berisi sembilan event aktual yang diketahui. Current_RAID memperbarui status 13 catatan awal serta menambahkan I05 untuk gap UAT, I06 untuk forecast belum direkonsiliasi, dan D03 untuk repository tujuan GitHub. Tidak membuat insiden perusahaan baru atau mengisi peristiwa masa depan. Skor inherent lama dan skor residual tidak diubah atau dianggap nol.

Dependency Power BI digantikan oleh keluaran HTML sesuai instruksi user. G01 tetap HOLD karena semantic as of dan freeze baseline belum terbukti. G02 belum disetujui, G03 belum diterima dan G04 menunggu penerimaan owner. Status unggah tidak dipakai sebagai bukti gate operasional lolos.

## Pembaruan dashboard dan notebook

Dashboard handover HTML-1.2 memperbarui snapshot Jira, RAID dan gate. Antarmuka menyebut status RAID terkini dan jumlahnya mengikuti data, sementara snapshot awal disimpan pada workbook. Notebook batch membawa metadata PMO yang sama. Skor, kapasitas 20%, data model, parameter training dan nilai finansial tidak berubah.

Demo tetap replay historis 277 proyek, 56 prioritas dan 44 kasus terlambat di dalam prioritas. Aturan CPI menangkap 39 pada jumlah yang sama. Keunggulan belum konklusif. Opsi B belum dieksekusi dan tidak ada training ulang atau audit generator baru dalam tugas handover ini. Jika pengguna menjalankan notebook pada environment berbeda, jalur reproduksi model untuk kompatibilitas tetap mengikuti engine lama dan dijelaskan pada runbook.

## Pemeriksaan yang dilakukan

- Dua puluh tiga pemeriksaan DOM interaksi lulus pada HTML handover, termasuk navigasi, filter, pencarian, impor ekspor, validasi review serta kesesuaian snapshot Jira dan 16 catatan RAID.
- Sumber training, protokol dan requirements dibandingkan dengan artefak Tahap 5 dan tidak berubah. Kode Python dalam paket diperiksa sintaksnya. Notebook tidak dieksekusi untuk melatih model pada Tahap 8.
- Pola credential yang diperiksa tidak ditemukan pada teks dan XML dokumen dalam paket. Pemeriksaan tersebut tidak diklaim sebagai security approval atau audit keamanan menyeluruh.
- Workbook dihitung ulang, diperiksa formula error dan dirender untuk menilai bagian yang berubah. Tidak ditemukan pola error formula yang dipindai. Snapshot asli dan sumber skor risiko tetap dipertahankan.
- Byte sumber dataset dan struktur arsip diperiksa terhadap hash yang tercatat. Indeks berkas dan manifest disertakan.
- Hasil unggah Drive diperiksa melalui metadata, termasuk identitas, jenis, ukuran dan folder tujuan. Tidak menganggap hasil pencarian kosong sebagai keberhasilan unggah.

Uji DOM tidak membuktikan native render browser Windows. Microsoft Excel, Word dan PowerPoint Windows tidak dibuka. Checklist UAT owner tetap belum dijalankan dan tidak diisi dengan hasil buatan.

## Tanggal dan anggaran

Tanggal penyusunan aktual adalah 6 November 2026. Baseline cerita SIM Tahap 8 tetap 10, 11, 12 dan 15 Februari 2027, masing masing tiga jam rencana. Itu tidak menjadi actual timesheet. Cutoff keuangan tetap 27 Januari 2027 dengan overrun Base Rp400.185 atau 2,03%. Dampak bersih perubahan alat dan usulan Opsi B belum direforecast. Tidak ada pembayaran atau pembelian baru.

## Langkah yang masih memerlukan owner

Untuk menyelesaikan distribusi GitHub, diperlukan repository tujuan pada akun yang terhubung. Owner dapat membuat repository bernama ai-project-risk-monitoring dengan README awal lalu memberikan URL. Setelah repository tersedia, sumber yang telah siap dapat diunggah melalui koneksi GitHub tanpa perlu melatih model lagi.

Owner juga perlu menjalankan checklist UAT, meninjau narasi portofolio dan CV, lalu mencatat penerimaan. Penyelesaian paket portofolio tetap terpisah dari keputusan kelayakan operasional model.
