# 🎓 Capstone Project: AI Assistant Usage in Student Life
## Data Classification and Summarization Analysis

### 📋 Overview
This capstone project analyzes AI assistant usage patterns among students using advanced machine learning techniques for classification and text summarization. The project combines traditional ML algorithms with modern AI models (IBM Granite) to provide comprehensive insights into how students interact with AI tools in their academic journey.

### 🎯 Objectives
- **Classification**: Automatically categorize AI assistant usage patterns (Academic, Personal, Creative)
- **Summarization**: Generate concise summaries of student feedback using IBM Granite
- **Analysis**: Identify key factors influencing AI adoption and usage in education
- **Insights**: Provide actionable recommendations for educational institutions and AI developers

### 📊 Dataset
- **Source**: Kaggle - AI Assistant Usage in Student Life (Synthetic)
- **Size**: Variable (depends on selected dataset)
- **Features**: Mixed (categorical, numerical, text)
- **Target**: Usage categories/patterns

### 🛠️ Technology Stack
- **Platform**: Google Colab
- **Language**: Python 3.8+
- **ML Framework**: Scikit-learn
- **AI Model**: IBM Granite (via Replicate.com)
- **Visualization**: Plotly, Matplotlib, Seaborn
- **Text Processing**: NLTK, TextStat

### 📁 Project Structure
```
capstone-project/
├── notebooks/
│   ├── 01_data_exploration.ipynb          # Data exploration and analysis
│   ├── 02_data_preprocessing.ipynb        # Data cleaning and preparation
│   ├── 03_classification_analysis.ipynb   # ML model training and evaluation
│   ├── 04_text_summarization.ipynb       # Text summarization with IBM Granite
│   ├── 05_model_evaluation.ipynb         # Comprehensive model evaluation
│   └── 06_visualization_dashboard.ipynb   # Interactive visualizations
├── data/
│   └── [dataset files - upload via notebook]
├── requirements.txt                       # Project dependencies
├── README.md                             # This file
└── presentation/
    └── presentation_structure.md         # Presentation outline
```

### 🚀 Quick Start

#### 1. Environment Setup
```bash
# Install required packages (in Google Colab)
!pip install -r requirements.txt

# Or install individual packages:
!pip install plotly replicate wordcloud textstat
```

#### 2. API Configuration
```python
# Set up Replicate API for IBM Granite access
import os
os.environ["REPLICATE_API_TOKEN"] = "your_replicate_token_here"
```

#### 3. Dataset Upload
```python
# Use Google Colab file upload
from google.colab import files
uploaded = files.upload()
```

#### 4. Notebook Execution Order
Run notebooks in the following sequence:
1. `01_data_exploration.ipynb` - Understand your data
2. `02_data_preprocessing.ipynb` - Clean and prepare data
3. `03_classification_analysis.ipynb` - Train ML models
4. `04_text_summarization.ipynb` - Generate summaries
5. `05_model_evaluation.ipynb` - Evaluate models comprehensively
6. `06_visualization_dashboard.ipynb` - Create final visualizations

### 📈 Expected Results

#### Classification Performance
- **Best Model**: Random Forest (expected ~85% accuracy)
- **Metrics**: Precision, Recall, F1-Score, Cross-validation scores
- **Features**: Feature importance analysis and interpretability

#### Summarization Quality
- **Compression**: ~70% text reduction
- **Quality**: Maintained key information integrity
- **Speed**: ~2-3 seconds per text summary

#### Visualizations
- Interactive dashboards with Plotly
- Comprehensive model comparison charts
- Feature importance visualizations
- Data exploration plots

### 🔧 Configuration Options

#### Model Parameters
```python
# Classification models can be configured:
models = {
    'Random Forest': RandomForestClassifier(n_estimators=100, random_state=42),
    'Gradient Boosting': GradientBoostingClassifier(random_state=42),
    'Logistic Regression': LogisticRegression(max_iter=1000, random_state=42),
    'SVM': SVC(probability=True, random_state=42)
}
```

