# 2025 COMPREHENSIVE-FMCG-ANALYSIS (ON - GOING PROJECT)


supported by :
<img src="https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=white" /> <img src="https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white" /> <img src="https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue" /> <img src="https://img.shields.io/badge/Sqlite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" /> <img src="https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white" /> <img src="https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252" />

### **link dashboard dan Notebook**
[dashboard](https://datastudio.google.com/reporting/e2d1aecd-caec-49a2-a8b5-115fe035f9b8)
[Notebook](https://colab.research.google.com/drive/1NPu0dFfk-DdUbpODntTAwbz04qDOA8IR?usp=sharing)



<img width="959" height="442" alt="image" src="https://github.com/user-attachments/assets/6e531afe-6c35-4e52-9850-34376aa1a996" />
<img width="959" height="442" alt="image" src="https://github.com/user-attachments/assets/15cb83e4-5f9e-4975-b474-020a0aacfffb" />
<img width="959" height="441" alt="image" src="https://github.com/user-attachments/assets/09ea8ee0-1eaa-4c32-bb6b-933b23760f9c" />



     
### **Executive Summary** 
  "Proyek analitik data menyeluruh yang berfokus pada analisis kinerja penjualan, efektivitas promosi, profitabilitas, dan faktor pendorong bisnis di industri FMCG."
  tools : 
  - Bigquery (SQL)
  - Google Colab (Python)
  - Looker Studio

### **Tahapan Tahapan project** :
* Data Extraction :
  Data didapatkan di website Kaggle <https://www.kaggle.com/datasets/atharvasoundankar/fmcg-sales-marketing-and-profit-data>, data diekstrak menggunakan bahasa pemrograman python dan dibersihkan dan diperiksa lebih lanjut granularitas datanya 
* Data Cleaning : data dibersihkan dari data duplikat dan null values, setelah diperhatikan tidak  ada duplikasi data dan null values yang akan berpengaruh negatif ke analisis
* Data Analysis : analisis yang dilakukan adalah eksploratory analysis dengan melakukan modeling data menggunakan query sql untuk mengetahui retensi pelanggan
### **Tahapan Tahapan Analisa** :
**1. Analisa kinerja keseluruhan**

-  Revenue meningkat 3.6% dibanding tahun sebelumnya
-  Profit naik 4.2%, sedangkan profit margin hanya naik 0.5%, mengindikasikan pertumbuhan profit berasal dari peningkatan reveneu penjualan, bukan peningkatan efisiensi operasional.
-  Wholesale masih menjadi kontributor terbesar terhadap penjualan (38%)
-  Personal Care memiliki profit margin tertinggi.
-  Beverage memiliki profit margin terendah sehingga menjadi kategori yang perlu dievaluasi
-  Meskipun Units Sold sedikit menurun, Revenue dan Profit tetap meningkat. Hal ini mengindikasikan adanya peningkatan nilai penjualan per transaksi atau pergeseran ke produk dengan margin yang lebih tinggi. 
- United States menjadi wilayah dengan penjualan tertinggi
  
**2. Analisa kinerja penjualan**
**Overall Sales Performance**

Secara keseluruhan, jumlah order meningkat sebesar **0,4% YoY**, sementara **Average Order Value (AOV)** meningkat sebesar **3,2%**. Di sisi lain, **Average Quantity per Order** menurun sebesar **-0,9%**, menunjukkan bahwa peningkatan nilai transaksi tidak didorong oleh peningkatan jumlah unit yang dibeli dalam setiap order. Dengan menggunakan hubungan **Revenue = Orders × AOV**, implied revenue growth dapat dihitung sebesar **3,61%**, melalui perhitungan **((1+0,004)(1+0,032)-1)**. Angka tersebut sesuai memvalidasi **pertumbuhan revenue lebih banyak didorong oleh peningkatan nilai per order dibandingkan pertumbuhan volume**. Meskipun demikian, peningkatan AOV belum dapat secara langsung diatribusikan kepada kenaikan harga karena dapat pula dipengaruhi oleh perubahan **product mix**.

Secara historis, volume penjualan menunjukkan pola musiman dengan posisi tertinggi secara umum berada pada **bulan Desember**. Bahkan, **Desember 2025 mencatat volume penjualan tertinggi dalam dua tahun terakhir**, yang mengindikasikan adanya momentum penjualan yang kuat pada periode akhir tahun. Dari sisi brand, **Top 10 brand mencakup setidaknya satu brand dari setiap kategori**, menunjukkan bahwa performa penjualan pada level brand relatif tersebar dan tidak hanya bergantung pada satu kategori tertentu. Namun, ketika dianalisis pada level produk, terdapat konsentrasi yang lebih jelas. **Top 10 product berdasarkan quantity sales terdiri dari lima produk Snacks dan lima produk Beverages**, menunjukkan bahwa volume penjualan tertinggi lebih terkonsentrasi pada kedua kategori tersebut.

TOP 10 BRAND : 

<img width="484" height="242" alt="image" src="https://github.com/user-attachments/assets/4c63a60c-2f98-425e-b55a-640ef0e374f7" />

TOP 10 PRODUCT :

<img width="527" height="280" alt="image" src="https://github.com/user-attachments/assets/ef072596-370a-4d95-9c4d-9228016a9954" />




**Category Performance & Revenue Quality**

Dari sisi kontribusi quantity sales, **Beverages menjadi kategori dengan kontribusi terbesar sebesar 24,33%**, diikuti oleh Snacks **22,67%**, Personal Care **18,35%**, Household **17,89%**, dan Dairy & Breakfast **16,76%**. Selisih kontribusi antar kategori relatif tidak terlalu besar, yang menunjukkan bahwa **revenue stream perusahaan memiliki basis kategori yang cukup terdiversifikasi dan tidak bergantung secara berlebihan pada satu kategori**.

Namun, jika performa penjualan tidak hanya dinilai berdasarkan volume tetapi juga berdasarkan **profitability sebagai indikator kualitas revenue**, terdapat perbedaan yang cukup signifikan. Meskipun Beverages merupakan kategori dengan quantity sales tertinggi, kontribusinya terhadap total profit hanya sebesar **13,64%**, bahkan menjadi yang terendah dibandingkan kategori lainnya. Sebaliknya, **Household menghasilkan kontribusi profit tertinggi sebesar 26,71%**. Hal ini menunjukkan adanya perbedaan antara **sales volume dan sales quality**: Beverages mampu menghasilkan volume yang tinggi, tetapi volume tersebut belum diterjemahkan menjadi profit yang sebanding.

Temuan tersebut semakin relevan ketika dilihat dari sisi COGS. Beverages menyumbang **29,15% dari total COGS**, merupakan kontribusi COGS terbesar di antara seluruh kategori, sedangkan Household menyumbang **20,66%**. Dengan demikian, tingginya volume Beverages disertai dengan beban COGS yang relatif besar. **Temuan ini mengindikasikan bahwa Beverages memiliki revenue-to-profit conversion yang relatif rendah**, meskipun untuk menyimpulkan bahwa kategori tersebut memiliki *unit cost* yang lebih tinggi diperlukan analisis lanjutan terhadap COGS per unit atau gross margin.

<img width="1079" height="398" alt="image" src="https://github.com/user-attachments/assets/07694a9e-323b-4963-a459-8de4fd6b1244" />


**Implied Reveneu Growth**

Analisis ini bertujuan untuk mengetahui efek pertumbuhan penjualan setiap kategori terhadap reveneu keseluruhan dengan berlandaskan data jumlah Order_ID sebagai total order dan reveneu sebagai acuan basket value per order (AOV atau Average Order Value),
- **rumus implied reveneu growth ((1+pertumbuhan total order)(1+pertumbuhan AOV))-1**


<img width="719" height="428" alt="image" src="https://github.com/user-attachments/assets/9c3d98b4-ed59-4776-a4e5-f2ea71d20dcc" />


**TABEL ANALISA GROWTH REVENEU IMPACT :**


<img width="665" height="227" alt="image" src="https://github.com/user-attachments/assets/c64d272a-9465-4947-a124-8d2639def3a4" />


Pertumbuhan revenue secara keseluruhan terutama didorong oleh kategori Dairy & Breakfast, yang memberikan kontribusi pertumbuhan terbesar sebesar +1,90 percentage points (pp), diikuti oleh Personal Care sebesar +1,28 pp, Household sebesar +1,07 pp, dan Snacks sebesar +0,04 pp. Sebaliknya, Beverages menjadi satu-satunya kategori yang memberikan kontribusi negatif terhadap pertumbuhan revenue, yaitu sebesar −0,66 pp.

Temuan pada Beverages menjadi perhatian karena kategori ini memiliki revenue share terbesar, yaitu sekitar 25,87%, namun justru bertindak sebagai growth drag. Kontraksi tersebut terjadi karena kedua revenue driver Beverages melemah secara bersamaan: total order turun sekitar 1,72% dan AOV turun sekitar 0,85%, sehingga menghasilkan implied revenue growth sebesar −2,56%. Karena Beverages memiliki basis revenue terbesar, kontraksi tersebut memberikan tekanan yang relatif material terhadap pertumbuhan revenue perusahaan secara keseluruhan.

Secara agregat, kontribusi pertumbuhan dari seluruh kategori menghasilkan overall revenue growth sekitar 3,63% (selaras dengan reveneu growth index di dashboard pertamay). Pertumbuhan positif dari Dairy & Breakfast, Personal Care, Household, dan Snacks lebih dari cukup untuk mengompensasi kontraksi pada Beverages, sehingga revenue perusahaan secara keseluruhan tetap mengalami pertumbuhan. 

**Persebaran Performa Penjualan pada setiap produk dan brand**

<img width="685" height="337" alt="image" src="https://github.com/user-attachments/assets/f2912563-798d-4661-9f34-d13e7cbacfa1" />



<img width="241" height="112" alt="image" src="https://github.com/user-attachments/assets/f7f64eba-3ee6-4bfc-a0a7-4b13e070e664" /><img width="253" height="229" alt="image" src="https://github.com/user-attachments/assets/4d4d56fd-3201-4b06-9427-15d15225e510" />



Kategori Snacks menunjukkan performa penjualan yang paling merata di antara produk-produk unggulannya, tercermin dari coefficient of variation (CV) terendah, yaitu 6,09%. Angka tersebut menunjukkan bahwa penyimpangan penjualan antarproduk hanya sekitar 6,09% dari rata-rata penjualan kategori Snacks. Dengan kata lain, penjualan kategori ini tidak terlalu bergantung pada satu atau dua produk tertentu karena setiap produk unggulannya memiliki volume penjualan yang relatif konsisten. Kondisi tersebut berbeda dengan Personal Care, Household, Beverages, serta Dairy & Breakfast yang memiliki CV lebih tinggi, masing-masing sebesar 14,59%, 14,68%, 14,13%, dan 11,55%. Distribusi yang lebih merata ini mengindikasikan bahwa kategori Snacks memiliki portofolio produk yang lebih seimbang serta risiko konsentrasi penjualan yang lebih rendah. Oleh karena itu, apabila performa salah satu produk menurun, dampaknya terhadap keseluruhan penjualan kategori Snacks cenderung lebih terbatas karena penjualan turut ditopang oleh produk-produk lainnya.

**3. ANALISA DISTRIBUSI PROMOSI DAN EFEKTIFITASNYA PADA PROFITABILITAS**
Produk tanpa promosi mendominasi volume pesanan pada seluruh kategori produk dan saluran penjualan. Kondisi ini menunjukkan bahwa sebagian besar transaksi masih berasal dari penjualan reguler, sehingga promosi belum menjadi pendorong utama penjualan perusahaan. Terdapat kemungkinan bahwa perusahaan menerapkan promosi secara selektif, misalnya hanya pada produk yang penjualannya lemah, memiliki persediaan berlebih, atau membutuhkan peningkatan awareness. Namun, dominasi produk tanpa promosi juga dapat mengindikasikan adanya peluang ekspansi promosi yang belum dimanfaatkan secara optimal, terutama apabila pertumbuhan revenue dan quantity sold cenderung stagnan.

Dari sisi profitabilitas, transaksi tanpa promosi menghasilkan profit margin tertinggi, yaitu sekitar 25–26%. Loyalty Cashback memiliki margin yang hampir sama, sedangkan jenis promosi lainnya menghasilkan margin lebih rendah, berkisar antara 18–22%. Temuan ini menunjukkan bahwa dampak promosi terhadap profitabilitas berbeda-beda menurut jenisnya. Loyalty Cashback relatif mampu mempertahankan margin, sementara Festival Campaign dan Flash Discount memberikan tekanan margin yang lebih besar. Oleh karena itu, perusahaan sebaiknya tidak sekadar memperbanyak promosi, tetapi mengevaluasi efektivitas setiap jenis promosi berdasarkan tambahan penjualan dan profit yang dihasilkan. Promosi baru dapat dinilai efektif apabila peningkatan volume penjualan mampu mengompensasi penurunan margin per transaksi.
