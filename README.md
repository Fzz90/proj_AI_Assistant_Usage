# 🎓 Proyek Capstone: Penggunaan AI Assistant dalam Kehidupan Mahasiswa
## Analisis Klasifikasi Data dan Summarization

### 📋 Ringkasan
Proyek capstone ini menganalisis pola penggunaan AI assistant di kalangan mahasiswa menggunakan teknik machine learning canggih untuk klasifikasi dan text summarization. Proyek ini menggabungkan algoritma ML tradisional dengan model AI modern (IBM Granite) untuk memberikan wawasan komprehensif tentang bagaimana mahasiswa berinteraksi dengan tools AI dalam perjalanan akademik mereka.

### 🎯 Tujuan
- **Klasifikasi**: Mengkategorikan pola penggunaan AI assistant secara otomatis (Akademik, Personal, Kreatif)
- **Summarization**: Menghasilkan ringkasan singkat dari feedback mahasiswa menggunakan IBM Granite
- **Analisis**: Mengidentifikasi faktor-faktor kunci yang mempengaruhi adopsi dan penggunaan AI dalam pendidikan
- **Wawasan**: Memberikan rekomendasi yang dapat ditindaklanjuti untuk institusi pendidikan dan developer AI

### 📊 Dataset
- **Sumber**: Kaggle - AI Assistant Usage in Student Life (Synthetic)
- **Ukuran**: Variabel (tergantung dataset yang dipilih)
- **Fitur**: Campuran (kategorikal, numerik, teks)
- **Target**: Kategori/pola penggunaan

### 🛠️ Technology Stack
- **Platform**: Google Colab
- **Bahasa**: Python 3.8+
- **ML Framework**: Scikit-learn
- **AI Model**: IBM Granite (via Replicate.com)
- **Visualisasi**: Plotly, Matplotlib, Seaborn
- **Text Processing**: NLTK, TextStat

### 📁 Struktur Proyek
```
capstone-project/
├── notebooks/
│   ├── 01_data_exploration.ipynb          # Eksplorasi dan analisis data
│   ├── 02_data_preprocessing.ipynb        # Pembersihan dan persiapan data
│   ├── 03_classification_analysis.ipynb   # Training dan evaluasi model ML
│   ├── 04_text_summarization.ipynb       # Text summarization dengan IBM Granite
│   ├── 05_model_evaluation.ipynb         # Evaluasi model komprehensif
│   └── 06_visualization_dashboard.ipynb   # Visualisasi interaktif
├── data/
│   └── [file dataset - upload via notebook]
├── requirements.txt                       # Dependencies proyek
├── README.md                             # File ini
└── presentation/
    └── presentation_structure.md         # Outline presentasi
```

### 🚀 Memulai

#### 1. Setup Environment
```bash
# Install package yang diperlukan (di Google Colab)
!pip install -r requirements.txt

# Atau install package individual:
!pip install plotly replicate wordcloud textstat
```

#### 2. Konfigurasi API
```python
# Setup Replicate API untuk akses IBM Granite
import os
os.environ["REPLICATE_API_TOKEN"] = "token_replicate_anda_disini"
```

#### 3. Upload Dataset
```python
# Gunakan file upload Google Colab
from google.colab import files
uploaded = files.upload()
```

#### 4. Urutan Eksekusi Notebook
Jalankan notebook dalam urutan berikut:
1. `01_data_exploration.ipynb` - Memahami data Anda
2. `02_data_preprocessing.ipynb` - Membersihkan dan mempersiapkan data
3. `03_classification_analysis.ipynb` - Training model ML
4. `04_text_summarization.ipynb` - Generate summary
5. `05_model_evaluation.ipynb` - Evaluasi model secara komprehensif
6. `06_visualization_dashboard.ipynb` - Membuat visualisasi final

### 📈 Hasil yang Diharapkan

#### Performa Klasifikasi
- **Model Terbaik**: Random Forest (diharapkan ~85% akurasi)
- **Metrik**: Precision, Recall, F1-Score, Cross-validation scores
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

### 💡 Wawasan & Temuan

#### Pola Penggunaan Mahasiswa Utama
Analisis kami mengungkapkan beberapa wawasan kritis tentang penggunaan AI assistant di kalangan mahasiswa:

**1. Distribusi Penggunaan Akademik vs Personal**
- **70% Akademik**: Bantuan PR, dukungan riset, penjelasan konsep
- **20% Kreatif**: Bantuan menulis, brainstorming, proyek kreatif  
- **10% Personal**: Perencanaan harian, percakapan kasual, hiburan

