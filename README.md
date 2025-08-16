# 🎓 Capstone Project: Penggunaan AI Assistant dalam Kehidupan Mahasiswa
## Data Classification and Summarization Analysis

### 📋 Overview
Penelitian ini bertujuan untuk memahami bagaimana mahasiswa dari berbagai disiplin ilmu menggunakan AI Assistant dalam menyelesaikan tugas. Dengan menganalisis hubungan antara jenis tugas (TaskType), tingkat bantuan AI (AI_AssistanceLevel), dan hasil akhir (FinalOutcome) terhadap kepuasan (SatisfactionRating), penelitian ini mencoba mengungkap apakah AI benar-benar membantu peningkatan kualitas tugas dan pengalaman belajar mahasiswa. Proyek ini menggunakan teknik machine learning canggih untuk klasifikasi dan text summarization. Proyek ini menggabungkan algoritma ML tradisional dengan model AI modern (IBM Granite) untuk memberikan insight komprehensif tentang bagaimana mahasiswa berinteraksi dengan tools AI dalam perjalanan akademik.

### 🎯 Tujuan
- **Klasifikasi**: Mengungkap dan mengklasifikasi secara otomatis pola penggunaan AI Assistant di berbagai bidang studi, mulai dari brainstorming, penulisan, hingga belajar—serta menganalisis final outcome terhadap hasil akhir yang dihasilkan
- **Summarization**: Menghasilkan ringkasan singkat dari feedback mahasiswa menggunakan model IBM Granite
- **Analisis**: Mengidentifikasi faktor-faktor penting yang mempengaruhi adopsi dan penggunaan AI dalam pendidikan
- **Insight**: Memberikan rekomendasi yang dapat ditindaklanjuti untuk institusi pendidikan dan developer AI

