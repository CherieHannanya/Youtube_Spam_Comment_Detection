# Youtube_Spam_Comment_Detection
Machine Learning project to classify YouTube spam comments using Bernoulli Naive Bayes
YouTube Spam Comment Detection
1. Deskripsi Project
Project ini membahas penggunaan Machine Learning untuk
mengklasifikasikan komentar YouTube ke dalam dua kategori, yaitu
Spam dan Ham (bukan spam). Notebook yang menjadi sumber
pembahasan menggunakan algoritma Bernoulli Naive Bayes.
2. Dataset
Dataset yang digunakan adalah YouTube Spam Collection, yang terdiri
dari komentar dari lima video YouTube:
- Psy
- Katy Perry
- LMFAO
- Eminem
- Shakira
Jumlah keseluruhan data adalah 1.956 komentar, dengan rincian:

  Video               Spam       Ham       Total
  Psy                  175       175         350
Katy Perry           175       175         350
LMFAO                236       202         438
Eminem               245       203         448
Shakira              174       196         370
Total      1.005   951   1.956
Atribut Dataset
  Atribut        Keterangan
  COMMENT_ID   Identitas komentar
AUTHOR       Nama atau identitas penulis komentar
DATE         Tanggal komentar
CONTENT      Isi komentar
CLASS        Label kelas komentar

Pada pemeriksaan data, kolom DATE memiliki 245 nilai kosong. Kolom
lainnya memiliki 1.956 nilai terisi. Kolom DATE tidak digunakan dalam
pemodelan. Fitur yang digunakan adalah CONTENT, sedangkan CLASS
menjadi label target.

Sumber dataset: UCI Machine Learning Repository -- YouTube Spam
Collection

Notebook sumber: Kaggle -- YouTube Spam Comment
Detection
3. Metode dan Algoritma
Algoritma yang digunakan adalah Bernoulli Naive Bayes, yaitu
algoritma klasifikasi yang menggunakan pendekatan probabilitas dan cocok
untuk fitur biner.

Sebelum klasifikasi, teks komentar diubah menjadi representasi numerik
menggunakan CountVectorizer.

Pembagian data dilakukan menggunakan train_test_split dengan
perbandingan:
- 80% data training.
- 20% data testing.
Label kelas yang digunakan:
- 0 = Ham (bukan spam).
- 1 = Spam.
4. Alur Sistem
1. Mengimpor library yang dibutuhkan.
2. Membaca dataset komentar dari lima video.
3. Menggabungkan seluruh dataset.
4. Memeriksa dan memahami kondisi data.
5. Memilih isi komentar (CONTENT) sebagai fitur dan CLASS sebagai
   label.
6. Mengubah teks menjadi fitur numerik menggunakan CountVectorizer.
7. Membagi data menjadi data training dan data testing.
8. Melatih model menggunakan Bernoulli Naive Bayes.
9. Menguji model dan menghitung akurasi.
10. Menggunakan model untuk memprediksi komentar baru.
5. Hasil Evaluasi
Hasil evaluasi pada notebook menunjukkan akurasi sebesar 87,5%.

Artinya, model mengklasifikasikan sekitar 87,5% data pengujian dengan
benar. Nilai ini merupakan hasil pada pembagian data yang digunakan
dalam notebook, bukan jaminan bahwa model akan selalu memperoleh akurasi
yang sama pada data lain.
6. Kesimpulan
Berdasarkan notebook yang dianalisis, algoritma Bernoulli Naive Bayes
dapat digunakan untuk mengklasifikasikan komentar YouTube menjadi Spam
dan Ham. Teks komentar diproses menggunakan CountVectorizer sebelum
digunakan dalam proses pelatihan dan pengujian model. Pada pengujian
yang dilakukan, model memperoleh akurasi sebesar 87,5%.
7. File Repository
- youtube-spam-comment-detection(1).ipynb --- notebook sumber yang
  berisi kode dan proses analisis.
- README.md --- penjelasan dan rangkuman isi notebook.