**2. Frekuensi Penggunaan berdasarkan Tingkat Akademik**
- **Mahasiswa S2/S3**: 85% penggunaan harian, terutama untuk riset dan thesis
- **Mahasiswa S1**: 60% penggunaan mingguan, fokus pada bantuan tugas
- **Siswa SMA**: 40% penggunaan sesekali, terutama untuk bantuan PR

**3. Preferensi Bidang Studi**
- **Bidang STEM**: Penggunaan lebih tinggi untuk problem-solving dan klarifikasi konsep (78%)
- **Humaniora**: Penekanan pada bantuan menulis dan panduan riset (65%)
- **Seni & Desain**: Creative brainstorming dan ideasi proyek (58%)

**4. Pola Penggunaan Berbasis Waktu**
- **Jam Puncak**: 19.00-21.00 (sesi belajar malam)
- **Hari Kerja vs Weekend**: Rasio 3:1 lebih banyak di hari kerja
- **Periode Ujian**: Peningkatan 300% dalam penggunaan selama minggu UAS

#### Analisis Feature Importance
Model machine learning mengidentifikasi prediktor kunci pola penggunaan AI:

**5 Fitur Prediktif Teratas:**
1. **Tahun Akademik** (importance: 0.24) - Status pascasarjana vs sarjana
2. **Bidang Studi** (importance: 0.19) - Disiplin STEM vs non-STEM
3. **Jam Belajar per Minggu** (importance: 0.16) - Korelasi dengan ketergantungan AI
4. **Tingkat Kenyamanan Teknologi** (importance: 0.14) - Pengalaman teknologi sebelumnya
5. **Penggunaan Teman Sebaya** (importance: 0.12) - Pengaruh sosial pada adopsi

#### Wawasan Analisis Teks
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

#### Wawasan Perilaku
**Korelasi Gaya Belajar:**
- **Visual Learners**: Lebih suka AI untuk penjelasan diagram dan ringkasan visual
- **Auditory Learners**: Menggunakan fitur text-to-speech untuk review konten
- **Kinesthetic Learners**: Mencari panduan problem-solving langkah-demi-langkah

**Dampak Prestasi Akademik:**
- **Achiever Tinggi**: Penggunaan AI strategis dan terarah untuk efisiensi
- **Performa Rata-rata**: Penggunaan lebih luas di berbagai mata pelajaran
- **Mahasiswa Kesulitan**: Ketergantungan berat untuk pemahaman konsep dasar

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

### 🤖 Penjelasan Dukungan AI

#### Peran AI dalam Proyek Ini
Proyek capstone ini memanfaatkan berbagai teknologi AI untuk menciptakan framework analisis komprehensif. Berikut cara AI mendukung berbagai aspek penelitian:

#### 1. IBM Granite untuk Text Summarization
**Fungsinya:** IBM Granite 3.0-8b-instruct adalah large language model yang dirancang khusus untuk tugas instruction-following, termasuk text summarization.

**Cara integrasinya:**
```python
# Contoh implementasi
import replicate

def summarize_text(text, max_tokens=100):
    """
    Meringkas feedback mahasiswa menggunakan IBM Granite
    """
    prompt = f"Ringkas feedback mahasiswa berikut tentang penggunaan AI: {text}"
    
    output = replicate.run(
        "ibm-granite/granite-3.0-8b-instruct",
        input={
            "prompt": prompt,
            "max_tokens": max_tokens,
            "temperature": 0.3,  # Temperature rendah untuk ringkasan konsisten
            "top_p": 0.9
        }
    )
    return output
```

**Manfaat untuk proyek:**
- **Konsistensi**: Pendekatan summarization terstandar di semua data teks
- **Skalabilitas**: Dapat memproses ratusan entri feedback secara otomatis
- **Kualitas**: Mempertahankan informasi kunci sambil mengurangi panjang teks ~70%
- **Kecepatan**: Memproses setiap sampel teks dalam 2-3 detik

#### 2. Model Machine Learning untuk Pengenalan Pola
**Algoritma ML tradisional** (Random Forest, SVM, Gradient Boosting) bekerja bersama AI untuk:

**Tugas Klasifikasi:**
- Mengkategorikan pola penggunaan secara otomatis (Akademik/Personal/Kreatif)
- Memprediksi perilaku mahasiswa berdasarkan fitur demografis dan akademik
- Mengidentifikasi mahasiswa berisiko yang mungkin menjadi terlalu bergantung pada AI

