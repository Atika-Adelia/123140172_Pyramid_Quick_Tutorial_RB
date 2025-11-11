# Analisis Folder 04 : folder debugtoolbar (NIM : 123140172)

Percobaan keempat ini berpusat pada dua konsep arsitektur penting untuk pengembangannya, yaitu pemasangan add-on dan manajemen dependensi development. Pertama, pyramid_debugtoolbar diinstal sebagai add-on yang tidak memerlukan modifikasi kode Python inti (__init__.py). Sebaliknya, ia diaktifkan  dengan menambahkan nama paketnya ke dalam pengaturan pyramid.includes di file development.ini. Metode ini memudahkan untuk mengaktifkan atau menonaktifkan fitur penting (toolbar) hanya dengan mengedit file konfigurasi, yang menunjukkan manfaat memisahkan konfigurasi dari kode aplikasi.

Kemudian yang kedua, percobaan ini juga menjelaskan praktik Setuptools Extras dengan tag dev. Dibandingkan dengan menambahkan pyramid_debugtoolbar ke dependensi wajib (install_requires), paket ini dikelompokkan sebagai dependensi opsional yang hanya dibutuhkan untuk debugging lokal. Lalu, untuk instalasinya, percobaan ini menggunakan perintah $VENV/bin/pip install -e ".[dev]", yang secara eksplisit memuat paket tambahan ini. Dengan demikian, intinya pada percobaan keempat ini menunjukkan bagaimana aplikasi Pyramid dapat diperkaya dengan tool pihak ketiga secara terstruktur, serta memisahkan kebutuhan pengembangan dari kebutuhan produksinya. 

Tampilan di localhost 

<img src="gambar_04.png" alt="Tampilan Hello World" width="600"/>