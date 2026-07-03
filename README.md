# 📊 Unemployment Analysis with Python — Dampak Covid-19 terhadap Pasar Tenaga Kerja India

> Analisis data science menyeluruh terhadap dinamika tingkat pengangguran di India sebelum dan selama pandemi Covid-19, menggunakan pendekatan data cleaning, exploratory data analysis (EDA), dan analisis dampak kebijakan berbasis data.

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-150458?logo=pandas&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 📌 Project Overview

Proyek ini menyajikan analisis kuantitatif terhadap tingkat pengangguran (*unemployment rate*) di India menggunakan dua dataset resmi yang mencakup periode Mei 2019 hingga November 2020 — rentang waktu yang secara langsung mencakup awal mula pandemi Covid-19 dan penerapan lockdown nasional di India.

Analisis dilakukan menggunakan Python dengan pendekatan end-to-end data science: mulai dari pemahaman data (*data understanding*), pembersihan data (*data cleaning*), eksplorasi data (*exploratory data analysis*), hingga analisis dampak kebijakan (*policy impact analysis*). Proyek ini tidak hanya berhenti pada visualisasi, tetapi juga menerjemahkan temuan statistik menjadi insight yang actionable dan rekomendasi kebijakan yang realistis.

Proyek ini dibangun sebagai bagian dari portofolio Data Science untuk mendemonstrasikan kemampuan dalam data wrangling, visualisasi data, statistical thinking, dan kemampuan mengomunikasikan temuan data kepada audiens non-teknis (economic storytelling) — kompetensi inti seorang Data Analyst/Data Scientist di bidang ekonomi dan kebijakan publik.

---

## 🌍 Background

Tingkat pengangguran adalah salah satu indikator makroekonomi paling krusial dalam menilai kesehatan suatu perekonomian. Pengangguran yang tinggi berkorelasi dengan menurunnya daya beli masyarakat, meningkatnya risiko kemiskinan, serta potensi ketidakstabilan sosial-politik. Bagi pembuat kebijakan, memahami **kapan**, **di mana**, dan **seberapa besar** lonjakan pengangguran terjadi adalah prasyarat utama untuk merancang intervensi yang tepat sasaran — baik berupa bantuan sosial, stimulus ekonomi, maupun program pelatihan tenaga kerja.

Pandemi Covid-19 menjadi salah satu guncangan ekonomi (*economic shock*) terbesar dalam sejarah modern, memaksa banyak negara — termasuk India — menerapkan lockdown ketat yang menghentikan aktivitas ekonomi secara mendadak. Peristiwa ini menciptakan "eksperimen alami" yang sangat berharga untuk dianalisis: bagaimana pasar tenaga kerja bereaksi terhadap guncangan eksternal berskala nasional, dan wilayah mana yang lebih rentan atau lebih resilien.

---

## ❓ Business Problem

Proyek ini dirancang untuk menjawab pertanyaan-pertanyaan strategis berikut:

1. Bagaimana tren tingkat pengangguran di India dari waktu ke waktu (2019–2020)?
2. Seberapa besar dampak pandemi Covid-19 terhadap tingkat pengangguran nasional?
3. Wilayah (negara bagian/zona) mana yang paling terdampak, dan mana yang paling stabil?
4. Apakah terdapat perbedaan pola pengangguran antara area Rural dan Urban?
5. Bulan atau periode mana yang mengalami lonjakan pengangguran tertinggi?
6. Pola dan tren apa yang dapat diidentifikasi untuk mendukung perumusan kebijakan ekonomi dan sosial?

---

## 🗂️ Dataset Information

| Dataset | Deskripsi |
|---|---|
| `Unemployment_in_India.csv` | 768 observasi (740 valid setelah cleaning), periode **Mei 2019 – Juni 2020**, granularitas bulanan, mencakup 28 negara bagian, dipecah berdasarkan Area (Rural/Urban) |
| `Unemployment_Rate_upto_11_2020.csv` | 267 observasi, periode **Januari – November 2020**, mencakup 27 negara bagian dengan tambahan informasi Zona geografis dan koordinat (longitude/latitude) |

