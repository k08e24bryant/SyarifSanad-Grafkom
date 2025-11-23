# SyarifSanad-Grafkom

**Nama:** Syarif Sanad  
**NRP:** 5025221257  
**Mata Kuliah:** Grafika Komputer

-----

## Case Study: Personalized Glyph Rendering

Proyek ini adalah implementasi rendering objek 3D interaktif berbasis Web menggunakan **WebGL** dengan bantuan library **Three.js**. Proyek ini memvisualisasikan inisial nama dan digit terakhir NRP saya ke dalam ruang 3 dimensi dengan gaya geometris modern.

### Identifikasi Karakter

Sesuai aturan studi kasus, karakter yang dirender diambil dari data berikut:

  * **Nama Depan:** **Sy**arif $\rightarrow$ Huruf **"Sy"**
  * **NRP:** 502522125**7** $\rightarrow$ Angka **"7"**

### Hasil Render

Berikut adalah tampilan hasil rendering 3D dari glyph yang telah diimplementasikan:
<img width="1289" height="935" alt="image" src="https://github.com/user-attachments/assets/e1c5ee86-0034-45cc-9da3-7513a0664c73" />


### Implementasi & Fitur Teknis

Dalam implementasi ini, saya menggunakan teknik-teknik dasar Grafika Komputer sebagai berikut:

1.  **Geometri Primitif (Primitives Construction)**

      * Karakter tidak di-*load* dari file model 3D, melainkan disusun secara manual (*hard-coded*) menggunakan bentuk dasar.
      * **Huruf 'S':** Disusun menggunakan gabungan `BoxGeometry` (balok) yang diposisikan vertikal dan horizontal.
      * **Huruf 'y':** Disusun menggunakan `CylinderGeometry` dengan rotasi sudut tertentu untuk membentuk percabangan.
      * **Angka '7':** Gabungan `BoxGeometry` dengan manipulasi rotasi untuk memiringkan kaki angka.

2.  **Transformasi Geometris**

      * **Translation (Pergeseran):** Mengatur posisi (`position.set`) setiap karakter agar tertata rapi dalam satu *scene*.
      * **Rotation (Perputaran):** Menerapkan rotasi pada sumbu Y untuk memberikan animasi dinamis pada objek.
      * **Scaling (Penskalaan):** Objek angka "7" diberikan skala (`scale`) lebih besar untuk menonjolkan variasi visual.

3.  **Pencahayaan & Material (Lighting & Shading)**

      * Menggunakan `MeshStandardMaterial` agar objek bereaksi realistis terhadap cahaya (memiliki bayangan dan *highlight*).
      * Sistem pencahayaan menggunakan **Ambient Light** (cahaya dasar) dan **Directional Light** (cahaya utama) untuk menciptakan dimensi dan bayangan (*shadow*).

4.  **Interaksi (User Interaction)**

      * Menggunakan **OrbitControls** yang memungkinkan pengguna untuk memutar kamera 360 derajat, melakukan *zoom in/out*, dan menggeser pandangan di sekitar objek.

### Teknologi

  * **Language:** JavaScript (ES6)
  * **Library:** Three.js (WebGL Framework)
  * **Environment:** Web Browser

-----

