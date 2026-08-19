# COMPREHENSIVE-FMCG-ANALYSIS


supported by :
<img src="https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=white" /> <img src="https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white" /> <img src="https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue" /> <img src="https://img.shields.io/badge/Sqlite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" /> <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" /> <img src="https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252" />


     
### **Executive Summary** 
  "Proyek analitik data menyeluruh yang berfokus pada analisis kinerja penjualan, efektivitas promosi, profitabilitas, dan faktor pendorong bisnis di industri FMCG."

### **Tahapan Tahapan project** :
* Data Extraction :
  Data didapatkan di website Kaggle <https://www.kaggle.com/datasets/atharvasoundankar/fmcg-sales-marketing-and-profit-data>, data diekstrak menggunakan bahasa pemrograman python dan dibersihkan dan diperiksa lebih lanjut granularitas datanya 
* Data Cleaning : data dibersihkan dari data duplikat dan null values, setelah diperhatikan tidak  ada duplikasi data dan null values yang akan berpengaruh negatif ke analisis
* Data Analysis : analisis yang dilakukan adalah eksploratory analysis dengan melakukan modeling data menggunakan query sql untuk mengetahui retensi pelanggan
### **Tahapan Tahapan Analisa** :
1. Analisa kinerja keseluruhan

-  Revenue meningkat 4% dibanding tahun sebelumnya
-  Profit naik 4.6%, sedangkan profit margin hanya naik 0.6%, mengindikasikan pertumbuhan profit berasal dari peningkatan volume penjualan, bukan peningkatan efisiensi.
-  Wholesale masih menjadi kontributor terbesar terhadap penjualan (38%)
-  Personal Care memiliki profit margin tertinggi.
-  Beverage memiliki profit margin terendah sehingga menjadi kategori yang perlu dievaluasi
-  Meskipun Units Sold sedikit menurun, Revenue dan Profit tetap meningkat. Hal ini mengindikasikan adanya peningkatan nilai penjualan per transaksi atau pergeseran ke produk dengan margin yang lebih tinggi. 
- United States menjadi wilayah dengan penjualan tertinggi
2. Analisa kinerja penjualan
Secara keseluruhan, jumlah order meningkat sebesar 0,7% YoY, sementara Average Order Value (AOV) meningkat sebesar 3,3%. Di sisi lain, Average Quantity per Order menurun sebesar 0,9%, menunjukkan bahwa pertumbuhan nilai transaksi tidak didorong oleh peningkatan jumlah unit yang dibeli per order. Dengan menggunakan hubungan Revenue = Orders × AOV, implied revenue growth dapat dihitung sebagai:

YoY Revenue = (1 + 0,007)(1 + 0,033) − 1 = 4,02%

Angka ini konsisten dengan pertumbuhan revenue sekitar 4% yang terlihat pada dashboard kinerja keseluruhan. Dengan demikian, pertumbuhan revenue tampaknya lebih banyak didorong oleh peningkatan nilai per order dibandingkan pertumbuhan volume. Namun, kenaikan AOV belum dapat secara langsung diatribusikan kepada kenaikan harga per item karena dapat pula dipengaruhi oleh perubahan product mix.

Beverages menjadi kategori dengan penjualan tertinggi dengan kontribusi **24,33%** lalu diikuti oleh snack sebesar **22,67%,** sebesar lalu personal care sebesar **18,35%** lalu household sebesar **17,89%** dan dairy & breakfast sebesar **16,76%** dengan selisih yang tidak terpaut jauh antar kategori menunjukkan pondasi revenue stream penjualan tidak tergantung pada 1 kategori.

Namun yang perlu disorot disini adalah walaupun beverages memiliki quantity of sales yang tinggi jika dilihat dari segi profitabillitas sebagai bobot untuk mengukur kualitas penjualan maka beverages justru menyumbangkan profit terendah **(13,64%)** daripada kategori lainnya sedangkan Household menjadi kategori dengan kontribusi profit tertinggi **(26,71%)**, ini mengindikasikan bahwa kategori beverages bergantung pada kuantitas dan memiliki biaya satuan yang cukup tinggi, ini didukung setelah melihat lebih lanjut kepada kontribusi cogs pada setiap  kategori ternyata Beverages menyumbang COGS terbesar nomor 1 **(29,15%)** diikuti oleh kategori household **(20,66%)** 

    <img width="1318" height="446" alt="image" src="https://github.com/user-attachments/assets/2d0ce23c-61c7-48ef-a000-5349a2885656" />
  - 
    