**Variabel utama yang tersedia:**

| Kolom | Deskripsi |
|---|---|
| `Region` | Nama negara bagian (state) di India |
| `Date` | Tanggal pencatatan data (bulanan) |
| `Frequency` | Frekuensi pencatatan data |
| `Estimated Unemployment Rate (%)` | Persentase penduduk usia kerja yang menganggur |
| `Estimated Employed` | Estimasi jumlah penduduk yang bekerja |
| `Estimated Labour Participation Rate (%)` | Persentase penduduk usia kerja yang aktif di pasar tenaga kerja |
| `Area` | Klasifikasi Rural atau Urban *(hanya di dataset 1)* |
| `Region.1` (Zone), `longitude`, `latitude` | Informasi zona geografis dan koordinat *(hanya di dataset 2)* |

> Kedua dataset bersumber dari data publik ketenagakerjaan India dan digunakan murni untuk tujuan edukasi/portofolio.

---

## 🎯 Project Objectives

- Menganalisis tren tingkat pengangguran di India secara nasional maupun regional.
- Membersihkan dan mempersiapkan data mentah agar siap dianalisis (data wrangling).
- Mengeksplorasi pola distribusi, sebaran, dan hubungan antarvariabel melalui visualisasi.
- Mengukur dan menginterpretasikan dampak pandemi Covid-19 terhadap tingkat pengangguran secara kuantitatif.
- Mengidentifikasi wilayah-wilayah yang paling terdampak dan paling resilien terhadap guncangan ekonomi.
- Merumuskan insight berbasis data yang dapat mendukung pengambilan keputusan kebijakan ekonomi dan sosial.

---

## 🛠️ Tools and Libraries

| Tool / Library | Fungsi dalam Proyek |
|---|---|
| **Python** | Bahasa pemrograman utama untuk seluruh proses analisis |
| **Pandas** | Data wrangling — pembacaan, pembersihan, transformasi, dan agregasi data tabular |
| **NumPy** | Komputasi numerik dan operasi array (perhitungan statistik, kondisi periode, dll.) |
| **Matplotlib** | Visualisasi dasar (line chart, bar chart) dan kustomisasi plot tingkat lanjut |
| **Seaborn** | Visualisasi statistik tingkat lanjut (histogram, boxplot, heatmap) dengan estetika lebih baik |

---

## 🔄 Data Analysis Workflow

1. **Data Collection** — Mengumpulkan dua dataset publik terkait tingkat pengangguran India dari periode 2019–2020.
2. **Data Cleaning** — Menghapus baris kosong dan duplikat, merapikan nama kolom, membersihkan whitespace pada data kategorikal, serta mengonversi kolom tanggal ke format `datetime`.
3. **Data Transformation** — Mengganti nama kolom agar lebih ringkas, menambahkan kolom bantu waktu (`Year`, `Month`, `Month_Name`), dan membuat label periode (sebelum/saat Covid-19).
4. **Exploratory Data Analysis (EDA)** — Menganalisis statistik deskriptif, distribusi, serta pola berdasarkan wilayah dan waktu menggunakan berbagai teknik visualisasi.
5. **Trend Analysis** — Mengidentifikasi tren jangka pendek, volatilitas antarwilayah, serta mendeteksi outlier menggunakan metode IQR.
6. **Covid-19 Impact Analysis** — Membandingkan periode sebelum dan selama Covid-19 secara kuantitatif untuk mengukur besar dan arah dampaknya di tingkat nasional maupun regional.
7. **Insight Generation** — Menerjemahkan seluruh temuan statistik menjadi insight naratif dan rekomendasi kebijakan yang applicable.

---

## 📈 Exploratory Data Analysis

Beberapa jenis visualisasi digunakan, masing-masing dipilih untuk menjawab pertanyaan analisis yang spesifik:

