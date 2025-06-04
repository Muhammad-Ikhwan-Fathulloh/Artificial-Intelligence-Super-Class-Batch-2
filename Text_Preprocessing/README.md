# Text Processing dalam NLP

## 1. Pendahuluan
Text Processing adalah langkah awal dalam Natural Language Processing (NLP) yang bertujuan untuk membersihkan dan menyiapkan teks sebelum dianalisis atau digunakan dalam model machine learning. Proses ini mencakup beberapa tahapan seperti tokenization, stopword removal, stemming, dan lemmatization.

## 2. Langkah-langkah Text Processing
Berikut adalah langkah-langkah utama dalam text processing beserta contoh manual tanpa kode:

### a) Tokenization
Memisahkan teks menjadi unit kata atau kalimat.
- **Teks Asli**: "Saya sedang belajar Natural Language Processing."
- **Hasil Tokenization**: ["Saya", "sedang", "belajar", "Natural", "Language", "Processing", "."]

### b) Stopword Removal
Menghapus kata-kata umum yang tidak terlalu berkontribusi pada makna utama.
- **Sebelum**: ["Saya", "sedang", "belajar", "Natural", "Language", "Processing", "."]
- **Setelah**: ["belajar", "Natural", "Language", "Processing"]

### c) Stemming
Mengubah kata ke bentuk dasarnya dengan aturan tertentu.
- **Sebelum**: ["berlari", "bermain", "makan"]
- **Setelah Stemming**: ["lari", "main", "makan"]

### d) Lemmatization
Mengubah kata ke bentuk dasarnya dengan mempertimbangkan konteks gramatikal.
- **Sebelum**: ["running", "better", "was"]
- **Setelah Lemmatization**: ["run", "good", "be"]

## 3. Implementasi dalam Python
Berikut adalah implementasi dengan kode menggunakan pustaka NLTK dan spaCy:

```python
import nltk
from nltk.tokenize import word_tokenize
from nltk.corpus import stopwords
from nltk.stem import PorterStemmer, WordNetLemmatizer
import spacy

# Unduh dataset yang diperlukan
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')

# Contoh teks
text = "Saya sedang belajar Natural Language Processing."

# Tokenization
tokens = word_tokenize(text)
print("Tokenization:", tokens)

# Stopword Removal
stop_words = set(stopwords.words('indonesian'))
filtered_tokens = [word for word in tokens if word.lower() not in stop_words]
print("Stopword Removal:", filtered_tokens)

# Stemming
stemmer = PorterStemmer()
stemmed_words = [stemmer.stem(word) for word in filtered_tokens]
print("Stemming:", stemmed_words)

# Lemmatization
lemmatizer = WordNetLemmatizer()
lemmatized_words = [lemmatizer.lemmatize(word) for word in filtered_tokens]
print("Lemmatization:", lemmatized_words)
```

## 4. Kesimpulan
Text Processing adalah langkah esensial dalam NLP yang membantu dalam memahami teks sebelum digunakan dalam model machine learning. Dengan menerapkan teknik seperti tokenization, stopword removal, stemming, dan lemmatization, kita dapat meningkatkan kualitas analisis teks dan performa model NLP.