# COMPREHENSIVE-FMCG-ANALYSIS (ON - GOING PROJECT)


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

<img width="1079" height="398" alt="image" src="https://github.com/user-attachments/assets/07694a9e-323b-4963-a459-8de4fd6b1244" />




Jika ketiga perubahan tersebut dikombinasikan, implied revenue growth untuk Beverages adalah sekitar:


_(1-0,014)(1-0,009)-1 = -2,29%_


Jadi, **secara implied, revenue Beverages mengalami kontraksi sekitar 2,3%**, yang menunjukkan bahwa kategori dengan kontribusi quantity sales terbesar justru sedang menghadapi tekanan dari sisi volume maupun transaction value. Ini menjadi particularly important karena Beverages juga merupakan kategori dengan kontribusi COGS terbesar dan profit contribution terendah. Dengan demikian, masalah pada Beverages bukan hanya **"sales-nya turun"**, tetapi terdapat indikasi bahwa **kategori dengan volume terbesar sekaligus memiliki kualitas revenue yang relatif rendah dan sedang mengalami deterioration pada seluruh KPI utama**.

Pada level produk, meskipun enam produk utama Beverages—**Energy Drink Zero (198.116), Energy Drink Classic (180.188), Instant Coffee Gold (159.112), Sparkling Water Berry (153.643), Sparkling Water Lemon (152.099), dan Green Tea (138.110)**—memiliki volume yang relatif berdekatan, sehingga tidak terdapat satu produk yang mendominasi secara ekstrem. Hal ini menunjukkan bahwa performa quantity sales dalam kategori Beverages relatif tersebar di antara beberapa *hero products*. Namun, pola tersebut berbeda ketika dilihat dari level brand. **FuelCore (120.075) dan AquaGlow (105.453)** memiliki volume yang jauh lebih tinggi dibandingkan **RoastTrail (46.739) dan ZenLeaf (45.430)**. Bahkan, dua brand dengan performa terendah memiliki volume **lebih dari 100% lebih rendah** dibandingkan FuelCore dan AquaGlow. Hal ini menunjukkan bahwa meskipun performa produk relatif tersebar, **brand performance dalam kategori Beverages lebih terkonsentrasi pada FuelCore dan AquaGlow**.

##### **Snack Category Performance**

Kategori **Snacks** menunjukkan pola yang berbeda dibandingkan Beverages. Secara keseluruhan, Total Orders mengalami penurunan sebesar **1,3% YoY**, sementara Average Quantity per Order juga turun sebesar **1,1%**. Kedua indikator tersebut menunjukkan adanya tekanan pada volume, baik dari sisi jumlah transaksi maupun jumlah unit yang dibeli dalam setiap transaksi. Namun, pada saat yang sama, **AOV meningkat sebesar 1,8%**, yang menunjukkan bahwa nilai transaksi justru mengalami peningkatan meskipun customer membeli sedikit lebih sedikit unit per order. Dengan menggunakan hubungan *Revenue = Orders × AOV*, implied revenue growth untuk kategori Snacks adalah sekitar **+0,48%**, melalui perhitungan ((1-0,013)(1+0,018)-1). Dengan demikian, **Snacks masih mampu mempertahankan pertumbuhan revenue tipis meskipun mengalami contraction pada volume penjualan**, karena peningkatan nilai transaksi berhasil mengompensasi penurunan jumlah order.

Jika dilihat lebih lanjut, penurunan Average Quantity per Order sebesar **1,1%** yang terjadi bersamaan dengan peningkatan AOV sebesar **1,8%** mengindikasikan bahwa peningkatan nilai transaksi tidak berasal dari bertambahnya jumlah unit yang dibeli. Secara implied, average selling value per unit meningkat sekitar **2,9%**, yang dapat mengindikasikan adanya peningkatan harga maupun perubahan *product mix* menuju produk dengan nilai per unit yang lebih tinggi. Oleh karena itu, pertumbuhan nilai pada kategori Snacks cenderung bersifat **value-driven**, bukan volume-driven, meskipun peningkatan AOV tersebut masih perlu dianalisis lebih lanjut untuk membedakan kontribusi *price effect* dan *mix effect*.

Pada level produk, performa penjualan kategori Snacks relatif **terdistribusi secara merata**. Enam produk dengan volume tertinggi terdiri dari Protein Bar Peanut (**53.251**), Chocolate Cookies (**52.408**), Protein Bar (**49.928**), Trail Mix Original (**47.227**), Potato Chips Sea Salt (**46.915**), dan Potato Chips BBQ (**46.213**) dengan rata-rata volume sekitar **49.324 unit** dan median **48.578 unit**. Selisih antara produk dengan volume tertinggi dan terendah hanya sekitar **7.038 unit**, atau sekitar **14,3% dari rata-rata volume keenam produk tersebut**. Hal ini menunjukkan bahwa tidak terdapat satu *hero product* yang secara ekstrem mendominasi volume penjualan, sehingga performa kategori pada level SKU relatif **balanced dan tidak terlalu bergantung pada satu produk tertentu**.

Namun, pola tersebut berbeda ketika dianalisis pada level brand. **Crunchmile mencapai volume 93.128**, sementara Biscora sebagai salah satu brand dengan performa terendah hanya mencatat **52.408**, sehingga volume Crunchmile sekitar **77,7% lebih tinggi** dibandingkan Biscora. Dengan NutrIbite dan Crunchmile sebagai dua brand dengan performa penjualan tertinggi, terdapat indikasi bahwa **kekuatan penjualan pada kategori Snacks lebih terkonsentrasi pada brand tertentu dibandingkan pada level produk**. Dengan kata lain, meskipun tidak terdapat satu produk yang mendominasi secara ekstrem, terdapat brand yang memiliki daya tarik lebih kuat secara keseluruhan terhadap volume penjualan kategori.

