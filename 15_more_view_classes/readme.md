# Analisis Folder 15 : folder more view classes (NIM : 123140172)

*We have a home view available at http://localhost:6543/ with a clickable link to the hello view*. Berikut adalah tampilannya saat membuka localhost:6543

<img src="gambar_15_5.png" alt="Hasil di localhost:6543"/>

Percobaan kelima belas ini menerapkan dua teknik refactoring lanjutan, yang pertama adalah penggunaan decorator @view_defaults pada view class, secara signifikan mengurangi kode berulang yang sebelumnya mencemari setiap metode. Kedua, percobaan ini memperkenalkan Templating Inheritance (pewarisan template) untuk mengatasi redundansi HTML. Daripada mengulang markup dasar (<html>, <head>, header, footer) di setiap file template individual, membuat layout master (misalnya, layout.jinja2) yang berisi semua struktur HTML umum dan menggunakan Jinja2 blocks ({% block content %}) sebagai placeholder. View template spesifik kemudian mewarisi struktur ini dengan menggunakan tag {% extends "layout.jinja2" %} dan hanya mengisi konten unik mereka di dalam block yang relevan. Refactoring ini memastikan bahwa layout situs Anda konsisten, dan perubahan desain global—seperti memperbarui CSS atau JavaScript—hanya perlu dilakukan sekali pada file. 

Secara keseluruhan, Percobaan 15 ini bukan tentang menambah fungsionalitas baru, melainkan tentang meningkatkan skalabilitas view dan templating aplikasi. Berikut adalah tampilan hasil test dan di localhost : 

Tampilan hasil run the test : 

<img src="gambar_15_1.png" alt="Hasil 2 passed"/>

Tampilan di http://localhost:6543/howdy/jane/doe, 

tampilan saat edit : 

<img src="gambar_15_2.png" alt="Hasil di http://localhost:6543/howdy/jane/doe" />

tampilan hasil edit  : 

<img src="gambar_15_3.png" alt="Hasil di localhost:6543/howdy" width="600"/> 

tampilan saat delete : 

<img src="gambar_15_4.png" alt="Hasil di localhost:6543/howdy" width="600"/> 
