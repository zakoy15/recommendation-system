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
  * Melihat dataset: <br>
  ![image](https://github.com/zakoy15/recommendation-system/assets/143687145/3d997740-1b09-4cfb-ae2f-637a103aa237) <br>

  * Mengatasi Missing Value: <br>
    ![image](https://github.com/zakoy15/recommendation-system/assets/143687145/b729b6c0-485c-4aad-82a6-b7a92109a65a) <br>
    dikarenakan terdapat missing value pada kolom primary color, maka akan diganti dengan nilai yang paling sering muncul (blue) <br>

    ![image](https://github.com/zakoy15/recommendation-system/assets/143687145/cf568a64-f95d-484e-8b41-c6f2d448966d) <br>
    setelah mengganti missing value <br>
    
Pada proses pembuatan sistem rekomendasi kolom yang digunakan adalah ProductID, ProductName, ProductBrand, Price (INR), dan Description.

# Eksplonatory Data Analytics
* 10 Brand terbanyak didominasi oleh brand-brand fashion.
![image](https://github.com/zakoy15/recommendation-system/assets/143687145/990f2f83-5af8-4332-969c-c9ccd302a0dd)
Brand indian terrain merupakan brand yang paling diminati, maka akan lebih baik untuk brand ini selalu ready stock dan menjaga kualitas serta performanya,
untuk menjaga loyalitas user yang sudah ada. <br>

* 10 Produk Paling Banyak Diminati di Ecommerce
  ![image](https://github.com/zakoy15/recommendation-system/assets/143687145/86590847-a24a-457f-a81c-dbe5e31053c5)
  Untuk 10 produk yang paling banya diminati, dapat disediakan dalam berbagai ukuran yang ready stock. Sehingga user tidak perlu menunggu. Sedangkan, untuk produk yang masih
  kurang peminat, dapat memberlakukan promo atau product bundling, sehingga dapat meningkatkan daya beli produk/brand dan menghasilkan revenue. <br>

* Persebaran section Produk <br>
  ![Image](https://github.com/zakoy15/recommendation-system/assets/143687145/565d11a8-f3f3-45ab-aa49-b8f44bcb7684)
  Untuk persebaran section product, didominasi oleh section Women, disusul Men dan Unisex.
  Kebanyakan pembeli di Ecommerce adalah wanita, sehingga untuk section women dan men dapat terus dijaga untuk stock nya, jika bisa ditambah variasi/style nya agar user
  tidak jenuh.
  Dan untuk unisex kid dan girls, karena peminatnya sedikit, dapat diatur pendistribusiannya di ecommerce dan dapat dilakukan promo/bundling dengan produk2 section women
  atau men.

* 10 Brand dan Produk dengan harga tertinggi didominasi oleh brand/produk gadget/aksesoris. <br>
  ![Image](https://github.com/zakoy15/recommendation-system/assets/143687145/7c0ab1d9-fb3e-4070-84e5-91e16795c569) <br>
  ![image](https://github.com/zakoy15/recommendation-system/assets/143687145/0ac7b9c0-b4a6-42db-9a04-3b3819a351ed) <br>
  brand/produk gadget dan aksesoris, kurang diminati oleh user. Dikarenakan harga yang mahal sehingga user lebih memilih untuk langsung ke toko dibanding online. <br>
  Ecommerce dapat membuat imbauan/campaign untuk meyakinkan user atau memberikan jaminan, bahwa membeli produk gadget/aksesoris di platform mendapatkan asuransi keamanan,
  baik jika barang itu hilang, terdapat scam ataupun rusak saat pengiriman. <br>

* 10 Brand dengan harga terendah didominasi oleh brand/produk skincare. <br>
  ![image]("https://github.com/zakoy15/recommendation-system/assets/143687145/ae0c58e4-7d61-49d8-990d-e2f938f02712) <br>
  ![image](https://github.com/zakoy15/recommendation-system/assets/143687145/cad9a3f2-6072-426d-b0ac-731fa093d4bc) <br>
  ntuk brand skincare/bodycare, dapat fokus pada pembuatan campaign-campaign yang lebih menonjolkan manfaat dan keuntungan dari brand tersebut. Serta, menjaga loyalitas
  user, seperti memberikan promo kepada user yang sudah lama menggunakan suatu brand/membership. Dan dapat juga melakukan penawaran bundling. <br>

* Persebaran Harga <br>
  ![image](https://github.com/zakoy15/recommendation-system/assets/143687145/0e6f92d4-dff6-43aa-a75b-b26b113c606d) <br>
  Distribusi harga didominasi dengan produk/brand di <3000 INR <br>
  Kebanyakan user, lebih memilih produk/brand yang masih affordable atau <3000 INR. yang berati prefensi user terhadap harga lebih condong untuk membeli yang murah.
  Ecommerce dapat melakukan campaign besar, seperti tanggal kembar, hari nasional tertentu dll. Untuk memberi promo ke harga-harga yg di atas 3000 INR untuk menarik user.
  
# Sistem Rekomendasi
## Content-based Filtering

![image](https://github.com/zakoy15/recommendation-system/assets/143687145/e9a1d6dc-42aa-4902-858a-7a4e561aec47) <br>
Dengan rekomendasi sistem yang menggunakan metode content-based filtering dapat menghasilkan nama-nama brand yang memiliki kesamaan dari sisi deskripsi yang ada pada
dataset, sehingga user mendapatkan rekomendasi sesuai prefensinya sendiri. 

Contoh seperti di atas, ketika user mencari brand “Mochi” maka akan muncul juga produk/brand yang hampir serupa dengan brand “Mochi”.

## Collaborative Filtering

![image](https://github.com/zakoy15/recommendation-system/assets/143687145/bcb9fa9f-1ee9-4013-8b70-3bd182cc5b92) <br>
Pada metode CF ini, hanya beberapa kolom yang digunakan, yaitu kolom id, ClothingID, dan rating. 

![image](https://github.com/zakoy15/recommendation-system/assets/143687145/46ef3799-e8da-400b-b38b-47f953adf4b5) <br>
Setelah itu melakukan train dan test dari variabel yang sudah dibuat. <br>

![image](https://github.com/zakoy15/recommendation-system/assets/143687145/4e024909-5879-4209-bf55-159edcbc7847) <br>
Setelah melakukan train dan test, selanjutnya ke pemodelan. Di sini, menggunakan SVD. <br>

![image](https://github.com/zakoy15/recommendation-system/assets/143687145/cddfd3f3-1178-499e-b4b7-cc1e1a2ad5c1) <br>
Dari hasil prediksi di atas, memungkinkan untuk merekomendasikan produk dengan `id=1081` kepada `user id 21213`

## K-NN

![image](https://github.com/zakoy15/recommendation-system/assets/143687145/5392513d-561c-4bbc-b0f9-48b18b9caf62) <br>
Di atas adalah hasil data yang telah melalui preprocessing. 
Pada metode ini, menggunakan 2 kolom, yaitu class name dan rating. <br>

```
def product_recommended(class_name=list(fashion2['Class Name'].value_counts().index)):
  class_list_name = []
  item_id = fashion2[fashion2['Class Name']==class_name].index
  item_id = item_id[0]
  for new_id in idlist[item_id]:
    class_list_name.append(fashion2.loc[new_id]['Class Name'])
  return class_list_name

product_recommended('Jeans')
```

Dengan metode K-NN, dapat menampikan produk yang berdasarkan tingkat kesamaan produk satu dengan lainnya dari pencarian produk yang paling sering dicari oleh user
yang berdasarkan rating. 

contoh, ketika user ingin mencari kategori `Jeans` maka akan muncul rekomendasi `Knits`


  



  
