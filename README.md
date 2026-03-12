# Tugas Individu 3: Praktik Machine Learning (Computer Vision - OpenCV Part 3)
**Dosen Pengampu:** Herfandi, Ph.D.

Repositori ini berisi dokumentasi dan implementasi kode program untuk praktikum pengolahan citra digital menggunakan library OpenCV. Praktikum ini mencakup teknik-teknik fundamental yang digunakan dalam tahap pra-pemrosesan citra pada alur kerja Machine Learning dan Computer Vision.

---

## Identitas Mahasiswa
- **Nama:** [Wanda Setya Budi]
- **NIM:** [231001008]
- **Kelas:** Informatika – [C]

---

## Ringkasan Materi Praktik
Praktikum ini berfokus pada manipulasi citra menggunakan:
- **Editor:** Jupyter Notebook / VS Code (Python 3.x)
- **Library Utama:** `OpenCV (cv2)`, `NumPy`

### Fitur dan Implementasi:
1. **Image Smoothing (Penghalusan Citra):**
   - Reduksi noise menggunakan `cv2.blur()` dan `cv2.GaussianBlur()`.
   - Pengaturan ukuran kernel secara interaktif melalui Trackbar.
2. **Image Binarization (Thresholding):**
   - Konversi citra berwarna (BGR) ke Grayscale.
   - Eksperimen berbagai tipe Thresholding: `THRESH_BINARY`, `THRESH_BINARY_INV`, `THRESH_TRUNC`, `THRESH_TOZERO`.
   - Implementasi **Otsu’s Thresholding** untuk segmentasi objek secara otomatis tanpa penentuan nilai ambang manual.
3. **Edge Detection (Deteksi Tepi):**
   - Menggunakan algoritma **Canny Edge Detection**.
   - Penggunaan Trackbar ganda untuk menentukan batas minimal dan maksimal nilai Hysteresis secara real-time.

---

## Analisis & Kesimpulan
Berdasarkan hasil praktik, didapatkan beberapa poin analisis penting:
- **Peran Grayscale:** Sebagian besar fungsi analisis seperti Thresholding dan Canny membutuhkan input 1 channel (Grayscale) karena perhitungan didasarkan pada intensitas cahaya/kecerahan, bukan informasi warna.
- **Efektivitas Smoothing:** Teknik Gaussian Blur terbukti lebih efektif dalam menjaga integritas tepi objek dibandingkan Averaging biasa saat dilakukan penghalusan. Proses ini sangat krusial dilakukan sebelum deteksi tepi agar garis yang dihasilkan tidak terputus oleh noise.
- **Keunggulan Otsu's Method:** Metode Otsu mempermudah proses binarisasi dengan menghitung nilai ambang optimal berdasarkan varians antar-kelas pada histogram citra.
- **Fungsi Trackbar:** Fitur ini sangat membantu dalam proses *hyperparameter tuning* (mencari angka parameter terbaik) secara visual tanpa harus mengubah kode secara manual berulang kali.

---

## Video Presentasi & Demonstrasi
Penjelasan rinci mengenai logika pemrograman per baris serta demonstrasi jalannya aplikasi dapat diakses melalui tautan berikut:

👉 [https://youtu.be/sxHkUS8SEoo?si=4qQZiuseBeIsGr08]

---

## Referensi Tambahan
- **Official OpenCV Documentation:** [https://docs.opencv.org/](https://docs.opencv.org/)
- **Materi Kuliah:** Machine Learning - Computer Vision Part 3 (Informatika UTS).
