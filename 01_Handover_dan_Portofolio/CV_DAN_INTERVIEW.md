# Materi CV dan interview

## Entri proyek pada CV berbahasa Indonesia

**AI Project Risk Monitoring — Proyek Portofolio PMO dengan Bantuan AI**

- Menyusun portofolio simulasi pengelolaan inisiatif AI melalui delapan tahap, mencakup WBS 28 task, anggaran simulasi, RAID, tata kelola dan pelaporan keputusan.
- Mengarahkan dashboard HTML untuk prioritisasi review 20%, serta menilai hasil benchmark sintetis 277 proyek test dengan menampilkan pembanding, beban review dan keterbatasan model.
- Mendokumentasikan perubahan alat, status gate HOLD, rencana pemeriksaan data dan paket handover dengan jejak bukti serta panduan reproduksi.

## CV wording in English

**AI Project Risk Monitoring — AI assisted PMO Portfolio Simulation**

- Developed an eight stage PMO portfolio simulation covering a 28 task WBS, simulated budgeting, RAID governance and decision reporting with AI assistance.
- Directed an offline HTML review dashboard using a 20% capacity scenario and assessed synthetic model evidence across 277 test projects against a CPI rule.
- Documented tool changes, model HOLD criteria, data review options and a traceable handover package with reproduction instructions.

Tempatkan entri pada bagian Projects, bukan pengalaman kerja perusahaan. Tidak ada gelar pekerjaan, tanggal masa kerja, deployment produksi, penghematan atau stakeholder perusahaan nyata yang ditambahkan.

## Narasi pembuka sekitar satu menit

Saya membuat AI Project Risk Monitoring sebagai simulasi portofolio untuk memperlihatkan cara saya mengarahkan dan mengendalikan inisiatif AI dari perspektif PMO. Saya menggunakan bantuan AI untuk kode dan dokumen, sementara saya menetapkan arah, membatasi lingkup serta mengoreksi keputusan yang tidak sesuai. Dashboard akhirnya memakai HTML agar demo dapat dibuka langsung. Pada kapasitas review 56 dari 277 proyek test sintetis, model menangkap 44 kasus terlambat dibanding 39 oleh aturan CPI. Saya tetap mencatat hasilnya belum konklusif dan menahan penggunaan operasional karena bukti waktu tersedia fitur belum cukup. Yang saya tunjukkan adalah proses pengendalian dan keputusan berbasis bukti, disertai artefak yang dapat diperiksa.

## Alur demo sekitar lima menit

| Waktu | Materi yang ditunjukkan | Pesan |
|---|---|---|
| Menit 0 sampai 1 | README dan business case | Masalah prioritisasi review dan tujuan simulasi |
| Menit 1 sampai 2 | WBS, budget dan Jira | Perencanaan, status review dan batas actual SIM |
| Menit 2 sampai 3 | Risk Monitoring dan Model Evaluation | 56 prioritas, 44 vs 39, serta 144 kasus terlewat |
| Menit 3 sampai 4 | Current RAID dan brief Opsi B | Mengapa model HOLD dan opsi tindak lanjut |
| Menit 4 sampai 5 | Runbook dan checklist handover | Reproduksi, batas QA dan penerimaan yang masih terbuka |

## Pertanyaan yang perlu dapat dijelaskan

**Mengapa memakai AI jika aturan sederhana sudah ada?** Tujuannya menguji apakah ranking AI membantu pada beban review yang sama. Lima tambahan kasus pada test sintetis belum membuktikan keunggulan konklusif, jadi keputusan penggunaan tidak dipaksakan.

**Apa arti melatih model?** Algoritma mempelajari hubungan fitur dan label dari subset training. Validation memilih konfigurasi. Test dipakai untuk penilaian akhir, bukan untuk tuning setelah hasil dilihat. Model tabular ini menggunakan CPU dan tidak membutuhkan pendekatan NLP atau IndoBERT.

**Mengapa kapasitas 20%?** Itu skenario demo yang saya pilih. Dengan 277 proyek, pembulatan ke atas menghasilkan 56 prioritas. Itu bukan bukti kapasitas staffing suatu perusahaan.

**Mengapa status model HOLD?** Pemisahan train dan test saja belum membuktikan fitur benar benar tersedia pada saat prediksi. Bukti generator dan pembekuan baseline belum cukup. Opsi B memeriksa hal tersebut sebelum memutuskan training ulang.

**Apakah proyek ini menghemat biaya perusahaan?** Belum ada pengukuran itu. Anggaran adalah alokasi simulasi, dan hasil model adalah benchmark sintetis. Saya tidak mengubahnya menjadi klaim penghematan atau penurunan keterlambatan.

**Apa yang Anda kerjakan sendiri dan apa bantuan AI?** Saya mengarahkan tujuan, lingkup, kapasitas demo, pilihan alat serta koreksi konteks. AI membantu membuat kode, analisis dan dokumen. Saya perlu memahami dan meninjau artefak sebelum menggunakannya dalam lamaran.

**Apa yang akan diperbaiki berikutnya?** Memperkuat bukti as of, melengkapi UAT, merekonsiliasi dampak perubahan terhadap forecast, lalu mencatat keputusan owner. Tidak menjanjikan model baru sebelum hasil pemeriksaan data.
