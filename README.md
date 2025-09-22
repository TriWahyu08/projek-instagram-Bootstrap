# **Pertanyaan README:**
# **1. Mengapa Saya Memilih Konfigurasi col Tertentu untuk Setiap Breakpoint?**
Pendekatan yang saya gunakan untuk tata letak postingan adalah desain responsif. Saya memilih kombinasi kelas col-12, col-md-4, dan col-lg-3 untuk memastikan tampilan yang optimal di berbagai perangkat, dari ponsel hingga desktop.

### - **col-12:**
Di layar kecil, seperti ponsel, saya ingin setiap gambar tampil besar dan jelas, mengisi seluruh lebar layar. Itulah mengapa saya menggunakan col-12, yang berarti setiap gambar akan mengambil 12 dari 12 kolom yang tersedia. Ini memberikan pengalaman yang fokus dan tidak membuat mata lelah.

### - **col-md-4:**
Saat lebar layar bertambah ke ukuran tablet (breakpoint md), saya ingin halaman terlihat lebih rapi dengan menampilkan lebih banyak konten. Dengan col-md-4, setiap gambar hanya mengambil 4 dari 12 kolom, sehingga otomatis membentuk tata letak 3 gambar per baris.

### - **col-lg-3:** 
Untuk layar desktop yang lebar (breakpoint lg), saya memaksimalkan ruang dengan mengubah tata letak menjadi 4 gambar per baris menggunakan col-lg-3. Ini membuat tampilan profil sangat mirip dengan Instagram versi web dan memanfaatkan ruang kosong dengan efisien.
Dengan cara ini, saya tidak perlu membuat tiga halaman berbeda untuk setiap perangkat. Kode HTML yang sama secara cerdas menyesuaikan diri berkat sistem grid Bootstrap.

# **2. Bagaimana Saya Memastikan Tombol "Edit Profil" Tetap Mudah Diakses di Mobile?**
Saya memastikan tombol "Edit profil" dan "Bagikan profil" tetap ramah sentuhan di perangkat mobile dengan dua pendekatan utama:

### - **Ukuran Penuh (d-grid):**
Dengan menerapkan kelas d-grid pada kolom induk tombol, saya memastikan tombol-tombol tersebut secara otomatis memanjang hingga mengisi seluruh lebar layar saat berada di perangkat mobile. Ini membuat area kliknya lebih besar dan mudah dijangkau oleh jari.

### - **Perubahan Urutan (order-*):**
Saya menggunakan kelas order-md-1, order-md-2, dan order-md-3. Ini adalah trik cerdas yang memungkinkan saya mengubah urutan tombol saat layar membesar. Di layar mobile, tanpa kelas md yang aktif, tombol-tombol tersebut akan muncul secara vertikal satu per satu, yang lebih baik untuk navigasi. Namun, saat layar mencapai ukuran md atau lebih, mereka akan berbaris berdampingan.
Kombinasi ini membuat tata letak tombol fleksibel dan fungsional, beradaptasi dengan mulus dari tampilan vertikal di ponsel ke tampilan horizontal di desktop.

# **3. Jika Postingan Bertambah Jadi 50, Apa Potensi Masalah dan Bagaimana Solusi Grid Saya Mengatasinya?**

- Jika postingan bertambah menjadi 50, masalah utama yang akan muncul adalah performa dan waktu muat halaman. Memuat 50 gambar sekaligus bisa membuat halaman terasa berat dan lambat, terutama bagi pengguna dengan koneksi internet yang tidak stabil.

- Dari sisi tata letak, grid yang saya buat sudah siap mengatasinya. Konfigurasi col-12 col-md-4 col-lg-3 akan secara otomatis menyusun semua 50 gambar dengan rapi, menyesuaikan jumlah gambar per baris sesuai dengan lebar layar. Tampilan tidak akan berantakan dan akan tetap konsisten.

#### Namun, untuk mengatasi masalah performa, solusi grid saja tidak cukup. perlu menambahkan teknik lain:
### - **Lazy Loading**: 
Saya akan mengimplementasikan "lazy loading," di mana gambar-gambar hanya akan dimuat saat pengguna menggulir halaman hingga gambar tersebut terlihat. Ini akan sangat mengurangi beban awal saat halaman pertama kali dibuka, karena hanya beberapa gambar pertama yang perlu diunduh.

### - **Optimasi Gambar**: 
Saya juga akan memastikan setiap gambar dioptimalkan, yaitu dikompresi ke ukuran file terkecil tanpa mengurangi kualitas visual secara signifikan.

# **📱Proyek Profil Instagram Sederhana**
Proyek ini adalah halaman profil Instagram yg sederhana, yang dibuat menggunakan HTML dan CSS, dengan bantuan kerangka kerja Bootstrap 5. Tujuannya adalah untuk mendemonstrasikan komponen Bootstrap dan belajar cara membuat halaman web yang terlihat bagus dan rapi,layout responsif serta styling kustom di semua perangkat, baik di ponsel maupun di layar komputer.

# **📂 Struktur file**

- ## 📁assets/
ada:
- ### 📁css/ 🗃️bootstrap_profil_ig.css
- ### 📁img/ (foto_profil (dan gambar-gambar postingan lainnya))
- ## 🗃️index.html

- **index.html:** Ini adalah 'otak' dari halaman, di mana semua konten seperti foto profil, termasuk header, bio, sorotan (highlights), dan postingan disusun rapi.

- **assets/css/bootstrap_profil_ig.css:** Di sini saya menambahkan beberapa sentuhan personal, seperti mengatur warna latar belakang hitam dan warna teks putih agar tampilannya mirip Instagram.dll.

- **assets/img/:** Di sinilah semua foto tersimpan.

# **▶️ Cara Menjalankan**
karena tidak perlu instal apa-apa atau pakai program khusus, jadi menjalankannya cukup mudah:

1. Pastikan semua folder dan file berada di tempatnya, (terutama file HTML dan CSS di folder assets) berada dalam struktur yang benar.

2. Langsung saja buka file index.html menggunakan browser Anda (seperti Google Chrome, Edge atau Firefox). Halaman profil akan langsung muncul.

# **📦 Dependensi**
Proyek ini menggunakan beberapa pustaka eksternal yang dimuat dari CDN (Content Delivery Network). jadi tidak perlu menginstal apa pun secara lokal.

### - Bootstrap 5.3.3:
- Digunakan untuk sistem grid responsif, komponen navbar, tombol, dan tab.

- Link CSS: https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css

- Link JS: https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js

### - Font Awesome 6.0.0-beta3:
- Ini cuma untuk 'mempercantik' halaman. Digunakan untuk ikon-ikon seperti gembok, tanda plus, ikon at, dan ikon feed.

- Link CSS: https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all