| Visualisasi | Tujuan Penggunaan |
|---|---|
| **Histogram** | Melihat bentuk distribusi unemployment rate (normal, skewed, atau memiliki ekor panjang akibat nilai ekstrem) |
| **Boxplot** | Membandingkan sebaran dan mendeteksi outlier antar kategori (Rural vs Urban, antarzona) |
| **Line Chart** | Melacak tren unemployment rate dari waktu ke waktu secara nasional maupun per wilayah |
| **Bar Chart** | Membandingkan rata-rata unemployment rate antarnegara bagian secara berdampingan |
| **Heatmap (korelasi)** | Mengukur kekuatan hubungan linear antara unemployment rate, jumlah pekerja, dan labour participation rate |
| **Heatmap (region × waktu)** | Mengidentifikasi apakah lonjakan pengangguran terjadi serentak secara nasional atau terlokalisasi pada wilayah tertentu |

Setiap visualisasi disertai interpretasi naratif untuk memastikan hasil analisis dapat dipahami oleh audiens non-teknis, bukan sekadar grafik tanpa konteks.

---

## 🦠 Covid-19 Impact Analysis

Pendekatan yang digunakan untuk mengukur dampak Covid-19 adalah **perbandingan dua periode (before-after comparison)**:

- **Sebelum Covid-19**: Mei 2019 – Februari 2020
- **Saat Covid-19**: Maret – Juni 2020 (bertepatan dengan lockdown nasional India)

Metrik yang dibandingkan antara lain rata-rata unemployment rate nasional, rata-rata per negara bagian, serta volatilitas (standar deviasi) di tiap wilayah. Selain itu, dilakukan **deteksi outlier menggunakan metode IQR (Interquartile Range)** untuk mengonfirmasi bahwa lonjakan ekstrem yang teramati bukan noise statistik, melainkan sinyal nyata dari peristiwa eksogen berskala nasional.

---

## 💡 Key Findings

1. Rata-rata unemployment rate nasional naik dari **9,51% (sebelum Covid)** menjadi **17,77% (saat Covid)** — kenaikan sebesar **86,9%**.
2. Puncak krisis terjadi pada **Mei 2020 (24,88%)**, disusul April 2020 (23,64%), bertepatan persis dengan lockdown nasional ketat.
3. Pemulihan terjadi cepat pada Juni 2020 (11,90%), namun **belum kembali ke level normal pra-pandemi**.
4. **Puducherry** mencatat kenaikan tertinggi (+37,4 poin persentase), diikuti **Tamil Nadu** (+22,6 poin) dan **Jharkhand** (+22,1 poin).
5. Wilayah seperti **Assam, Sikkim, dan Uttarakhand** menunjukkan tingkat stabilitas tertinggi selama krisis.
6. Ditemukan dua kategori masalah berbeda: pengangguran **struktural-kronis** (Tripura, Haryana) vs. **situasional akibat syok Covid** (Puducherry, Tamil Nadu).
7. Area **Urban** cenderung lebih rentan dibanding **Rural** terhadap guncangan ekonomi mendadak.
8. **Zona West** (Gujarat, Maharashtra, dll.) menunjukkan resiliensi ekonomi terbaik secara nasional.
9. **Zona East dan South** mengalami lonjakan paling ekstrem, masing-masing mencapai >33% pada April 2020.
10. Sebanyak **4,7% observasi tergolong outlier statistik**, dan **80% di antaranya terkonsentrasi tepat di bulan puncak lockdown** — mengonfirmasi sifat sistemik dari krisis ini.
11. Tidak ditemukan pola musiman (*seasonality*) yang kuat pada periode pra-pandemi, menandakan lonjakan yang teramati murni disebabkan oleh peristiwa eksogen.

---

## 🏛️ Policy Recommendations

