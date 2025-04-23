# Deep_learning_autoencoder
Dataset : Diambil dari foto saya sendiri, lalu di augmentasi secara random sebesar 20 derajat.

Arsitektur Autoencoder;
Encoder : 
 - Input gambar berupa RGB berukuran (3,256,256))
 - Setiap layer menggunakan Conv2D, kernel 4x4 stride 2 padding 1
 - perubahan ukuran setiap feature map nya
     (3,256,256) --> (64,128,128)
     (64,128,128) --> (128,64,64)
     (128,64,64) --> (256,32,32)
   dengan hasil akhir 256 channel berukuran 32 x 32

Decoder : 
- Menggunakan  ConvTranspose2D
- Setiap layer menggunakan Conv2D, kernel 4x4 stride 2 padding 1
- perubahan ukuran setiap feature map nya
  (256, 32, 32) → (128, 64, 64)
  (128, 64, 64) → (64, 128, 128)
  (64, 128, 128) → (3, 256, 256)

  performa (loss): setelah 20 epoch performa loss nya sebesar 0.0079, model belajar dengan baik dan hasil rekonstruksi masih belum mendekati target.

  


   



