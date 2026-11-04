SAKURA AUTO DRAMA - PROYEK ANDROID (VERSI AWAL)
================================================

Yang tersedia pada versi awal:
- Aplikasi Android native, bukan HTML.
- Memilih video gameplay dari penyimpanan menggunakan pemilih dokumen Android.
- Pilihan tema cerita dan nama karakter.
- Membuat enam bagian cerita/dialog/subtitle sebagai naskah teks.
- Pratinjau voice-over menggunakan Text-to-Speech Android, jika mesin suara tersedia.

Yang BELUM tersedia:
- Belum merender/mengekspor video hasil edit.
- Subtitle belum dibakar ke dalam video.
- Voice-over belum digabungkan ke file video.
- Belum ada musik latar otomatis.

Cara membuka proyek:
1. Instal Android Studio di Windows.
2. Ekstrak ZIP ini ke folder biasa, misalnya C:\SakuraAutoDrama.
3. Buka Android Studio > Open > pilih folder SakuraAutoDrama.
4. Tunggu Gradle Sync selesai. Koneksi internet dibutuhkan saat pertama kali mengunduh Gradle/plugin.
5. Jika diminta, gunakan JDK yang disarankan Android Studio (JDK 17).
6. Untuk mencoba di HP: aktifkan Developer options dan USB debugging, sambungkan HP dengan kabel USB, lalu tekan Run.
7. Untuk membuat APK: Build > Build Bundle(s) / APK(s) > Build APK(s).
8. Setelah selesai, pilih Locate pada notifikasi untuk menemukan APK.

Persyaratan:
- Windows 10 64-bit direkomendasikan.
- Android Studio versi stabil terbaru.
- RAM PC 8 GB dapat digunakan, tetapi Gradle build bisa lambat jika banyak aplikasi terbuka.
- Android minSdk 23.

Penting:
Ini adalah proyek sumber yang bisa dibuka dan dibangun di Android Studio, bukan APK siap instal.
Silakan uji di HP sendiri. Pemilihan suara pria/wanita hanya memilih suara yang tersedia di mesin TTS; beberapa HP mungkin tidak menyediakan pilihan suara gender yang jelas.

CARA MEMBANGUN APK TANPA KOMPUTER (GITHUB ACTIONS)
==================================================
Pilihan ini membangun APK di server cloud; HP hanya dipakai untuk mengunggah proyek dan mengunduh hasil.

1. Buat akun atau masuk ke https://github.com lewat browser HP.
2. Buat repository baru bernama SakuraAutoDrama. Pilih Public agar langkah awal lebih sederhana; jangan unggah file pribadi.
3. Ekstrak ZIP di HP menggunakan pengelola file.
4. Upload semua isi folder proyek ke repository GitHub, termasuk folder tersembunyi .github/workflows/build-apk.yml.
   Catatan: beberapa aplikasi file manager menyembunyikan folder .github; pastikan file workflow ikut terunggah.
5. Buka tab Actions di repository dan pilih workflow "Build Sakura Auto Drama APK".
6. Tekan Run workflow. Tunggu hingga selesai.
7. Buka hasil run yang sukses, cari bagian Artifacts, unduh SakuraAutoDrama-debug-apk.zip.
8. Ekstrak ZIP tersebut untuk mendapatkan app-debug.apk, lalu ketuk APK untuk memasangnya. Jika Android meminta izin, izinkan pemasangan dari browser/file manager yang digunakan.
9. Jika build gagal, buka log build dan kirim screenshot pesan error.

Catatan: APK debug untuk pengujian, bukan rilis Play Store. Proyek saat ini masih versi awal; belum menggabungkan subtitle/voice-over ke video hasil akhir.
