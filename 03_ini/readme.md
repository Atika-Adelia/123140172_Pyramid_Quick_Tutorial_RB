# Analisis Folder 03 : folder ini (NIM : 123140172)

Pada percobaan ketiga ini, pyramidnya sudah diatur melalui file development.ini melalui pserve. Jadi, di file bagian [app:main] merujuk ke entry point egg:tutorial di mana pserve akan menemukan dan memanggil fungsi main() (yang baru didefinisikan di __init__.py) untuk mengembalikan objek aplikasi WSGI yang sudah dikonfigurasi. Lalu, di bagian [server:main], mengkonfigurasi server Waitress, memindahkan pengaturan host dan port untuk keluar dari kode Python. 

Kemudian, pada percobaan ini juga menghapus app.py karena sudah dipindahkan ke fungsi main() di __init__.py. Terjadinya perubahan struktur itu menciptakan entry point yag dapat dipanggil oleh pserve. Dengan demikian, percobaan ketiga ini memastikan bahwa setiap perubahan kode yang disimpan maka akan secara otomatis memuat ulang aplikasinya. 

Tampilan di localhost 

<img src="gambar_03.png" alt="Tampilan Hello World" width="600"/>