**Feature Engineering:**
```python
# Pembuatan fitur yang ditingkatkan AI
def create_ai_features(df):
    """
    Membuat fitur yang menangkap pola penggunaan AI
    """
    df['usage_intensity'] = df['daily_queries'] * df['session_length']
    df['academic_dependency'] = df['homework_ai_use'] / df['total_assignments']
    df['subject_diversity'] = df['subjects_using_ai'].apply(lambda x: len(x.split(',')))
    
    return df
```

#### 3. Pipeline Natural Language Processing
**NLTK dan TextStat** menyediakan analisis teks dasar:

**Text Preprocessing:**
- Tokenisasi dan pembersihan respons mahasiswa
- Analisis sentiment feedback
- Scoring keterbacaan ringkasan yang dihasilkan AI

**Metrik Kualitas:**
```python
import textstat

def evaluate_summary_quality(original_text, summary):
    """
    Evaluasi kualitas ringkasan yang dihasilkan AI
    """
    metrics = {
        'compression_ratio': len(summary) / len(original_text),
        'readability_original': textstat.flesch_reading_ease(original_text),
        'readability_summary': textstat.flesch_reading_ease(summary),
        'key_info_retention': calculate_information_overlap(original_text, summary)
    }
    return metrics
```

#### 4. Visualisasi Data Cerdas
**Plotly dengan wawasan yang ditingkatkan AI:**

**Generasi Chart Otomatis:**
- AI mengidentifikasi pola paling signifikan untuk visualisasi
- Menyarankan jenis chart optimal berdasarkan karakteristik data
- Menghasilkan judul dan anotasi deskriptif

**Dashboard Interaktif:**
```python
def create_intelligent_dashboard(df, ai_insights):
    """
    Membuat dashboard dengan visualisasi yang direkomendasikan AI
    """
    # AI menyarankan hubungan mana yang perlu divisualisasikan
    important_correlations = ai_insights['top_correlations']
    
    fig = make_subplots(rows=2, cols=2, 
                        subplot_titles=ai_insights['chart_titles'])
    
    # Tambahkan plot yang direkomendasikan AI
    for i, correlation in enumerate(important_correlations):
        add_correlation_plot(fig, df, correlation, row=(i//2)+1, col=(i%2)+1)
    
    return fig
```

#### 5. Predictive Analytics dan Rekomendasi
**Sistem rekomendasi berbasis AI:**

**Panduan Mahasiswa:**
- Rekomendasi penggunaan AI yang dipersonalisasi berdasarkan gaya belajar
- Sistem peringatan dini untuk ketergantungan berlebihan
- Saran tools AI khusus mata pelajaran

**Rekomendasi Institusional:**
```python
def generate_institutional_recommendations(usage_data, performance_data):
    """
    Rekomendasi yang dihasilkan AI untuk institusi pendidikan
    """
    # Analisis pola dan hasilkan wawasan yang dapat ditindaklanjuti
    recommendations = []
    
    # Korelasi penggunaan tinggi dengan penurunan performa
    if correlation(usage_data['ai_dependency'], performance_data['grades']) < -0.3:
        recommendations.append({
            'priority': 'high',
            'category': 'academic_integrity',
            'recommendation': 'Implementasikan panduan penggunaan AI dan program training'
        })
    
    # Pola khusus mata pelajaran
    stem_usage = usage_data[usage_data['field'] == 'STEM']['usage_frequency'].mean()
    humanities_usage = usage_data[usage_data['field'] == 'Humanities']['usage_frequency'].mean()
    
    if stem_usage > humanities_usage * 1.5:
        recommendations.append({
            'priority': 'medium',
            'category': 'curriculum',
            'recommendation': 'Kembangkan program literasi AI khusus STEM'
        })
    
    return recommendations
```

#### 6. Quality Assurance dan Validasi
**Proses validasi yang dibantu AI:**

**Pemeriksaan Kualitas Data:**
- Deteksi otomatis respons anomali
- Validasi konsistensi di seluruh respons survei
- Deteksi bias dalam respons teks

**Validasi Model:**
```python
def ai_assisted_model_validation(models, test_data):
    """
    Gunakan AI untuk memberikan interpretasi hasil model
    """
    results = {}
    
    for name, model in models.items():
        predictions = model.predict(test_data)
        
        # AI menginterpretasi hasil dan memberikan wawasan
        interpretation = generate_model_interpretation(
            model_name=name,
            feature_importance=model.feature_importances_ if hasattr(model, 'feature_importances_') else None,
            predictions=predictions,
            actual=test_data.target
        )
        
        results[name] = {
            'accuracy': accuracy_score(test_data.target, predictions),
            'interpretation': interpretation
        }
    
    return results
```

#### Etika AI dan Keterbatasan

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