#### Summarization Parameters
```python
# IBM Granite summarization settings:
summarization_params = {
    "max_tokens": 50,      # Summary length
    "temperature": 0.3,    # Creativity level
    "top_p": 0.9          # Nucleus sampling
}
```

### 📊 Key Features

#### 1. Comprehensive Data Analysis
- Automated data quality assessment
- Missing value handling strategies
- Feature engineering for mixed data types
- Statistical analysis and visualization

#### 2. Advanced Classification Pipeline
- Multiple algorithm comparison
- Cross-validation with stratified sampling
- Hyperparameter optimization
- Feature importance analysis
- Model interpretability tools

#### 3. State-of-the-Art Summarization
- IBM Granite integration via Replicate API
- Batch processing capabilities
- Quality metrics (compression ratio, readability)
- Error handling and retry logic

#### 4. Interactive Visualizations
- Plotly-based dashboards
- Real-time model comparison
- Feature importance plots
- Confusion matrix heatmaps
- Data distribution visualizations

#### 5. Comprehensive Evaluation
- Cross-validation analysis
- Learning curves
- Validation curves for hyperparameter sensitivity
- Stability analysis across random splits
- Error analysis and misclassification patterns

### 🎯 Use Cases

#### Educational Institutions
- Monitor AI tool adoption among students
- Identify usage patterns and trends
- Develop AI literacy programs
- Optimize learning resources

#### AI Tool Developers
- Understand user behavior and preferences
- Improve product features and UX
- Prioritize development roadmap
- Enhance user engagement strategies

#### Researchers
- Study human-AI interaction patterns
- Analyze impact of AI on learning
- Develop better AI educational tools
- Contribute to AI ethics discussions

### 🔍 Troubleshooting

#### Common Issues and Solutions

**1. API Connection Issues**
```python
# Test Replicate connection
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

**2. Memory Issues with Large Datasets**
```python
# Process data in chunks
def process_in_chunks(df, chunk_size=1000):
    for i in range(0, len(df), chunk_size):
        yield df[i:i + chunk_size]
```

**3. Model Training Time**
```python
# Use reduced parameter grids for faster training
param_grid_fast = {
    'n_estimators': [50, 100],  # Reduced from [50, 100, 200]
    'max_depth': [10, None]     # Reduced from [10, 20, None]
}
```

### 📚 Additional Resources

#### Learning Materials
- [Scikit-learn User Guide](https://scikit-learn.org/stable/user_guide.html)
- [Plotly Python Documentation](https://plotly.com/python/)
- [IBM Granite Model Details](https://replicate.com/ibm-granite/granite-3.0-8b-instruct)
- [NLTK Book](https://www.nltk.org/book/)

#### Related Projects
- Text Classification with Transformers
- Educational Data Mining Techniques
- AI Ethics in Education Research
- Automated Content Analysis Systems

### 🤝 Contributing
This is a capstone project, but suggestions and improvements are welcome:
1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

### 📝 License
This project is for educational purposes. Please respect the dataset license and API terms of service.

### 🙏 Acknowledgments
- Kaggle for providing the dataset
- IBM and Replicate for API access
- Open source community for excellent libraries
- Educational institution for project guidance

### 📞 Contact
- **Email**: [your.email@example.com]
- **LinkedIn**: [Your LinkedIn Profile]
- **GitHub**: [Your GitHub Repository]

---

**Note**: This project demonstrates practical application of data science techniques in educational technology. Results may vary based on dataset characteristics and parameter settings.

### 📊 Project Metrics
- **Lines of Code**: ~2,000+
- **Notebooks**: 6 comprehensive analyses
- **Models Tested**: 4-5 algorithms
- **Visualizations**: 20+ interactive charts
- **Processing Time**: ~45-60 minutes total
- **Documentation**: Comprehensive with examples

🎯 **Ready to explore AI assistant usage patterns? Start with notebook 01 and follow the journey!**