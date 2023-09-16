# GL_tools
kembangkan ya cuk, jan cuma make doang

# OpenGL Object Manager

OpenGL Object Manager adalah pustaka Python yang dirancang untuk mengelola objek dalam tampilan OpenGL. Ini memungkinkan Anda membuat, mengatur, dan menggambar berbagai objek seperti persegi panjang, lingkaran, segitiga, titik, poligon, dan garis dalam tampilan OpenGL Anda. Berikut adalah cara menggunakan dan mengintegrasikan pustaka ini ke dalam proyek OpenGL Anda.

## Instalasi

Untuk menggunakan OpenGL Object Manager, Anda memerlukan PyOpenGL. Jika Anda belum menginstalnya, Anda dapat menonton tutorial video berikut : https://www.youtube.com/watch?v=a4NVQC_2S2U


Setelah Anda menginstal PyOpenGL, Anda dapat mengimpor `GL_tools` ke dalam proyek Anda.

## Penggunaan

### Membuat dan Mengatur Objek

Berikut adalah cara membuat objek-objek yang berbeda menggunakan `GL_tools`:

```python
from GL_tools import *

# Inisialisasi OpenGLInitializer
initializer = OpenGLInitializer()
initializer.initialize_window()

# Membuat dan menambahkan objek persegi panjang
initializer.object_manager.create_rectangle(-0.5,-0.6,1,1,(0,1,0))
initializer.object_manager.create_rectangle(-0.8,-0.7,1,1,(1,0,0))

# Membuat dan menambahkan objek lingkaran
initializer.object_manager.create_circle(0,0,1,(0,0,1))

# Membuat dan menambahkan objek segitiga
initializer.object_manager.create_triangle(x=0.0, y=0.0, side_length=0.2, color=(0.0, 1.0, 0.0))

# Membuat dan menambahkan objek titik
initializer.object_manager.create_point(x=0.1, y=0.1, color=(1.0, 1.0, 1.0))

# Membuat dan menambahkan objek poligon
vertices = [(0.0, 0.0), (0.2, 0.0), (0.1, 0.2)]
initializer.object_manager.create_polygon(vertices, color=(1.0, 0.5, 0.0))

# Membuat dan menambahkan objek garis
initializer.object_manager.create_line(x1=0.0, y1=0.0, x2=0.2, y2=0.2, color=(0.5, 0.5, 0.5))


Pastikan Anda memiliki berkas README ini dalam direktori proyek Anda agar pengguna lain dapat dengan mudah memahami cara menggunakan `ObjectManager` yang Anda buat. Selain itu, pastikan juga untuk menambahkan detail kontak atau cara berkontribusi jika Anda ingin menerima kontribusi dari pengguna lain.
