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
  - Beverages menjadi kategori dengan penjualan tertinggi dengan kontribusi 24,33% lalu diikuti oleh snack 22,67%, lalu personal care 18,35% lalu household 17,89% dan dairy & breakfast 16,76 dengan selisih yang tidak terpaut jauh antar kategori menunjukkan pondasi revenue stream penjualan tidak tergantung pada 1 kategori namun yang perlu disorot disini adalah walaupun beverages memiliki quantity of sales yang tinggi jika dilihat dari sudut pandang profitabillitas sebagai bobot untuk mengukur kualitas penjualan maka beverages justru menyumbangkan profit terendah (13,64%) daripada kategori lainnya sedangkan Household menjadi kategori dengan kontribusi profit tertinggi (26,71%), ini mengindikasikan bahwa kategori beverages bergantung pada kuantitas dan memiliki biaya satuan yang cukup tinggi, ini didukung setelah melihat lebih lanjut kepada kontribusi cogs pada setiap  kategori ternyata Beverages menyumbang COGS terbesar nomor 1 (29,15%) diikuti oleh kategori household (20,66%)
  -  4. Analisa Alokasi Promosi


