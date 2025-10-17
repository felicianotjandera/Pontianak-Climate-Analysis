# Analisis Dinamika Iklim Pontianak (2010-2024)

Sebuah proyek analisis data dan visualisasi yang bertujuan untuk menganalisis tren dan pola iklim jangka panjang di Pontianak. Alur kerja proyek ini mencakup pembersihan data menggunakan Python (Pandas) dan pembuatan *dashboard* interaktif menggunakan Power BI.

---

## 📊 Dashboard

![Screenshot Dashboard Iklim Pontianak](pontianak-climate-analysis/pontianak-climate.png)

---

## 🎯 Deskripsi & Tujuan Proyek

Pontianak, sebagai kota yang dilintasi garis khatulistiwa, memiliki dinamika iklim yang unik. Proyek ini bertujuan untuk melakukan analisis data eksploratif (EDA) pada data klimatologis historis (2010-2024) untuk mengidentifikasi tren jangka panjang, pola musiman, dan hubungan antar parameter cuaca. Tujuannya adalah untuk menyajikan temuan ini dalam sebuah *dashboard* interaktif yang mudah dipahami, memberikan wawasan tentang perubahan iklim lokal.

---

## 🛠️ Alur Kerja (Workflow)

Proyek ini dibagi menjadi dua tahap utama untuk memanfaatkan kekuatan dari masing-masing *tool*:

1.  **Pembersihan & Persiapan Data (Python):**
    * Data mentah iklim dimuat menggunakan *library* Pandas.
    * Dilakukan pembersihan data, termasuk penanganan nilai tidak standar (`8888`, `9999`, `-`) yang diubah menjadi nilai kosong (`NaN`).
    * Data yang kosong diisi menggunakan metode *backward fill* (`bfill`), sebuah pendekatan yang cocok untuk data deret waktu.
    * Nama kolom diubah menjadi format yang deskriptif dan dalam Bahasa Inggris (misalnya, `Tavg` menjadi `Avg Temperature (°C)`).
    * Singkatan arah angin (`DDD_CAR`) dipetakan menjadi nama lengkap (misalnya, `SW` menjadi `Southwest`).
    * Hasil akhir adalah sebuah file CSV yang bersih (`pontianak_climate_cleaned.csv`) yang siap untuk divisualisasikan.

2.  **Visualisasi & Dashboard (Power BI):**
    * Data yang sudah bersih diimpor ke Power BI.
    * Sebuah *dashboard* interaktif dibangun untuk memvisualisasikan temuan utama, dengan fitur-fitur berikut:
        * **Kartu KPI:** Menampilkan ringkasan metrik utama seperti Suhu Rata-rata dan Total Curah Hujan.
        * **Grafik Tren:** Menganalisis perubahan suhu dan curah hujan dari tahun ke tahun.
        * **Analisis Distribusi:** Menunjukkan frekuensi kejadian cuaca (misalnya, berapa banyak hari dengan curah hujan tinggi).
        * **Analisis Angin:** Visualisasi arah angin yang paling dominan.
        * ***Slicer***: Filter interaktif berdasarkan **Tahun** dan **Bulan** untuk eksplorasi data yang dinamis.

---

## 💡 Temuan Utama (Key Insights)

*Dashboard* ini dirancang untuk menjawab pertanyaan-pertanyaan kunci seperti:
* Apakah ada tren peningkatan atau penurunan suhu rata-rata di Pontianak selama 14 tahun terakhir?
* Bulan apa saja yang secara konsisten menjadi puncak musim hujan dan musim kemarau?
* Bagaimana hubungan antara kelembapan udara dan curah hujan?
* Dari arah mana angin paling sering berhembus di Pontianak?

---

## 🔧 Tools yang Digunakan

* **Python:** Untuk pembersihan dan transformasi data.
    * *Library:* Pandas, NumPy, Matplotlib, Seaborn
* **Power BI:** Untuk membuat *dashboard* interaktif.
    * *Bahasa:* DAX (untuk membuat *measure* dan kolom kalkulasi)
* **Jupyter Notebook:** Sebagai lingkungan kerja untuk analisis data di Python.

---

## 🚀 Cara Menjalankan

1.  **Lihat Dashboard:** *Screenshot* utama dari *dashboard* dapat dilihat di atas.
2.  **Eksplorasi File Power BI:** Unduh file `.pbix` dan buka menggunakan Power BI Desktop untuk berinteraksi dengan *dashboard* secara penuh.
3.  **Jalankan Kode Python:** Buka file `pontianak-climate.ipynb` menggunakan Jupyter Notebook untuk melihat proses pembersihan dan analisis data. Pastikan Anda memiliki file data mentah di folder yang sama.
