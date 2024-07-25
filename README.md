# Rekomendasi Film Menggunakan Metode Naive Bayes dan Cosine Similarity

**Nama**: Nova Adrian Pasha  
**NIM**: A11.2020.12834



## Ringkasan dan Permasalahan Project

### Ringkasan

Proyek ini bertujuan untuk menyediakan rekomendasi film kepada pengguna berdasarkan nama film yang dimasukkan. Aplikasi web ini menggunakan metode Naive Bayes untuk analisis sentimen ulasan film dan Cosine Similarity untuk merekomendasikan film berdasarkan kesamaan konten.

### Permasalahan

- Menyediakan rekomendasi film yang relevan dan akurat kepada pengguna.
- Mengklasifikasikan ulasan film sebagai positif atau negatif menggunakan model Naive Bayes.

### Tujuan

- Mengimplementasikan model rekomendasi film berbasis konten dan analisis sentimen.
- Mengintegrasikan model ke dalam aplikasi web Flask untuk interaksi pengguna.

### Model / Alur Penyelesaian

1. **Praproses Data**: Mengumpulkan dan memproses data film.
2. **Membangun Model**:
   - **Model Rekomendasi**: Menggunakan Cosine Similarity untuk merekomendasikan film serupa.
   - **Model Sentimen**: Menggunakan Naive Bayes untuk analisis sentimen ulasan film.
3. **Integrasi Flask**: Membuat aplikasi web dengan Flask untuk menerima input pengguna, memproses data, dan menampilkan hasil.

![Bagan Alur](https://mermaid.ink/img/pako:eNpNkV1vgjAUhv8KOddgBKx8XCyZIssuTJbp1cCLM6hA1lJS2m3O-N9Xiyb2qj3Pc962OWeoRE0hhSMTP1WLUjn7rOwds56LN9o3mg-aYe9kqPDgeN6TszJ1LsVIR1Pe06_xMPkrS9fFOx0kHWmvcOycfe69ZvnNWFsju_Z_YtPdUyeYWbgxkKHqWgO35mXsRjeW5sXmG5m-Bj_C3MKXYtfxAfuHTnCBU8mxq80Pz1e5BNVSTktIzbamR9RMlVD2F6OiVmJ36itIldTUBSl000J6RDaakx5qVDTrsJHI74q5DtIz_EIaRNEsJMtkHvthnCwi4sIJUm8RzxaEBGFIkiSY-9Hy4sKfECZgPksS309IFMahT0gchDbuw8IpndadEnI7DcjO6fIPsqCD5Q?type=png) 

## Penjelasan Dataset, EDA, dan Proses Features Dataset

### Penjelasan Dataset

- **`main_data.csv`**: Berisi data film dengan kolom seperti `movie_title` dan `comb` yang digunakan untuk menghitung kesamaan film.
- **`reviews.txt`**: Berisi ulasan film untuk pelatihan model Naive Bayes.

### EDA (Exploratory Data Analysis)

- Melakukan analisis statistik deskriptif pada dataset film.
- Menganalisis distribusi genre, rating, dan atribut film lainnya.

### Proses Features Dataset

- Menggabungkan berbagai fitur teks menjadi satu kolom `comb` untuk menghitung kesamaan.
- Menggunakan `CountVectorizer` untuk mengubah teks menjadi matriks fitur.

## Proses Learning / Modeling

### Model Rekomendasi

- Menggunakan `CountVectorizer` untuk membuat matriks hitung dari deskripsi film.
- Menghitung kesamaan kosinus antar film menggunakan `cosine_similarity`.

### Model Sentimen

- Menggunakan Naive Bayes untuk mengklasifikasikan ulasan film sebagai positif atau negatif.
- Menggunakan TF-IDF untuk representasi fitur teks.

## Performa Model

- **Akurasi Model Sentimen**: 97.47%
  - Model menunjukkan performa yang sangat baik dalam mengklasifikasikan sentimen ulasan film.

## Diskusi Hasil dan Kesimpulan

### Diskusi Hasil

- **Model Rekomendasi**: Memberikan rekomendasi yang relevan berdasarkan kesamaan konten film. Hasilnya tergantung pada kualitas data dan fitur yang digunakan.
- **Model Sentimen**: Mencapai akurasi tinggi, menunjukkan bahwa model dapat dengan baik memprediksi sentimen ulasan film.
- **Deployment**: Saat ini, aplikasi belum dapat dideploy karena kendala biaya. Banyak layanan hosting memerlukan biaya yang tidak sesuai dengan anggaran, sehingga masih mencari solusi hosting yang terjangkau atau gratis.

### Kesimpulan

- Aplikasi web ini efektif dalam memberikan rekomendasi film berdasarkan nama film yang diberikan oleh pengguna.
- Model Naive Bayes memberikan hasil analisis sentimen yang akurat, yang bermanfaat untuk menentukan kualitas ulasan film.

## Hasil Screenshot Web

### Tampilan Halaman Utama

![Screenshot Halaman Utama](https://github.com/NovaAdrian/ML-4412/blob/main/images/ss1.PNG?raw=true) 
![Screenshot Halaman Utama](https://github.com/NovaAdrian/ML-4412/blob/main/images/ss2.PNG?raw=true) 
![Screenshot Halaman Utama](https://github.com/NovaAdrian/ML-4412/blob/main/images/ss3.PNG?raw=true) 

### Tampilan Halaman Rekomendasi

![Screenshot Halaman Rekomendasi](https://github.com/NovaAdrian/ML-4412/blob/main/images/ss5.PNG?raw=true) 
![Screenshot Halaman Rekomendasi](https://github.com/NovaAdrian/ML-4412/blob/main/images/ss4.PNG?raw=true) 

---