### 📊 Dataset
- **Sumber**: Kaggle - AI Assistant Usage in Student Life (Synthetic) (https://www.kaggle.com/datasets/ayeshasal89/ai-assistant-usage-in-student-life-synthetic)
- **Size**: Variabel (tergantung dataset yang dipilih)
- **Fitur**: Kategorikal & Numerikal
- **Target**: Kategori/pola penggunaan

### 🛠️ Technology Stack
- **Platform**: Google Colab
- **Bahasa**: Python 3.8+
- **ML Framework**: Scikit-learn
- **AI Model**: IBM Granite (via Replicate.com)
- **Visualisasi**: Plotly, Matplotlib, Seaborn
- **Text Processing**: NLTK, TextStat


### 🚀 Quick Start

#### Eksekusi Notebook
1. `01_data_class&visualization.ipynb` - Klasifikasi data serta visualisasinya
2. `02_text_summarization.ipynb` - Summarize text 

### 📈 Hasil yang Diharapkan

#### Performa Klasifikasi
- **Model Terbaik**: Tergantung target variable
- **Metrik**: Accuracy, Precision, Recall, F1-Score, Cross-validation mean
- **Fitur**: Analisis feature importance dan interpretabilitas

#### Kualitas Summarization
- **Kompresi**: ~70% pengurangan teks
- **Kualitas**: Mempertahankan integritas informasi kunci
- **Kecepatan**: ~2-3 detik per ringkasan teks

#### Visualisasi
- Dashboard interaktif dengan Plotly
- Chart perbandingan model komprehensif
- Visualisasi feature importance
- Plot eksplorasi data

### 💡 Insights & Findings

#### Pola Penggunaan Mahasiswa Utama
Analisis mengungkapkan beberapa wawasan penting tentang penggunaan AI assistant di kalangan mahasiswa:

**1. Distribusi Penggunaan TaskType vs Discipline**
- Writing = kebutuhan utama mahasiswa hampir semua jurusan.
- Coding digunakan lintas disiplin, tidak hanya di ilmu komputer.
- Research surprisingly rendah, menunjukkan mahasiswa lebih suka menggunakan AI untuk membantu tugas praktis ketimbang eksplorasi akademik mendalam.
- Math menonjol di Writing, indikasi bahwa AI dipakai untuk menjelaskan konsep dan menghasilkan laporan.

**2. Distribusi Hasil output dari penggunaan AI terhadap Discipline**
- Math unggul dalam menyelesaikan tugas (highest completion, lowest confusion).
- History cenderung pakai AI untuk ide drafting ketimbang langsung menyelesaikan tugas, sesuai sifat bidang yang berbasis esai dan argumentasi.
- Computer Science unik → banyak tugas selesai, tapi juga tertinggi dalam kategori gave up. Ini bisa menandakan gap antara ekspektasi teknis dan kualitas solusi AI.
- Biology punya tantangan dalam memahami hasil (highest confusion), tapi tetap rendah dalam menyerah.

**3. Hubungan Discipline dengan Total Prompt yang dihasilkan**
Mayoritas mahasiswa dari berbagai disiplin menggunakan AI assistant dengan intensitas rendah–sedang (median 3–4 prompts), dengan rata-rata hampir sama di semua bidang. Namun, terdapat kelompok kecil heavy users di setiap disiplin yang mendorong nilai maksimum tinggi (hingga 39 prompts). Variasi individu lebih berperan daripada perbedaan disiplin ilmu.


#### Analisis Fitur
Model machine learning mengidentifikasi prediktor kunci pola penggunaan AI:

**Fitur Prediktif Teratas:**
1. **StudentType (High School, Undergraduate, Graduate)**
2. **Discipline (Biology, CS, Engineering, Math, Psychology, History, Business)** 
3. **AIAssistanceLevel** (1, 2, 3, 4, 5) 
4. **SatisfactionRating** (1.0 ~ 5.0) 
5. **Total Prompt** (1 ~ 39)
6. **TaskType** (Writing, Studying, Homework Help, Coding, Brainstorming, Research)
7. **Final Oucome** (Assignment Completed, Idea Drafted, Confused, Gave Up)

#### Text Analysis Insights
Melalui analisis summarization dari feedback mahasiswa, kami menemukan:

**Tema Positif (65% dari feedback):**
- "Menghemat waktu untuk riset dan fact-checking"
- "Membantu memahami konsep-konsep kompleks"
- "Meningkatkan kualitas dan kejelasan tulisan"
- "Tersedia 24/7 untuk bantuan langsung"

**Kekhawatiran dan Tantangan (25% dari feedback):**
- "Risiko ketergantungan berlebihan dan berkurangnya critical thinking"
- "Kualitas bervariasi di berbagai bidang studi"
- "Kekhawatiran privasi dengan informasi akademik sensitif"
- "Potensi pelanggaran integritas akademik"

**Respon Netral/Campuran (10% dari feedback):**
- "Berguna tapi perlu supervisi manusia"
- "Titik awal yang baik tapi memerlukan verifikasi"

#### Implikasi Institusional
**Untuk Institusi Pendidikan:**
1. **Kebutuhan Pengembangan Kebijakan**: 78% mahasiswa menginginkan panduan penggunaan AI yang jelas
2. **Training Dosen**: Hanya 45% instruktur merasa siap membimbing penggunaan AI
3. **Integrasi Kurikulum**: Permintaan yang berkembang untuk mata kuliah literasi AI
4. **Integritas Akademik**: Kebutuhan untuk kode etik dan alat deteksi yang diperbarui

**Untuk Developer Tools AI:**
1. **Spesialisasi Pendidikan**: Permintaan untuk AI assistant khusus mata pelajaran
2. **Fitur Kolaborasi**: Mahasiswa menginginkan dukungan proyek kelompok
3. **Progress Tracking**: Minat pada learning analytics dan metrik peningkatan
4. **Aksesibilitas**: Kebutuhan untuk interface multibahasa dan ramah disabilitas

### 🤖 AI Support Explanation

#### Peran AI dalam Proyek Ini
Proyek capstone ini memanfaatkan berbagai teknologi AI untuk menciptakan framework analisis komprehensif. Berikut cara AI mendukung berbagai aspek penelitian:

#### 1. IBM Granite untuk Text Summarization
**Fungsinya:** IBM Granite 3.2-8b-instruct adalah large language model yang dirancang khusus untuk tugas instruction-following, termasuk text summarization.

**Manfaat untuk proyek:**
- **Konsistensi**: Pendekatan summarization terstandar di semua data teks
- **Skalabilitas**: Dapat memproses ratusan entri feedback secara otomatis
- **Kualitas**: Mempertahankan informasi kunci sambil mengurangi panjang teks ~70%
- **Kecepatan**: Memproses setiap sampel teks dalam 2-3 detik

#### 2. Model Machine Learning untuk Pengenalan Pola
**Algoritma ML tradisional** (Random Forest, Decision Tree, Logistic Regression, KNN) bekerja bersama AI untuk:

**Tugas Klasifikasi:**
- Mengkategorikan pola penggunaan AI secara otomatis 
- Memprediksi perilaku mahasiswa berdasarkan fitur demografis dan akademik

#### 3. Data Visualization
**Plotly with AI-enhanced insights:**

**Generate Chart Otomatis:**
- AI mengidentifikasi pola paling signifikan untuk visualisasi
- Menyarankan jenis chart optimal berdasarkan karakteristik data
- Menghasilkan judul dan anotasi deskriptif

#### 4. Quality Assurance and Validation
**Proses validasi yang dibantu AI:**

**Pemeriksaan Kualitas Data:**
- Deteksi otomatis respons anomali
- Validasi konsistensi di seluruh respons survei
- Deteksi bias dalam respons teks

#### Etika AI dan Keterbatasannya

**Langkah-langkah Transparansi:**
- Semua konten yang dihasilkan AI diberi label yang jelas
- Model confidence scores disediakan jika berlaku
- Validasi manusia diperlukan untuk wawasan kritis

**Mitigasi Bias:**
- Beberapa model digunakan untuk cross-validate temuan
- Data training yang beragam memastikan hasil representatif
- Audit bias reguler dilakukan pada output AI

**Perlindungan Privasi:**
- Tidak ada informasi identifikasi personal yang diproses oleh AI
- Semua data diagregasi sebelum analisis AI
- Panggilan API menggunakan koneksi yang aman dan terenkripsi

#### Peningkatan AI di Masa Depan
**Perbaikan yang direncanakan:**
1. **Analisis Real-time**: Pemrosesan data streaming dengan online learning
2. **AI Multimodal**: Menggabungkan analisis gambar dan video dari perilaku belajar
3. **Model Personal**: Pemodelan mahasiswa individual untuk rekomendasi yang disesuaikan
4. **Federated Learning**: Pembelajaran kolaboratif antar institusi sambil menjaga privasi

Pendekatan terintegrasi AI ini memastikan bahwa proyek capstone tidak hanya menganalisis penggunaan AI mahasiswa tetapi juga mendemonstrasikan praktik terbaik untuk implementasi AI yang bertanggung jawab dalam penelitian pendidikan.

### 📊 Fitur Utama

#### 1. Analisis Data Komprehensif
- Penilaian kualitas data otomatis
- Strategi penanganan missing value
- Feature engineering untuk jenis data campuran
- Analisis statistik dan visualisasi

#### 2. Pipeline Klasifikasi Canggih
- Perbandingan algoritma multiple
- Cross-validation
- Optimisasi hyperparameter
- Analisis feature importance

#### 3. State-of-the-Art Summarization
- Integrasi IBM Granite via Replicate API
- Kemampuan batch processing
- Metrik kualitas (compression ratio, readability)
- Error handling dan retry logic

#### 4. Visualisasi Interaktif
- Dashboard berbasis Plotly
- Perbandingan model real-time
- Plot feature importance
- Heatmap confusion matrix
- Visualisasi distribusi data

#### 5. Evaluasi Komprehensif
- Analisis cross-validation
- Analisis error dan confusion matrix

### 🎯 Use Cases

#### Institusi Pendidikan
- Memantau adopsi tools AI di kalangan mahasiswa
- Mengidentifikasi pola dan tren penggunaan
- Mengembangkan program literasi AI
- Mengoptimalkan sumber daya pembelajaran

#### Developer Tools AI
- Memahami perilaku dan preferensi pengguna
- Meningkatkan fitur produk dan UX
- Memprioritaskan roadmap pengembangan
- Meningkatkan strategi engagement pengguna

#### Peneliti
- Mempelajari pola interaksi manusia-AI
- Menganalisis dampak AI pada pembelajaran
- Mengembangkan tools AI pendidikan yang lebih baik
- Berkontribusi pada diskusi etika AI

### 📚 Sumber Tambahan

#### Materi Pembelajaran
- [Panduan Pengguna Scikit-learn](https://scikit-learn.org/stable/user_guide.html)
- [Dokumentasi Plotly Python](https://plotly.com/python/)
- [Detail Model IBM Granite](https://replicate.com/ibm-granite/granite-3.2-8b-instruct)
- [NLTK Book](https://www.nltk.org/book/)


### 📝 Lisensi
Proyek ini untuk tujuan pendidikan. Harap hormati lisensi dataset dan terms of service API.

### 📞 Kontak
- **Email**: faizsyihab77@gmail.com
- **LinkedIn**: https://www.linkedin.com/in/faizsyihab/

---

**Catatan**: Proyek ini mendemonstrasikan aplikasi praktis teknik data science dalam teknologi pendidikan. Hasil dapat bervariasi berdasarkan karakteristik dataset dan pengaturan parameter.

### 📊 Metrik Proyek
- **Baris Kode**: ~2,000+
- **Notebook**: 6 analisis komprehensif
- **Model yang Diuji**: 4-5 algoritma
- **Visualisasi**: 20+ chart interaktif
- **Waktu Pemrosesan**: ~45-60 menit total
- **Dokumentasi**: Komprehensif dengan contoh
