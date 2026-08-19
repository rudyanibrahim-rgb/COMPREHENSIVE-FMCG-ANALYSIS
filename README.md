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
#### **1. Analisa kinerja keseluruhan**

-  Revenue meningkat 4% dibanding tahun sebelumnya
-  Profit naik 4.6%, sedangkan profit margin hanya naik 0.6%, mengindikasikan pertumbuhan profit berasal dari peningkatan volume penjualan, bukan peningkatan efisiensi.
-  Wholesale masih menjadi kontributor terbesar terhadap penjualan (38%)
-  Personal Care memiliki profit margin tertinggi.
-  Beverage memiliki profit margin terendah sehingga menjadi kategori yang perlu dievaluasi
-  Meskipun Units Sold sedikit menurun, Revenue dan Profit tetap meningkat. Hal ini mengindikasikan adanya peningkatan nilai penjualan per transaksi atau pergeseran ke produk dengan margin yang lebih tinggi. 
- United States menjadi wilayah dengan penjualan tertinggi
#### **2. Analisa kinerja penjualan**
##### **Overall Sales Performance**

Secara keseluruhan, jumlah order meningkat sebesar **0,7% YoY**, sementara **Average Order Value (AOV)** meningkat sebesar **3,3%**. Di sisi lain, **Average Quantity per Order** menurun sebesar **0,9%**, menunjukkan bahwa peningkatan nilai transaksi tidak didorong oleh peningkatan jumlah unit yang dibeli dalam setiap order. Dengan menggunakan hubungan **Revenue = Orders × AOV**, implied revenue growth dapat dihitung sebesar **4,02%**, melalui perhitungan **((1+0,007)(1+0,033)-1)**. Angka tersebut konsisten dengan pertumbuhan revenue sekitar 4% pada dashboard, sehingga dapat disimpulkan bahwa **pertumbuhan revenue lebih banyak didorong oleh peningkatan nilai per order dibandingkan pertumbuhan volume**. Meskipun demikian, peningkatan AOV belum dapat secara langsung diatribusikan kepada kenaikan harga karena dapat pula dipengaruhi oleh perubahan **product mix**.

Secara historis, volume penjualan menunjukkan pola musiman dengan posisi tertinggi secara umum berada pada **bulan Desember**. Bahkan, **Desember 2025 mencatat volume penjualan tertinggi dalam dua tahun terakhir**, yang mengindikasikan adanya momentum penjualan yang kuat pada periode akhir tahun. Dari sisi brand, **Top 10 brand mencakup setidaknya satu brand dari setiap kategori**, menunjukkan bahwa performa penjualan pada level brand relatif tersebar dan tidak hanya bergantung pada satu kategori tertentu. Namun, ketika dianalisis pada level produk, terdapat konsentrasi yang lebih jelas. **Top 10 product berdasarkan quantity sales terdiri dari lima produk Snacks dan lima produk Beverages**, menunjukkan bahwa volume penjualan tertinggi lebih terkonsentrasi pada kedua kategori tersebut.

##### **Category Performance & Revenue Quality**

Dari sisi kontribusi quantity sales, **Beverages menjadi kategori dengan kontribusi terbesar sebesar 24,33%**, diikuti oleh Snacks **22,67%**, Personal Care **18,35%**, Household **17,89%**, dan Dairy & Breakfast **16,76%**. Selisih kontribusi antar kategori relatif tidak terlalu besar, yang menunjukkan bahwa **revenue stream perusahaan memiliki basis kategori yang cukup terdiversifikasi dan tidak bergantung secara berlebihan pada satu kategori**.

Namun, jika performa penjualan tidak hanya dinilai berdasarkan volume tetapi juga berdasarkan **profitability sebagai indikator kualitas revenue**, terdapat perbedaan yang cukup signifikan. Meskipun Beverages merupakan kategori dengan quantity sales tertinggi, kontribusinya terhadap total profit hanya sebesar **13,64%**, bahkan menjadi yang terendah dibandingkan kategori lainnya. Sebaliknya, **Household menghasilkan kontribusi profit tertinggi sebesar 26,71%**. Hal ini menunjukkan adanya perbedaan antara **sales volume dan sales quality**: Beverages mampu menghasilkan volume yang tinggi, tetapi volume tersebut belum diterjemahkan menjadi profit yang sebanding.

Temuan tersebut semakin relevan ketika dilihat dari sisi COGS. Beverages menyumbang **29,15% dari total COGS**, merupakan kontribusi COGS terbesar di antara seluruh kategori, sedangkan Household menyumbang **20,66%**. Dengan demikian, tingginya volume Beverages disertai dengan beban COGS yang relatif besar. **Temuan ini mengindikasikan bahwa Beverages memiliki revenue-to-profit conversion yang relatif rendah**, meskipun untuk menyimpulkan bahwa kategori tersebut memiliki *unit cost* yang lebih tinggi diperlukan analisis lanjutan terhadap COGS per unit atau gross margin.

##### **Beverages Diagnostic**

Beverages kemudian menjadi kategori yang paling perlu mendapatkan perhatian karena selain memiliki volume penjualan tertinggi, **seluruh KPI utamanya justru mengalami penurunan**: Total Orders turun **1,4%**, AOV turun **0,9%**, dan Average Quantity per Order turun **2,9%**. Ini merupakan sinyal yang lebih kuat dibandingkan sekadar melihat penurunan salah satu KPI, karena penurunan terjadi secara simultan pada **frequency, transaction value, dan basket size**. Dengan kata lain, kategori Beverages tidak hanya kehilangan jumlah order, tetapi customer yang tetap melakukan transaksi juga cenderung membeli **lebih sedikit unit dengan nilai transaksi yang lebih rendah**.

Jika ketiga perubahan tersebut dikombinasikan, implied revenue growth untuk Beverages adalah sekitar:


_(1-0,014)(1-0,009)-1 = -2,29%_


Jadi, **secara implied, revenue Beverages mengalami kontraksi sekitar 2,3%**, yang menunjukkan bahwa kategori dengan kontribusi quantity sales terbesar justru sedang menghadapi tekanan dari sisi volume maupun transaction value. Ini menjadi particularly important karena Beverages juga merupakan kategori dengan kontribusi COGS terbesar dan profit contribution terendah. Dengan demikian, masalah pada Beverages bukan hanya **"sales-nya turun"**, tetapi terdapat indikasi bahwa **kategori dengan volume terbesar sekaligus memiliki kualitas revenue yang relatif rendah dan sedang mengalami deterioration pada seluruh KPI utama**.

Pada level produk, meskipun enam produk utama Beverages—**Energy Drink Zero (198.116), Energy Drink Classic (180.188), Instant Coffee Gold (159.112), Sparkling Water Berry (153.643), Sparkling Water Lemon (152.099), dan Green Tea (138.110)**—memiliki volume yang relatif berdekatan, sehingga tidak terdapat satu produk yang mendominasi secara ekstrem. Hal ini menunjukkan bahwa performa quantity sales dalam kategori Beverages relatif tersebar di antara beberapa *hero products*. Namun, pola tersebut berbeda ketika dilihat dari level brand. **FuelCore (120.075) dan AquaGlow (105.453)** memiliki volume yang jauh lebih tinggi dibandingkan **RoastTrail (46.739) dan ZenLeaf (45.430)**. Bahkan, dua brand dengan performa terendah memiliki volume **lebih dari 100% lebih rendah** dibandingkan FuelCore dan AquaGlow. Hal ini menunjukkan bahwa meskipun performa produk relatif tersebar, **brand performance dalam kategori Beverages lebih terkonsentrasi pada FuelCore dan AquaGlow**.


    
 
    



