Nama : Nelil Amaani
NPM : 2306227835
Kelas : PBP B

1. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial)
1.) Membuat sebuah proyek Django baru
dalam hal ini saya membuat program Django bernama plantshop yang berada pada subdirektori bernama plantshop. keduanya saya hubungkan dengan repository di GitHub untuk memudahkan version control
2.)  Membuat aplikasi dengan nama main pada proyek tersebut
saya menambahkan menambahkan aplikasi main ke dalam proyek dengan melakukan perintah di CMD python manage.py startapp main. Main kemudian didaftarkan ke dalam file setting.py proyek dibawah INSTALLED_APPS agar terhubung dengan proyek utama.
3.)  Melakukan routing pada proyek agar dapat menjalankan aplikasi main.
agar dapat menjalankan aplikasi main, saya menambahkan file urls.py dalam proyek utama dan menambahkan rute untuk mengarahkan URL ke aplikasi main.
from django.urls import include, path

urlpatterns = [
    path('main/', include('main.urls')),  # Mengarahkan ke aplikasi main
]
4.) Membuat Model Product pada Aplikasi main
pada file models.py dalam aplikasi main, saya mendefinisikan Product dengan atribut name, prive, dan description. Model ini akan digunakan untuk mempresentasikan produk dalam database.
5.) Membuat Fungsi di views.py untuk Menampilkan Data di Template
membuat fungsi show_info di file views.py yang dapat mengembalikan informasi nama aplikasi, nama, dan kelas. Fungsi tersebut akan mengembalikan data ke dalam file template main.html
6.) Membuat Routing di urls.py Aplikasi main
Membuat file urls.py dalam aplikasi main dan menambahkan rute untuk memetakan show_info yang telah di buat dalam file views.py
7.) Melakukan Deployment ke PWS
Setelah aplikasi selesai saya melakukan deployment ke platform PWS . saya memastikan agar aplikasi dapat diakses melalui URL yang telah disediakan PWS.
8.) Membuat README.md
saya membuat file README.md yang berisi:
Tautan menuju aplikasi yang sudah di-deploy di PWS.
Penjelasan tentang bagaimana cara saya mengimplementasikan checklist di atas secara step-by-step.
Jawaban atas beberapa pertanyaan terkait

2. Buatlah bagan yang berisi request client ke web aplikasi berbasis Django beserta responnya dan jelaskan pada bagan tersebut kaitan antara urls.py, views.py, models.py, dan berkas html.
client melakukan request ->  urls.py (mencocokan URL) -> views.py (menjalankan logika aplikasi) -> models.py (mengambil data dari database) -> views.py (memproses data) -> Template (main.html) -> Respons kembali ke client

3. Jelaskan fungsi git dalam pengembangan perangkat lunak!
1.) Git memfasilitasi berkolaborasi dengan banyak pengembang yang bekerja dalam proyek yang sama tanpa saling menggangu.
2.) Git memudahkan pengembang untuk melacak perubahan kode yang terjadi seiring waktu.
3.) Git dapat menjadi backup dan dapat melakukan pemulihan dengan mudah, karena perubahan kode disimpan pada lokal dan disinkronkan ke repositori jarak jauh seperti GitLab atau GitHub.
4.) Git memberikan riwayat perubahan dan transparansi mengenai siapa dan kapan yang melakukan perubahan kode.

4. Menurut Anda, dari semua framework yang ada, mengapa framework Django dijadikan permulaan pembelajaran pengembangan perangkat lunak?
1.) Django memiliki dokumentasi yang lengkap dan dapat dengan mudah dipahami oleh pemula.
2.) Django dibangun dengan bahasa python, bahasa yang mudah untuk dipelajari, yang membuat  ideal untuk pengembangan web.
3.) Django dapat mengembangkan aplikasi mulai dari yang sederhana maupun kompleks.
4.) Django menerapkan pola MVT (Model-View-Template) yang dapat memudahkan pengembang logika aplikasi, data, dan tampilan dalam struktur yang terorganisir.
5.) Django dilengkapi fitur keamanan bawaan yang memiliki perlindungan yang kuat seperti CSRF, SQL injection, dan XSS dll.
6.) Django merupakan salah satu framework yang banyak digunakan di seluruh dunia, sehingga memudahkan menemukan tutorial, forum/komunitas, dan bantuan ketika menemui masalah.

5. Mengapa model pada Django disebut sebagai ORM?
model pada Django disebut sebagai ORM (Object-Relational Mapping) karena model tersebut menggunakan pendekatan pemetaan object python ke dalam struktur basis data relasional, sehingga memungkinkan developer untuk berinteraksi dengan basis data dengan menggunakan object python tanpa perlu membuka SQL secara langsung.