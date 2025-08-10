# 🎓 Capstone Project: Penggunaan AI Assistant dalam Kehidupan Mahasiswa
## Analisis Klasifikasi Data dan Ringkasan Teks

### 📋 Gambaran Umum
Proyek capstone ini menganalisis pola penggunaan AI assistant di kalangan mahasiswa menggunakan teknik machine learning lanjutan untuk klasifikasi dan summarization. Proyek ini menggabungkan algoritma ML tradisional dengan model AI modern (IBM Granite) untuk memberikan wawasan menyeluruh tentang bagaimana mahasiswa berinteraksi dengan alat AI dalam perjalanan akademis mereka.

### 🎯 Tujuan
- **Klasifikasi**: Mengkategorikan pola penggunaan AI assistant secara otomatis (Academic, Personal, Creative)  
- **Summarization**: Menghasilkan ringkasan singkat dari umpan balik mahasiswa menggunakan IBM Granite  
- **Analisis**: Mengidentifikasi faktor-faktor utama yang mempengaruhi adopsi dan penggunaan AI di pendidikan  
- **Wawasan**: Memberikan rekomendasi yang dapat ditindaklanjuti untuk institusi pendidikan dan pengembang AI

### 📊 Dataset
- **Sumber**: Kaggle - AI Assistant Usage in Student Life (https://www.kaggle.com/datasets/ayeshasal89/ai-assistant-usage-in-student-life-synthetic)  
- **Ukuran**: Variabel (tergantung dataset yang dipilih)  
- **Fitur**: Campuran (kategorikal, numerik, teks)  
- **Target**: Kategori/pola penggunaan

### 🛠️ Teknologi yang Digunakan
- **Platform**: Google Colab  
- **Bahasa**: Python 3.8+  
- **Framework ML**: Scikit-learn  
- **Model AI**: IBM Granite (via Replicate.com)  
- **Visualisasi**: Plotly, Matplotlib, Seaborn  
- **Pemrosesan Teks**: NLTK, TextStat

### 📁 Struktur Proyek
```
capstone-project/
├── notebooks/
│   ├── 01_data_exploration.ipynb          # Eksplorasi dan analisis data
│   ├── 02_data_preprocessing.ipynb        # Pembersihan dan persiapan data
│   ├── 03_classification_analysis.ipynb   # Pelatihan dan evaluasi model ML
│   ├── 04_text_summarization.ipynb        # Ringkasan teks dengan IBM Granite
│   ├── 05_model_evaluation.ipynb          # Evaluasi model secara komprehensif
│   └── 06_visualization_dashboard.ipynb   # Visualisasi interaktif
├── data/
│   └── [file dataset - unggah via notebook]
├── requirements.txt                       # Dependensi proyek
├── README.md                              # File ini
└── presentation/
    └── presentation_structure.md          # Struktur presentasi
```

### 🚀 Quick Start

#### 1. Persiapan Environment
```bash
# Install paket yang dibutuhkan (di Google Colab)
!pip install -r requirements.txt

# Atau install paket satu-per-satu:
!pip install plotly replicate wordcloud textstat
```

#### 2. Konfigurasi API
```python
# Siapkan Replicate API untuk akses IBM Granite
import os
os.environ["REPLICATE_API_TOKEN"] = "your_replicate_token_here"
```

#### 3. Unggah Dataset
```python
# Gunakan Google Colab file upload
from google.colab import files
uploaded = files.upload()
```

#### 4. Urutan Eksekusi Notebook
Jalankan notebook dalam urutan berikut:
1. `01_data_exploration.ipynb` - Pahami data Anda  
2. `02_data_preprocessing.ipynb` - Bersihkan dan persiapkan data  
3. `03_classification_analysis.ipynb` - Latih model ML  
4. `04_text_summarization.ipynb` - Hasilkan ringkasan  
5. `05_model_evaluation.ipynb` - Evaluasi model secara komprehensif  
6. `06_visualization_dashboard.ipynb` - Buat visualisasi akhir

### 📈 Hasil yang Diharapkan

#### Performa Klasifikasi
- **Best Model**: Random Forest (diperkirakan ~85% akurasi)  
- **Metrik**: Precision, Recall, F1-Score, skor Cross-validation  
- **Fitur**: Analisis feature importance dan interpretabilitas

#### Kualitas Ringkasan
- **Compression**: ~70% pengurangan teks  
- **Kualitas**: Menjaga integritas informasi utama  
- **Kecepatan**: ~2–3 detik per ringkasan teks

#### Visualisasi
- Dashboard interaktif dengan Plotly  
- Grafik perbandingan model yang lengkap  
- Visualisasi feature importance  
- Plot eksplorasi data

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
    "temperature": 0.3,    # Tingkat kreativitas
    "top_p": 0.9           # Nucleus sampling
}
```

### 📊 Fitur Utama

#### 1. Analisis Data Komprehensif
- Penilaian kualitas data otomatis  
- Strategi penanganan missing value  
- Feature engineering untuk tipe data campuran  
- Analisis statistik dan visualisasi

#### 2. Pipeline Klasifikasi Tingkat Lanjut
- Perbandingan beberapa algoritma  
- Cross-validation dengan stratified sampling  
- Optimasi hyperparameter  
- Analisis feature importance  
- Alat interpretabilitas model

#### 3. Summarization Mutakhir
- Integrasi IBM Granite via Replicate API  
- Kapabilitas batch processing  
- Metrik kualitas (rasio kompresi, readability)  
- Penanganan error dan logika retry

#### 4. Visualisasi Interaktif
- Dashboard berbasis Plotly  
- Perbandingan model secara real-time  
- Plot feature importance  
- Heatmap confusion matrix  
- Visualisasi distribusi data

#### 5. Evaluasi Komprehensif
- Analisis cross-validation  
- Learning curves  
- Validation curves untuk sensitivitas hyperparameter  
- Analisis stabilitas antar random split  
- Analisis error dan pola misclassification

### 🎯 Use Cases

#### Institusi Pendidikan
- Memantau adopsi alat AI di antara mahasiswa  
- Mengidentifikasi pola dan tren penggunaan  
- Mengembangkan program literasi AI  
- Mengoptimalkan sumber daya pembelajaran

#### Pengembang AI Tool
- Memahami perilaku dan preferensi pengguna  
- Meningkatkan fitur produk dan UX  
- Memprioritaskan roadmap pengembangan  
- Meningkatkan strategi keterlibatan pengguna

#### Peneliti
- Mempelajari pola interaksi manusia-AI  
- Menganalisis dampak AI pada pembelajaran  
- Mengembangkan alat pendidikan AI yang lebih baik  
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
        print("✅ API connected successfully")
        return True
    except Exception as e:
        print(f"❌ API error: {e}")
        return False
```

