# Deep_learning_autoencoder
Dataset : Diambil dari celebrity face image dataset di kaggle saya ambil 30 gambar wajah

Arsitektur Autoencoder;
Encoder : 
 - Input gambar berupa RGB berukuran (3,256,256))
 - Setiap layer menggunakan Conv2D, kernel 3x3 stride 2 padding 1
 - perubahan ukuran setiap feature map nya
     (3,256,256) --> (64,128,128)
     (64,128,128) --> (128,64,64)
     (128,64,64) --> (256,32,32)
   dengan hasil akhir 256 channel berukuran 32 x 32

Decoder : 
- Menggunakan  ConvTranspose2D
- Setiap layer menggunakan Conv2D, kernel 3x3 stride 2 padding 1
- perubahan ukuran setiap feature map nya
  (256, 32, 32) → (128, 64, 64)
  (128, 64, 64) → (64, 128, 128)
  (64, 128, 128) → (3, 256, 256)

  performa (loss): 

  


   



