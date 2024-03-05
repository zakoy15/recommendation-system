# Final Project Report Recommendation System - Puadi Zakiy
---
## Project Overview
<p align="justify">Sistem rekomendasi untuk brand di Ecommerce adalah sebuah sistem rekomendasi di mana kita dapat merekomendasikan suatu brand/produk yang serupa kepada user
berdasarkan prefensi dan interaksi mereka masing-masing. Dengan sistem rekomendasi, dapat dengan mudah bagi user untuk mencari brand/produk sesuai keinginan mereka.
Sedangkan untuk penjual, brand/produk mereka dapat dilihat atau direkomendasikan langsung kepada user tanpa harus bersusah payah. Dan juga, dapat meningkatkan user experience
sehingga juga dapat meningkatkan profit. <br>
  
# Objective
<p align="justify">Merekomendasikan produk dari brand tertentu berdasarkan prefensi brand yang disukai user, sehingga dapat mempermudah serta meningkatkan user experience.
Dengan membangun beberapa sistem rekomendasi, yaitu content-based filtering, collaborative filtering, dan K-NN. Sehingga dapat mempermudah konsumen untuk membandingan 
serta memilih produk/brand berdasarkan prefensi personal. <br>

# Problem Ideas
* Persebaran produk/brand termahal dan termurah
* Bagaimana persebaran harga?
* Bagaimana persebaran brand yang ada?

# Goals
* Melihat persebaran harga dan brand yang ada
* Membuat sistem rekomendasi berdasarkan deskripsi produk, antaruser, dan rating.

# Data Understanding and Preparation
Sebelum memulai membuat sistem rekomendasi, dataset harus terlebih dahulu dicek, apakah ada data duplicate, missing value, ataupun data type yang tidak sesuai.
Setelah itu, harus dilakukan transformasi data agar dapat diproses ke sistem rekomendasi. 
[Dataset](https://www.kaggle.com/datasets/shivamb/fashion-clothing-products-catalog/data)

## Kolom pada dataset: <br>
  **ProductID** <br>
  Kode unik untuk setiap produk dari setiap brand. Setiap kode mewakili satu produk yang ada. <br>
  **ProductName** <br>
  Nama produk dari setiap brand. <br>
  **ProductBrand** <br>
  Nama sebuah brand dari suatu produk. <br>
  **Gender** <br>
  Jenis kelamin dari user yang membeli suatu produk/brand pada e-commerce. <br>
  **Price (INR)** <br>
  Harga perproduk dalam mata uang India. <br>
  **NumImages** <br>
  Gambar produk yang tersedia/ditampilkan di E-commerce. <br>
  **Description** <br>
  Penjelasan detail dari sebuah produk yang ada. <br>
  **PrimaryColor** <br>
  Warna utama pada suatu produk. <br>

  ## Data Overview
  Melihat dataset: <br>
  ![image] ()

  