Temuan ini menunjukkan adanya perbedaan penting dalam struktur penjualan Snacks: **product performance relatif tersebar, tetapi brand performance lebih terkonsentrasi**. Kondisi tersebut mengindikasikan bahwa performa kategori tidak semata-mata bergantung pada keberadaan satu SKU unggulan, melainkan pada kekuatan portofolio produk yang berada di bawah brand tertentu. Oleh karena itu, analisis lanjutan pada kategori Snacks sebaiknya diarahkan untuk mengidentifikasi apakah keunggulan NutrIbite dan Crunchmile berasal dari **jumlah produk yang lebih banyak, performa masing-masing SKU yang lebih tinggi, positioning harga, atau kombinasi product mix**. Analisis tersebut akan membantu menentukan apakah pertumbuhan value pada Snacks dapat dipertahankan atau justru berisiko mengalami tekanan apabila volume terus menurun.

##### Personal Care Category Performance

Kategori **Personal Care** menunjukkan performa yang relatif kuat dibandingkan kategori lainnya. Secara keseluruhan, Total Orders meningkat sebesar **2,2% YoY**, sementara **Average Order Value (AOV)** meningkat sebesar **5,1%**. Di sisi lain, **Average Quantity per Order** mengalami penurunan sebesar **1,1%**, yang menunjukkan bahwa pertumbuhan kategori tidak berasal dari peningkatan jumlah unit yang dibeli dalam setiap transaksi. Dengan menggunakan hubungan *Revenue = Orders × AOV*, implied revenue growth Personal Care mencapai sekitar **7,42%**, melalui perhitungan ((1+0,022)(1+0,051)-1). Angka ini menunjukkan bahwa Personal Care merupakan salah satu kategori yang memberikan kontribusi positif terhadap pertumbuhan revenue, dengan pertumbuhan yang lebih tinggi dibandingkan implied overall revenue growth sekitar 4%.

Menariknya, peningkatan revenue tersebut terjadi meskipun Average Quantity per Order mengalami penurunan. Kombinasi **AOV yang meningkat 5,1%** dan Average Quantity per Order yang turun 1,1% menghasilkan implied increase pada average selling value per unit sekitar **6,3%**. Hal ini mengindikasikan bahwa peningkatan nilai transaksi kemungkinan berasal dari peningkatan nilai produk yang dibeli, baik melalui perubahan harga maupun *product mix*. Namun, angka tersebut masih bersifat implied dan belum dapat secara langsung diinterpretasikan sebagai kenaikan harga aktual, sehingga diperlukan analisis lebih lanjut terhadap unit price dan perubahan komposisi produk.

Pada level produk, performa penjualan Personal Care relatif tersebar tanpa adanya satu produk yang mendominasi secara ekstrem. **Shampoo Repair** menjadi produk dengan volume tertinggi sebesar **46.395**, diikuti oleh **Hand Soap Gentle (45.146)**, **Body Wash Citrus (42.047)**, **Toothbrush Soft (40.029)**, **Toothpaste Mint (33.567)**, dan **Conditioner Smooth (32.457)**. Keenam produk tersebut memiliki rata-rata volume sebesar sekitar **39.940 unit**, dengan median **41.038 unit**. Meskipun Shampoo Repair menjadi produk dengan performa tertinggi, selisih antara produk tertinggi dan terendah mencapai sekitar **13.938 unit**, atau sekitar **34,9% dari rata-rata volume**, sehingga distribusinya dapat dikategorikan relatif diversified tetapi dengan gap performa yang lebih terlihat dibandingkan kategori Snacks. Dengan demikian, tidak terdapat indikasi bahwa revenue Personal Care sangat bergantung pada satu *hero product*, meskipun Shampoo Repair memiliki posisi yang paling kuat di antara produk yang dianalisis.

Pada level brand, tiga brand dengan volume penjualan tertinggi menunjukkan distribusi yang relatif balanced, yaitu **FreshNest (87.193)**, **PureLiva (78.852)**, dan **BrightSmile (73.596)**. Ketiga brand tersebut memiliki rata-rata volume sekitar **79.880 unit** dan median **78.852 unit**, dengan selisih antara brand tertinggi dan terendah sebesar **13.597 unit**. FreshNest memang menjadi brand dengan performa tertinggi, tetapi volumenya hanya sekitar **18,5% lebih tinggi dibandingkan BrightSmile**, sehingga belum menunjukkan tingkat konsentrasi brand yang ekstrem. Hal ini mengindikasikan bahwa, setidaknya di antara tiga brand dengan volume tertinggi, performa penjualan Personal Care relatif tidak terpusat pada satu brand tertentu.

Secara keseluruhan, **Personal Care menunjukkan pola pertumbuhan yang lebih sehat dibandingkan Beverages dan Snacks**. Pertumbuhan order sebesar **2,2%** menunjukkan adanya peningkatan aktivitas transaksi, sementara kenaikan AOV sebesar **5,1%** memberikan tambahan value yang cukup signifikan meskipun basket size turun 1,1%. Dengan implied revenue growth sekitar **7,42%**, Personal Care dapat dipandang sebagai **positive growth driver**, dengan pertumbuhan yang terutama didorong oleh kombinasi peningkatan jumlah transaksi dan peningkatan nilai transaksi, bukan oleh peningkatan jumlah unit per order. Tantangan analisis berikutnya adalah menentukan apakah peningkatan AOV tersebut terutama berasal dari **price effect, product-mix shift, atau perubahan kontribusi brand/product tertentu**.



    
 
    



