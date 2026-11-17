# AI Project Risk Monitoring — PMO Risk Dashboard

Versi HTML-1.2-Handover, direvisi 6 November 2026. File utama **Dashboard_PMO_HTML.html**. Nama proyek: **AI Project Risk Monitoring**; deskripsi dashboard: **PMO Risk Dashboard**. Branding lama diganti; draft review versi sebelumnya tetap dapat dibaca pada browser yang sama.

## Mulai langsung

1. Unduh file HTML ke perangkat. Jika tampilan Library hanya menunjukkan kode/preview statis, gunakan Download.
2. Buka file yang sudah diunduh dengan Chrome, Edge atau Firefox modern.
3. Gunakan menu di sebelah kiri; pada layar kecil menu berada di atas.

Tidak perlu aplikasi BI, Python, akun Microsoft, server, koneksi Drive, atau memasang library untuk melihat dashboard. CSS, JavaScript dan data demo tertanam dalam satu file. Tautan sumber hanya membuka situs bila diklik. Tidak ada pengambilan data otomatis dari internet.

## Lima halaman

- **Risk Monitoring:** awalnya menampilkan 56 prioritas dari 277 proyek valid. Cari Project ID, ubah kelompok, rentang skor dan urutan. Klik Project ID untuk detail. Ekspor CSV mengekspor seluruh hasil filter, bukan hanya 15 baris halaman tabel.
- **Project Delivery:** baseline 28 pekerjaan, status snapshot Jira terverifikasi sampai Tahap 8 pada 6 November 2026, jam rencana dan finansial simulasi. Filter tahap/status dan pencarian pekerjaan tersedia. Status In Review bukan Done atau persentase progres.
- **Model Evaluation:** perbandingan test historis dan kapasitas 10/20/30%. Tombol sensitivitas tidak mengubah kapasitas 20% yang diterapkan pada risk inbox.
- **Governance & QA:** 16 catatan RAID terkini, empat gate dan alasan input ditolak. Filter Risk/Issue/Assumption/Dependency. Catatan RAID tidak diubah oleh formulir review.
- **Review Queue:** 56 draft antrean. Isi owner, status, tanggal review dan catatan bukti bila Anda benar-benar melakukan review. Simpan di browser atau ekspor CSV.

G01 HOLD dan label simulasi tetap terlihat. Skor disajikan sebagai angka 0–1, bukan probabilitas perusahaan nyata yang telah terbukti. Ranking diurutkan menurut skor menurun lalu ID menaik; prioritas diambil sebanyak ceil(20% × seluruh proyek valid) sebelum filter.

## Memasukkan hasil batch lain

Pada Risk Monitoring, pilih **Impor predictions.csv** dari hasil notebook Tahap 6. Kolom wajib untuk tampilan adalah Project_ID dan Risk_Score; kolom budget/durasi/CPI ikut ditampilkan jika tersedia. Header dan angka mengikuti CSV dari notebook (pemisah koma, desimal titik).

Dashboard menolak ID kosong/ganda dan skor kosong/tidak finite/di luar 0–1. Semua baris dengan ID ganda ditolak. Maksimum file 5 MB. Ranking 20% dihitung ulang dari skor valid. Impor tidak menjalankan training atau model di JavaScript; data mentah harus diproses melalui notebook terlebih dahulu. Tidak ada upload ke server.

Setelah impor, outcome ditandai belum diketahui. Halaman evaluasi tetap hasil test historis Tahap 5; tidak dihitung sebagai precision/recall baru. **Pulihkan data file ini** mengembalikan seed data pada file HTML tersebut. Jika CSV rusak/seluruh baris invalid, data sebelumnya dipertahankan.

## Catatan review

“Sedang direview” membutuhkan owner. “Review selesai” membutuhkan owner, tanggal dan catatan bukti. Nilai awal kosong; dashboard tidak membuat persetujuan atau tindakan selesai sendiri.

Draft disimpan melalui localStorage di browser/perangkat yang sama, dipisahkan menurut identitas dataset. Perilaku penyimpanan file lokal dapat berbeda antarbrowser; jika penyimpanan ditolak, pesan error ditampilkan dan ekspor CSV tetap dapat digunakan. Ekspor CSV sebagai cadangan sebelum pindah perangkat atau membersihkan data browser. Tidak ada sinkronisasi otomatis ke Jira/RAID.

**Cetak/PDF** mencetak halaman aktif beserta baris tabel yang sedang tampil. Gunakan ekspor CSV untuk seluruh hasil filter.

## Bila ingin menjalankan batch sendiri

Buka **Colab_Batch_ke_HTML.ipynb**, jalankan satu sel, lalu pilih ZIP HASIL Tahap 5 yang sudah Anda miliki. Tidak perlu script/protokol tambahan. CSV input batch opsional mengikuti template pada paket. Notebook menghasilkan ZIP berisi hasil prediksi, error, draft queue dan Dashboard_PMO_HTML.html dengan data terbaru.

Jika versi model berbeda, pilihan RF depth 4 direproduksi pada train saja dengan parameter terkunci; mode dan perbedaan versi dicatat, tanpa tuning pada test. Template dashboard dan data PMO dibawa notebook. Angka finansial/RAID tetap snapshot sumber, bukan live sync.

## Dasar data dan batas kualitas

Demo: 280 input termasuk tiga fixture QA invalid, 277 valid, 56 prioritas. Pada test historis, 44 dari 188 kasus terlambat tertangkap; 144 masih terlewat. Keunggulan atas aturan CPI (39 kasus) belum konklusif. Model terbatas pada proyek IT pada akhir bulan kedua. G01 tetap HOLD karena as-of/frozen baseline belum terbukti.

Budget sumber proyek adalah USD. Budget pembangunan adalah IDR, skenario Base per 27 Januari 2027. Tidak digabung. Perubahan alat visualisasi belum direbaseline dalam estimasi lama; tidak dianggap nol usaha.

## Bukti pengujian

21 pemeriksaan interaksi lulus pada eksekusi HTML melalui JSDOM, termasuk konsistensi nama, script, data/count, navigasi, pagination, filter/search/empty-state, detail, sensitivitas, RAID, review validation/persistence/migrasi data lama, parser/import/CSV, escaping dan dependency eksternal. Native render/browser visual belum diverifikasi: layanan preview browser lingkungan ini tidak tersedia. Tidak menggunakan screenshot tiruan sebagai bukti browser.

Notebook juga diuji penuh dengan fungsi unggah/unduh Colab disimulasikan. Bukti ada pada verification.json dan notebook_verification.json. Uji tersebut tidak menyatakan Naufal sudah menjalankan notebook, tidak menjadi business UAT/sign-off, dan tidak mengubah G01 menjadi lolos.

Referensi File API: https://developer.mozilla.org/en-US/docs/Web/API/File_API/Using_files_from_web_applications . Sumber dataset: Reyhane Hajihoseyni (2026), Mendeley Data v1, DOI 10.17632/2p5sz57wh2.1, CC BY 4.0; data ditransformasi menjadi snapshot dan hasil eksperimen. Tidak ada endorsement sumber.

## Pembaruan handover

Versi paket ini memperbarui snapshot Jira, RAID dan gate berdasarkan hasil aktual Tahap 8. Snapshot awal 13 catatan tetap disimpan di workbook. D03 menyimpan kendala repository GitHub sampai bukti unggah tersedia. Tabel delivery bukan koneksi live. Skor, model, kapasitas dan finansial tidak diubah.