**2. Masalah Memori dengan Dataset Besar**
```python
# Proses data secara chunk
def process_in_chunks(df, chunk_size=1000):
    for i in range(0, len(df), chunk_size):
        yield df[i:i + chunk_size]
```

**3. Waktu Pelatihan Model**
```python
# Gunakan grid parameter yang diperkecil untuk pelatihan lebih cepat
param_grid_fast = {
    'n_estimators': [50, 100],  # Dikurangi dari [50, 100, 200]
    'max_depth': [10, None]     # Dikurangi dari [10, 20, None]
}
```

### 📚 Sumber Tambahan

#### Materi Belajar
- [Scikit-learn User Guide](https://scikit-learn.org/stable/user_guide.html)  
- [Plotly Python Documentation](https://plotly.com/python/)  
- [IBM Granite Model Details](https://replicate.com/ibm-granite/granite-3.0-8b-instruct)  
- [NLTK Book](https://www.nltk.org/book/)

#### Proyek Terkait
- Text Classification with Transformers  
- Educational Data Mining Techniques  
- AI Ethics in Education Research  
- Automated Content Analysis Systems

### 🤝 Kontribusi
Ini adalah proyek capstone, namun saran dan perbaikan sangat disambut:
1. Fork repository  
2. Buat feature branch Anda  
3. Commit perubahan Anda  
4. Push ke branch tersebut  
5. Buat Pull Request

### 📝 Lisensi
Proyek ini untuk tujuan edukasi. Mohon hargai lisensi dataset dan ketentuan layanan API.

### 🙏 Ucapan Terima Kasih
- Kaggle untuk penyediaan dataset  
- IBM dan Replicate untuk akses API  
- Komunitas open source untuk library yang luar biasa  
- Institusi pendidikan untuk bimbingan proyek

### 📞 Kontak
- **Email**: faizsyihab77@gmail.com  
- **LinkedIn**: [linkedin.com/in/faizsyihab/](https://linkedin.com/in/faizsyihab/)

---

**Catatan**: Proyek ini mendemonstrasikan aplikasi praktis teknik data science dalam teknologi pendidikan. Hasil dapat bervariasi berdasarkan karakteristik dataset dan pengaturan parameter.

### 📊 Metriķ Proyek
- **Lines of Code**: ~2,000+  
- **Notebooks**: 6 analisis komprehensif  
- **Model yang Diuji**: 4–5 algoritma  
- **Visualisasi**: 20+ chart interaktif  
- **Waktu Pemrosesan**: ~45–60 menit total  
- **Dokumentasi**: Komprehensif dengan contoh

🎯 **Siap menjelajahi pola penggunaan AI assistant? Mulai dari notebook 01 dan ikuti perjalanannya!**
