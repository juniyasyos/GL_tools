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

#Di akhir kode jalankan
glutMainLoop()
```


### Membuat dan Mengatur Objek
```python
Terdapat penggunaan color tamplate berupa dictionary tuple
colors = {
        '--Red': (255, 0, 0),
        '--Green': (0, 255, 0),
        '--Blue': (0, 0, 255),
        '--Yellow': (255, 255, 0),
        '--Cyan': (0, 255, 255),
        '--Magenta': (255, 0, 255),
        '--White': (255, 255, 255),
        '--Black': (0, 0, 0),
        '--Gray': (128, 128, 128),
        '--Aqua': (0, 255, 255),
        '--Lime': (0, 255, 0),
        '--Navy': (0, 0, 128),
        '--Fuchsia': (255, 0, 255),
        '--Olive': (128, 128, 0),
        '--Teal': (0, 128, 128),
        '--Maroon': (128, 0, 0),
    }

#Penggunaannya
from GL_tools.GL_tools import *

def main():
    window = OpenGLInitializer(window_size=(1000,1000),window_title="Tugas Nama")
    window.initialize_window()
    window.object_manager.create_rectangle(100,100,50,100,color=colors['--Red'])
    window.object_manager.create_rectangle(150,100,50,100,color=colors['--White'])
    window.object_manager.create_rectangle(200,100,50,100,color=colors['--Green'])
    window.object_manager.create_rectangle(250,100,50,100,color=colors['--Blue'])
    window.object_manager.create_rectangle(300,100,50,100,color=colors['--Yellow'])
    window.object_manager.create_rectangle(350,100,50,100,color=colors['--Cyan'])
    window.object_manager.create_rectangle(400,100,50,100,color=colors['--Magenta'])
    window.object_manager.create_rectangle(450,100,50,100,color=colors['--Aqua'])
    window.object_manager.create_rectangle(500,100,50,100,color=colors['--Lime'])
    window.object_manager.create_rectangle(550,100,50,100,color=colors['--Navy'])
    window.object_manager.create_rectangle(600,100,50,100,color=colors['--Fuchsia'])
    window.object_manager.create_rectangle(650,100,50,100,color=colors['--Olive'])
    window.object_manager.create_rectangle(700,100,50,100,color=colors['--Teal'])
    window.object_manager.create_rectangle(750,100,50,100,color=colors['--Maroon'])
    glutMainLoop()
main()
```


Pastikan Anda memiliki berkas README ini dalam direktori proyek Anda agar pengguna lain dapat dengan mudah memahami cara menggunakan `ObjectManager` yang Anda buat. Selain itu, pastikan juga untuk menambahkan detail kontak atau cara berkontribusi jika Anda ingin menerima kontribusi dari pengguna lain.
