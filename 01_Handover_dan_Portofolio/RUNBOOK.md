# Runbook penggunaan dan reproduksi

## Demo tanpa setup

Ekstrak paket lengkap. Buka dashboard/Dashboard_PMO_HTML.html di browser. Data demo tertanam. Kapasitas awal adalah 20% atau 56 prioritas dari 277 proyek. Tidak ada model yang dijalankan di JavaScript. Impor predictions.csv hanya membaca skor dari hasil batch.

## Batch di Google Colab

Unggah code/batch/Colab_Batch_ke_HTML.ipynb ke Colab. Jalankan satu sel kode. Ketika pemilih file muncul, pilih artifacts/HASIL_Colab_Tahap5.zip. CSV input batch bersifat opsional. Tanpa CSV tambahan, notebook memakai replay historis test yang sudah ada. Unduh ZIP keluaran, ekstrak lalu buka HTML.

Notebook memeriksa paket yang diperlukan dan memasang hanya dependensi yang belum tersedia. Tidak perlu memasang GPU atau layanan berbayar. Gunakan paket hasil model milik proyek ini. Mode pemuatan dan versi tercatat dalam model_trace.json. Pada runtime yang tidak cocok, engine mereproduksi model terpilih pada train asli dengan parameter terkunci, tanpa tuning pada test. Jadi menjalankan batch di environment lain dapat menjalankan fit untuk kompatibilitas. Hal tersebut tidak terjadi hanya dengan membuka dashboard.

## Menjalankan batch lokal

Lingkungan sumber yang diuji adalah Python 3.12 dengan versi paket di code/training/requirements.txt. Dari folder code/batch, panggil fungsi run_stage6 dengan path ZIP dan direktori hasil. Entry point yang disediakan dalam paket adalah notebook satu sel; tidak ada klaim bahwa batch_engine.py memiliki CLI sendiri.

CSV mentah memakai sembilan kolom yang dijelaskan dalam DATA_CONTRACT.md. Angka harus finite, budget positif, sektor IT, snapshot bulan 2, nilai kumulatif tidak menurun dan ID unik. Input invalid dipisahkan dengan alasan. Output harus memenuhi received = accepted + rejected. Pada replay yang direkam, 280 diterima sebagai input, 277 lolos dan 3 fixture QA ditolak.

## Reproduksi training historis

Langkah ini adalah cara mengulangi benchmark yang sudah ada, bukan instruksi melaksanakan usulan Opsi B. Jangan gunakan hasil test lama untuk tuning berulang.

```bash
python -m pip install -r code/training/requirements.txt
python code/training/train_stage5.py --source-dir data/source --output-dir reproduced_training
```

Kode membaca tiga file sumber yang disertakan, membangun snapshot, memakai split seed 20261104 dan menghasilkan hasil pada direktori baru. Dua XLSX sumber mengandung CSV satu kolom dan parser menangani format tersebut. Input, protokol dan environment tercatat. Hasil lintas versi dapat sedikit berbeda. Paket menyimpan hasil historis dan manifest sebagai pembanding, bukan menjanjikan semua environment identik.

Untuk alur Colab langsung, buka code/training/Colab_Langsung_Jalan.ipynb dan unggah tiga sumber yang diminta. Jangan memilih notebook lama yang mencari folder Drive. Alur ini menjalankan training bila user mengeksekusinya, sedangkan handover saat ini hanya mengemas kode yang sudah tersedia.

## Batas interpretasi

Kolom outcome pada data historis hanya untuk evaluasi. Model tidak memprediksi jumlah hari terlambat atau EAC implementasi. Untuk CSV custom, outcome belum diketahui dan hasil evaluasi pada dashboard tetap benchmark historis. As of fitur belum terbukti dan G01 tetap HOLD.
