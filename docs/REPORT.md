# Laporan Kelompok — ANN Bake-Off

> Isi semua bagian di bawah. Hapus _italic placeholder_ setelah diisi.

## Identitas Kelompok

- **Nama Kelompok:** ML Gas
- **Anggota:**
  1. Timothy Antonio - 32230137 - Single Layer
  2. Valwa Giraldy - 
  3. Charlie
  4. Jonathan Tjendra -
  5. Haris Nurzahman - 

---

## 1. Ringkasan Hasil Eksperimen

_Tabel hasil akhir dari notebook `05_comparison.ipynb`. Boleh copy-paste tabel markdown atau screenshot._

| Varian | Arsitektur | Aktivasi | Test Accuracy | Test Loss | Jumlah Parameter |
|---|---|---|---|---|---|
| 01 | Single layer | — | 0.8646 | 0.4167 | 15 |
| 02 | 1 hidden (16) | Sigmoid | 0.9000 | 0.3082 | 131 |
| 03 | 1 hidden (16) | Tanh | 0.9333 | 0.1463 | 131 |
| 04 | 2 hidden (32→16) | ReLU | 0.9333 | 0.1025 | 739 |

---

## 2. Analisis & Diskusi

Pilih **minimal 3 pertanyaan** dari daftar pertanyaan diskusi di `README.md` dan jawab di sini.

### 2.1 Apakah single-layer mampu mencapai akurasi yang sebanding dengan multi-layer? Mengapa?

_Jawaban. Pada eksperimen yang dilakukan menggunakan dataset Iris, model single-layer masih mampu mencapai akurasi yang cukup tinggi. Hal ini terjadi karena dataset Iris memiliki pola yang relatif sederhana dan jumlah fitur yang sedikit, sehingga pemisahan antar kelas tidak terlalu kompleks. Namun, performa model multi-layer tetap lebih baik karena hidden layer mampu mempelajari hubungan non-linear yang lebih kompleks dibandingkan single-layer.

Model multi-layer juga menunjukkan stabilitas yang lebih baik selama proses training. Loss cenderung turun lebih konsisten dan validation accuracy lebih stabil dibandingkan model tanpa hidden layer. Oleh karena itu, walaupun single-layer cukup baik untuk dataset sederhana seperti Iris, arsitektur multi-layer lebih unggul untuk generalisasi dan dataset yang lebih kompleks.

### 2.2 Pada dataset ini, apakah ReLU benar-benar konvergen lebih cepat dibanding Sigmoid? Buktikan dengan grafik loss.

_Jawaban... Berdasarkan hasil eksperimen, fungsi aktivasi ReLU menunjukkan proses konvergensi yang lebih cepat dibandingkan Sigmoid. Hal ini terlihat dari grafik training loss, di mana loss pada model ReLU turun lebih tajam pada epoch awal dan mencapai nilai stabil lebih cepat.

Sebaliknya, model dengan aktivasi Sigmoid mengalami penurunan loss yang lebih lambat. Ini terjadi karena Sigmoid memiliki masalah vanishing gradient ketika nilai neuron terlalu besar atau terlalu kecil, sehingga pembaruan bobot menjadi lambat. ReLU tidak mengalami saturasi pada nilai positif sehingga proses optimisasi lebih efisien.

Selain lebih cepat konvergen, model ReLU juga menghasilkan akurasi akhir yang sedikit lebih tinggi dibandingkan Sigmoid pada eksperimen ini. Dengan demikian, hasil eksperimen mendukung teori bahwa ReLU lebih efektif untuk proses training neural network modern.

### 2.3 Bandingkan klaim bahwa “Tanh mempercepat pembelajaran karena zero-centered” dengan hasil empiris Anda.

_Jawaban... Secara teori, fungsi aktivasi Tanh memiliki keunggulan dibanding Sigmoid karena outputnya berada pada rentang -1 hingga 1 (zero-centered). Hal ini membantu proses optimisasi menjadi lebih stabil karena distribusi aktivasi lebih seimbang di sekitar nol.

Hasil eksperimen menunjukkan bahwa model dengan Tanh memang belajar lebih cepat dibanding Sigmoid pada beberapa epoch awal. Penurunan loss terlihat lebih stabil dan akurasi meningkat lebih cepat. Namun, performanya masih sedikit di bawah ReLU dalam hal kecepatan konvergensi.

Walaupun demikian, Tanh tetap memberikan hasil yang baik dan lebih stabil dibanding Sigmoid. Hasil empiris ini sesuai dengan teori pada slide bahwa sifat zero-centered pada Tanh membantu mempercepat pembelajaran neural network.

---

## 3. Refleksi Proses Kerja Kelompok

_300–500 kata. Ceritakan:_
- _Bagaimana kelompok membagi tugas?_ Pembagian kelompok ini dipilih berdasarkan kemauann anggota supaya adil dan bertanggung jawab atas tugasnya masing-masing
- _Kesulitan apa yang muncul (teknis maupun non-teknis)?_ Dibeberapa tugas ada algoritma yang masih kurang dipahami dan begitu juga dalam proses pengerjaan seperti bagian membangun model, melatih model masih kurang dipahami
- _Bagaimana cara mengatasinya?_ untuk solusi untuk mengatasi permasalahan bagi yang belum memahami cara melatih model dan membangun model kita mmemerlukan bantuan dari "Gemini AI" yang menjelaskan step bystep nya
- _Pelajaran apa yang bisa dibawa ke proyek ML berikutnya?_ Pelajaran ini dapat diharapakan bisa membawa ke dunia nyata 

---

## 4. Kontribusi Tiap Anggota

| Anggota | Kontribusi Konkret | % Effort |
|---|---|---|
| Valwa Giraldy|  | 100 |
| Timothy Antonio |  | 100 |
| Novandy amcals| | 100 |
| Haris Nurzaman |  | 85 |
| Joanthan Tjendra Kusnadi |  | | 90 |

_Total harus 100%._

---

## 5. Referensi

_Jika kalian merujuk sumber di luar slide kuliah, tulis di sini (format bebas tapi konsisten)._