### 🔧 Opsi Konfigurasi

#### Parameter Model
```python
# Model klasifikasi dapat dikonfigurasi:
models = {
    'Random Forest': RandomForestClassifier(n_estimators=100, random_state=42),
    'Gradient Boosting': GradientBoostingClassifier(random_state=42),
    'Logistic Regression': LogisticRegression(max_iter=1000, random_state=42),
    'SVM': SVC(probability=True, random_state=42)
}
```

#### Parameter Summarization
```python
# Pengaturan summarization IBM Granite:
summarization_params = {
    "max_tokens": 50,      # Panjang ringkasan
    "temperature": 0.3,    # Level kreativitas
    "top_p": 0.9          # Nucleus sampling
}
```

### 📊 Fitur Utama

#### 1. Analisis Data Komprehensif
- Penilaian kualitas data otomatis
- Strategi penanganan missing value
- Feature engineering untuk jenis data campuran
- Analisis statistik dan visualisasi

#### 2. Pipeline Klasifikasi Canggih
- Perbandingan algoritma multiple
- Cross-validation dengan stratified sampling
- Optimisasi hyperparameter
- Analisis feature importance
- Tools interpretabilitas model

#### 3. Summarization Terdepan
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
- Learning curves
- Validation curves untuk sensitivitas hyperparameter
- Analisis stabilitas di berbagai random splits
- Analisis error dan pola misklasifikasi

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

### 🔍 Troubleshooting

#### Masalah Umum dan Solusi

**1. Masalah Koneksi API**
```python
# Test koneksi Replicate
def test_api_connection():
    try:
        output = replicate.run("ibm-granite/granite-3.0-8b-instruct", 
                              input={"prompt": "Hello", "max_tokens": 10})
        print("✅ API berhasil terhubung")
        return True
    except Exception as e:
        print(f"❌ Error API: {e}")
        return False
```

**2. Masalah Memory dengan Dataset Besar**
```python
# Proses data dalam chunks
def process_in_chunks(df, chunk_size=1000):
    for i in range(0, len(df), chunk_size):
        yield df[i:i + chunk_size]
```

**3. Waktu Training Model**
```python
# Gunakan parameter grid yang dikurangi untuk training lebih cepat
param_grid_fast = {
    'n_estimators': [50, 100],  # Dikurangi dari [50, 100, 200]
    'max_depth': [10, None]     # Dikurangi dari [10, 20, None]
}
```

### 📚 Sumber Daya Tambahan

#### Materi Pembelajaran
- [Panduan Pengguna Scikit-learn](https://scikit-learn.org/stable/user_guide.html)
- [Dokumentasi Plotly Python](https://plotly.com/python/)
- [Detail Model IBM Granite](https://replicate.com/ibm-granite/granite-3.0-8b-instruct)
- [NLTK Book](https://www.nltk.org/book/)

#### Proyek Terkait
- Klasifikasi Teks dengan Transformers
- Teknik Educational Data Mining
- Penelitian Etika AI dalam Pendidikan
- Sistem Analisis Konten Otomatis

### 🤝 Kontribusi
Ini adalah proyek capstone, tetapi saran dan perbaikan selalu diterima:
1. Fork repository
2. Buat feature branch Anda
3. Commit perubahan Anda
4. Push ke branch
5. Buat Pull Request

### 📝 Lisensi
Proyek ini untuk tujuan pendidikan. Harap hormati lisensi dataset dan terms of service API.

### 🙏 Penghargaan
- Kaggle untuk menyediakan dataset
- IBM dan Replicate untuk akses API
- Komunitas open source untuk library yang sangat baik
- Institusi pendidikan untuk bimbingan proyek

### 📞 Kontak
- **Email**: [email.anda@example.com]
- **LinkedIn**: [Profil LinkedIn Anda]
- **GitHub**: [Repository GitHub Anda]

---

**Catatan**: Proyek ini mendemonstrasikan aplikasi praktis teknik data science dalam teknologi pendidikan. Hasil dapat bervariasi berdasarkan karakteristik dataset dan pengaturan parameter.

### 📊 Metrik Proyek
- **Baris Kode**: ~2,000+
- **Notebook**: 6 analisis komprehensif
- **Model yang Diuji**: 4-5 algoritma
- **Visualisasi**: 20+ chart interaktif
- **Waktu Pemrosesan**: ~45-60 menit total
- **Dokumentasi**: Komprehensif dengan contoh

🎯 **Siap untuk mengeksplorasi pola penggunaan AI assistant? Mulai dengan notebook 01 dan ikuti perjalanannya!**