# Pok-mon-Text-to-Image

Laporan Tugas: Implementasi Generative Model (Pokémon Text-to-Image)
Proyek ini mendemonstrasikan pembuatan model AI generatif sederhana untuk membangkitkan gambar berdasarkan deskripsi teks (prompt). Dataset yang digunakan adalah kumpulan gambar Pokémon beserta keterangannya.

👥 Identitas Mahasiswa

Nama: Putri Regina 

NIM: 41236774

Kelas: TI KIP P3

📋 Deskripsi Proyek
Proyek ini menggunakan arsitektur Transformer untuk mempelajari hubungan antara deskripsi tekstual (caption) dengan representasi visual (visual tokens). 

1. Dataset & Preprocessing

Sumber Data: Dataset reach-vb/pokemon-blip-captions yang dimuat melalui library datasets. 


Vektorisasi Teks: Menggunakan TextVectorization untuk mengubah caption menjadi angka dengan maksimal 5000 kata unik. 


Preprocessing Gambar: Gambar Pokémon diubah ukurannya menjadi 64x64 piksel dan dinormalisasi agar dapat diproses oleh model. 

2. Arsitektur Model

Transformer: Dibangun untuk memprediksi token visual secara autoregresif berdasarkan input teks. 


Pelatihan (Training): Model dilatih selama 20 epoch dengan pengoptimal Adam (learning rate 1e-4). 


Loss Function: Menggunakan sparse_categorical_crossentropy untuk menghitung tingkat kesalahan prediksi model. 

3. Hasil Generasi
Berdasarkan pengujian akhir dengan prompt "a pink cute pokemon", model berhasil membangkitkan representasi visual awal. Karena pelatihan dilakukan dalam skala kecil dan cepat, hasil gambar yang muncul saat ini masih berupa noise visual/abstrak sebagai bukti bahwa alur kerja model sudah berjalan. 

<img width="328" height="350" alt="image" src="https://github.com/user-attachments/assets/4275bef9-34ec-419e-83d6-c1be9854723c" />