- **Kebijakan Ketenagakerjaan**: Prioritaskan program padat karya di wilayah dengan lonjakan tertinggi, serta perkuat perlindungan kerja formal melalui subsidi upah sementara pada masa krisis.
- **Bantuan Sosial**: Rancang skema bantuan tunai darurat yang dapat terpicu otomatis saat indikator unemployment rate melewati ambang batas tertentu.
- **Pelatihan Tenaga Kerja**: Terapkan reskilling jangka panjang bagi wilayah dengan pengangguran struktural, dan diversifikasi keterampilan bagi wilayah yang rentan terhadap syok sektoral.
- **Dukungan Sektor Terdampak**: Berikan insentif fiskal bagi sektor jasa dan manufaktur di zona paling terdampak, serta perkuat sektor pertanian/UMKM sebagai penyangga ekonomi.
- **Strategi Pemulihan Ekonomi**: Bangun sistem *early-warning* berbasis data historis untuk mendeteksi lonjakan pengangguran secara dini, dan replikasi strategi diversifikasi ekonomi dari wilayah paling resilien ke wilayah yang lebih rentan.

---

## 📁 Project Structure

```
unemployment-analysis-india/
│
├── data/
│   ├── raw/
│   │   ├── Unemployment_in_India.csv
│   │   └── Unemployment_Rate_upto_11_2020.csv
│   └── processed/
│       ├── df1_clean.csv
│       └── df2_clean.csv
│
├── notebooks/
│   └── unemployment_analysis.ipynb
│
├── src/
│   └── analisis_unemployment_india.py
│
├── reports/
│   ├── Laporan_Analisis_Unemployment_India.docx
│   └── figures/
│       ├── 01_histogram_distribusi.png
│       ├── 02_boxplot_area_zone.png
│       ├── 03_line_tren_nasional.png
│       ├── 04_bar_rata_rata_per_region.png
│       ├── 06_heatmap_korelasi.png
│       ├── 07_heatmap_region_waktu.png
│       ├── 08_bar_sebelum_saat_covid.png
│       ├── 09_line_per_zona.png
│       └── 10_bar_dampak_per_state.png
│
├── requirements.txt
├── .gitignore
├── LICENSE
└── README.md
```

---

## ⚙️ Installation

```bash
# 1. Clone repository
git clone https://github.com/<username>/unemployment-analysis-india.git
cd unemployment-analysis-india

# 2. (Opsional tapi disarankan) Buat virtual environment
python -m venv venv
source venv/bin/activate      # Mac/Linux
venv\Scripts\activate         # Windows

# 3. Install dependencies
pip install -r requirements.txt
```

---

## ▶️ Usage

**Menjalankan script Python lengkap:**
```bash
python src/analisis_unemployment_india.py
```
Script akan otomatis membaca dataset, melakukan cleaning, menjalankan EDA, analisis dampak Covid-19, dan menyimpan seluruh visualisasi ke folder `reports/figures/`.

**Menjalankan melalui Jupyter Notebook (opsional, untuk eksplorasi interaktif):**
```bash
jupyter notebook notebooks/unemployment_analysis.ipynb
```

---

## 🚀 Future Improvements

- Menambahkan model prediktif (time series forecasting, misalnya ARIMA/Prophet) untuk memproyeksikan tren unemployment rate ke depan.
- Membangun dashboard interaktif (Streamlit/Power BI/Tableau) agar hasil analisis dapat dieksplorasi secara dinamis oleh pengguna non-teknis.
- Memperluas periode data hingga pasca-pandemi (2021–2023) untuk menganalisis kecepatan dan pola pemulihan jangka panjang.
- Menambahkan analisis spasial berbasis peta (choropleth map) memanfaatkan data longitude/latitude yang tersedia.
- Mengintegrasikan data makroekonomi lain (PDB, inflasi, IPM) untuk analisis multivariat yang lebih komprehensif.

---

## 👤 Author

**[Nama Anda]**
Data Analyst / Aspiring Data Scientist

- 🔗 LinkedIn  : (https://www.linkedin.com/in/muhammad-fahrur-rozy-325931245/)
- 💻 GitHub    : (https://github.com/PouBenParker)
- 📧 Email     : fahrurozy1602@gmail.com
- 📝 Portfolio : (https://myuniverseproject.wordpress.com/)

---

## 📄 License

Proyek ini dilisensikan di bawah [MIT License](LICENSE).
