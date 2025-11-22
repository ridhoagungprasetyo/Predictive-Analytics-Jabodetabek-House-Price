# Predictive Analytics Jabodetabek House Price

## Domain Proyek
### Latar Belakang
Wilayah Jabodetabek (Jakarta, Bogor, Depok, Tangerang, dan Bekasi) Wilayah Jabodetabek, yang terdiri dari Jakarta, Bogor, Depok, Tangerang, dan Bekasi, merupakan pusat aktivitas ekonomi terbesar di Indonesia.
Kawasan ini juga menjadi titik utama pertumbuhan penduduk dan urbanisasi. Dengan meningkatnya migrasi dan kepadatan penduduk, permintaan akan perumahan di Jabodetabek mengalami lonjakan yang signifikan.

Menurut laporan tahunan Bank Indonesia pada tahun 2023, harga rumah di Jabodetabek tercatat naik rata-rata sebesar 8% per tahun, lebih tinggi dibandingkan dengan rata-rata nasional yang berada di angka 6% (https://www.bbc.com/indonesia/articles/cx7dnn864z1o)24. 

Kenaikan ini membuat ketidakstabilan harga properti yang cukup tinggi, yang di sisi lain memberikan tantangan bagi calon pembeli yang ingin menilai harga pasar secara lebih akurat.

Fluktuasi atau perubahan harga rumah dapat dipengaruhi oleh beberapa faktor termasuk lokasi, ukuran rumah, kondisi bangunan, faktor ekonomi makro dan sebagainya. Beberapa faktor tadi terkadang membingungkan dan membutuhkan waktu untuk mempertimbangkan dan memilih rumah yang sesuai. Oleh karena itu, dibutuhkan sebuah sistem untuk memprediksi harga rumah yang dapat memberikan estimasi dengan tepat/pantas dan membantu para penjual dan pembeli dalam mengambil keputusan.

Dengan membangun sistem yang bisa memprediksi harga rumah, pembeli maupun penjual akan mendapatkan harga rumah yang akurat serta ekspektasi harga yang realistis sehingga bisa meminimalkan risiko overpricing atau underpricing. Jika seorang investor atau pengembang, memiliki perkiraan harga rumah yang akurat dapat membantu dalam menentukan apakah suatu properti merupakan investasi yang menguntungkan atau tidak.

Menurut hasil studi dari [Alan Ihre et al](https://www.diva-portal.org/smash/record.jsf?pid=diva2%3A1354741&dswid=-7113) dalam jurnalnya berjudul *Predicting House Prices with Machine Learning Methods* dengan menggunakan dataset yang sama, didapat hasil bahwa permasalahan mengenai prediksi harga rumah bisa menggunakan metode regresi seperti misalnya KNN (K-Nearest Neighbor) atau Random Forest.

Penelitian oleh [Zhang et al] (2021)(https://repository.ipb.ac.id/handle/123456789/56157) menunjukkan bahwa model pembelajaran mesin seperti Random Forest dan Gradient Boosting memiliki kemampuan untuk memperkirakan harga rumah dengan akurasi tinggi.
Model-model ini mempertimbangkan berbagai variabel seperti:
Lokasi: Faktor lokasi sangat menentukan nilai properti.
Luas Lahan: Ukuran tanah berpengaruh langsung terhadap harga.
Usia Bangunan: Bangunan baru biasanya memiliki nilai lebih tinggi dibandingkan bangunan lama.
Aksesibilitas Fasilitas Umum: Kedekatan dengan transportasi umum, sekolah, dan pusat perbelanjaan juga memengaruhi harga.

Dengan memanfaatkan teknik pembelajaran mesin dan data historis harga rumah di Jabodetabek, model prediksi ini dapat memberikan wawasan berharga kepada pemangku kepentingan seperti pengembang properti, lembaga keuangan, dan pembeli individu. Penerapan model prediksi yang andal diharapkan tidak hanya membantu dalam menentukan harga jual dan beli yang wajar tetapi juga dapat mengidentifikasi faktor-faktor utama yang memengaruhi harga properti di kawasan ini. Oleh karena itu, pengembangan model prediksi harga rumah berbasis data dan teknologi AI menjadi kebutuhan mendesak untuk mengatasi tantangan dinamika harga rumah di Jabodetabek yang semakin kompleks.

## Business Understanding
Dengan harga rumah yang meningkat rata-rata 8% per tahun, lebih tinggi dari rata-rata nasional yang hanya sekitar 6%, calon pembeli sering kali menghadapi kesulitan dalam menentukan nilai wajar dari properti. Ketidakpastian ini dapat mengakibatkan keputusan investasi yang tidak tepat, yang pada gilirannya dapat mempengaruhi stabilitas pasar dan aksesibilitas perumahan bagi masyarakat.

Saat ini, banyak informasi mengenai harga rumah yang tidak tersedia secara terbuka, sehingga calon pembeli kesulitan dalam membuat keputusan. Dengan menyediakan data yang dapat diandalkan dan analisis yang mendalam tentang faktor-faktor yang memengaruhi harga rumah, proyek ini diharapkan dapat membantu menciptakan lingkungan pasar yang lebih transparan. Hal ini tidak hanya akan memberikan kepercayaan kepada pembeli tetapi juga mendorong pengembang untuk beroperasi dengan lebih etis dan bertanggung jawab.

### Problem Statements
Wilayah Jabodetabek, yang terdiri dari Jakarta, Bogor, Depok, Tangerang, dan Bekasi, mengalami pertumbuhan populasi yang pesat dan urbanisasi yang terus meningkat. Hal ini menyebabkan permintaan akan perumahan meningkat tajam, yang berdampak pada kenaikan harga properti secara signifikan. Menurut laporan tahunan Bank Indonesia pada tahun 2023, harga rumah di Jabodetabek meningkat rata-rata sebesar 8% per tahun, lebih tinggi dibandingkan dengan rata-rata nasional yang berada di angka 6%.
Berdasarkan kondisi yang telah diuraikan sebelumnya, perl dikembangkannya sistem yang mampu memprediksi harga rumah untuk menjawab permasalahan berikut:
- Dari serangkaian fitur yang ada, fitur apa saja yang paling berpengaruh terhadap harga jual rumah?
- Berapa harga pasar rumah dengan karakteristik atau fitur tertentu?

### Goals
- Mengetahui fitur yang paling berkorelasi dengan harga jual rumah.
- Membuat model machine learning yang dapat memprediksi harga jual rumah seakurat mungkin berdasarkan fitur - fitur yang ada.

### Solution statements
- Membuat sebuah model untuk memprediksi harga jual rumah. Pengembangan model akan menggunakan beberapa algoritma machine learning yaitu K-Nearest Neighbor, Random Forest, dan Boosting Algorithm dengan mengatur hyperparameter tuning dan melakukan improvement pada baseline model. Dari ketiga model ini, akan dipilih satu model yang memiliki nlai kesalahan prediksi terkecil untuk membuat model yang seakurat mungkin.
- Metrik digunakan untuk mengevaluasi seberapa baik model dalam memprediksi harga. Karena kasus kali ini merupakan kasus regresi, beberapa metrik yang digunakan adalah Mean Squared Error (MSE). Secara umum, metrik ini mengukur seberapa jauh hasil prediksi dengan nilai sebenarnya.

## Data Understanding
Data yang akan digunakan pada proyek kali ini adalah [Daftar Harga Rumah Jabodetabek](https://www.kaggle.com/datasets/nafisbarizki/daftar-harga-rumah-jabodetabek) yang diunduh dari kaggle 

Dataset ini dikumpulkan pada akhir 2022

### Variabel-variabel pada dataset jabodetabek_house_price adalah sebagai berikut:
Dataset berisi 3553 records dan 27 kolom yang memiliki karakteristik sebagai berikut:
- url : Link sumber data
- price_in_rp : Harga properti dalam satuan Rp (rupiah).
- title : Judul atau nama properti.
- address : Alamat lengkap properti.
- district : Wilayah administratif yang lebih kecil daripada kabupaten/kota, namun masih berstatus wilayah administratif.
- city : Nama kota dimana properti berada.
- lat : Koordinat lintang (latitude), nilai antara -90° sampai +90°.
- long : Koordinat bujur (longitude), nilai antara -180° sampai +180°.
- facilities : Fasilitas yang disediakan bersamaan dengan sewaan/milik properti.
- property_type : Jenis properti (rumah, apartemen, villa, dll.)
- ads_id : ID iklan properti.
- bedrooms : Jumlah kamar tidur.
- bathrooms : Jumlah kamar mandi.
- land_size_m2 : Luas tanah milik properti dalam meter persegi.
- building_size_m2 : Luas bangunan properti dalam meter persegi.
- carports : Tempat penyimpanan kendaraan mobil
- certificate : Dokumen legal yang menunjukkan kepemilikan atau hak atas suatu properti
- electricity : Sistem listrik yang digunakan di properti
- maid_bedrooms : Jumlah kamar tidur untuk pelayan.
- maid_bathrooms : Jumlah kamar mandi untuk pelayan.
- floors : Tingkat/titik tertinggi dari sebuah struktur bangunan.
- building_age : Umur bangunan
- year_built : Tahun pembangunan properti
- property_condition : Status kondisi properti sekarang ini (baru,sedang renovasi,dll.)
- building_orientation : Orientasi arah bangunan relatif matahari/sinar matahari
- garages : Lahan parkir kendaraan
- furnishing : Pengaturan interior/dekorasi ruangan

Untuk memahami data, selanjutnya akan dilakukan proses berikut:
### 1. Data Loading
Supaya isi dataset lebih mudah dipahami, kita perlu melakukan proses loading data terlebih dahulu dengan import library pandas untuk dapat membaca file datanya.

### 2. Exploratory Data Analysis
#### Informasi Dataset
Mengecek informasi pada dataset dengan fungsi info()
<!-- ![image](https://drive.google.com/file/d/1-0liDpOEg2AFYHdNhPT2fd3wxbaDEBC-/view?usp=drive_link) -->

Berdasarkan informasi yang diatmpilkan dataset memiliki beberapa kriteria antara lain:
- 14 Kolom dengan tipe float64 
- 13 Kolom dengan tipe object yaitu Name, Symbol, dan Date
#### Melihat deskripsi satistik
memberikan informasi statistik pada masing - masing kolom, antara lain:
Count adalah jumlah sampel pada data.
Mean adalah nilai rata-rata.
Std adalah standar deviasi.
Min yaitu nilai minimum setiap kolom.
25% adalah kuartil pertama. Kuartil adalah nilai yang menandai batas interval dalam empat bagian sebaran yang sama.
50% adalah kuartil kedua, atau biasa juga disebut median (nilai tengah).
75% adalah kuartil ketiga.
Max adalah nilai maksimum

## Data Preparation
#### Cek Missing Value
Jika data terdiri dari ratusan bahkan ribuan baris tentu akan susah dalam menemukan nilai field yang kosong. Oleh karena itu, Pandas memungkinkan kita dapat menemukan missing value secara cepat dengan fungsi isna() dan sum().
<!-- ![image](https://drive.google.com/file/d/1TrSTw5hiJnevEQWByUKY8Q2Gq4Pnfo-0/view?usp=drive_link) -->

#### Menghapus Missinng Value
Menghapus Variabel/Fitur yang terdaapat Nilai NaN sehingga tidak lagi muncul dalam data terbaru sehingga hanya tersisa 14 Fitur.
<!-- ![image](https://drive.google.com/file/d/1CvntNAN4bnkyMVXs7OCmhceVUxWJNgbL/view?usp=drive_link) -->

#### Cek dan Penanganan Outlier
Pada kasus ini, kita memeriksa outlier pada kolom numerik dan menghapus outlier menggunakan teknik Inter Quartile Range (IQR). IQR didefinisikan sebagai berikut:

IQR=Q3−Q1 
Batas Bawah =  Q1−1.5∗IQR 
Batas Atas =  Q3+1.5∗IQR

Dan dari penanganan outlier yang ada didapatkan hasil jumlah data tanpa adanya oulier tersisa 3076 baris dan 14 kolom
#### Cek data duplikat
Berdasarkan hasil dari data_cleaned.duplicated().sum(), tidak terdapat data duplikat pada data.
<!-- ![image](https://drive.google.com/file/d/1p4LornNgRQsGGFGBCY1-Ty3g0S42Onvd/view?usp=drive_link) -->

### Data Cleaning
Menghapus data yang memiliki korelasi yang kecil yang ditunjukkan pada visualisasi heatmap.
<!-- ![image](https://drive.google.com/file/d/1VKRAETEyn6LS2DaSMNlaOTVvdhuVaH5N/view?usp=drive_link) -->

Jika dilihat dari korelasi numerik fitur, bisa disimpulkan bahwa Fitur yang kuat dalam mempengaruhi harga rumah di jabodetabek adalah maid_bedrooms dan maid_bethrooms begitu juga disini terlihat pada kolom garages memiliki korelasi palinng kecil terhadap price_in_rp.

### Encoding Fitur Kategori
Proses encoding fitur kategori menggunakan teknik one-hot-encoding. Teknik ini adalah salah satu metode dalam proses encoding fitur (feature encoding) pada data kategorikal. Tujuannya adalah untuk mengubah variabel kategorikal menjadi representasi biner yang dapat digunakan dalam algoritma pembelajaran mesin. Dalam dataset terdapat beberapa variabel kategori, maka dilakukan proses encoding ini dengan fitur get_dummies.
### Reduksi Dimensi dengan PCA
Teknik reduksi (pengurangan) dimensi adalah prosedur yang mengurangi jumlah fitur dengan tetap mempertahankan informasi pada data. Teknik pengurangan dimensi yang digunakan pada proyek ini adalah PCA. PCA adalah teknik untuk mereduksi dimensi, mengekstraksi fitur, dan mentransformasi data dari “n-dimensional space” ke dalam sistem berkoordinat baru dengan dimensi m, di mana m lebih kecil dari n.

PCA bekerja menggunakan metode aljabar linier dengan mengasumsikan bahwa sekumpulan data pada arah dengan varians terbesar merupakan yang paling penting (utama). PCA umumnya digunakan ketika variabel dalam data memiliki korelasi yang tinggi. Korelasi tinggi ini menunjukkan data yang berulang atau redundant. Karena hal inilah, teknik PCA digunakan untuk mereduksi variabel asli menjadi sejumlah kecil variabel baru yang tidak berkorelasi linier, disebut komponen utama (PC). Komponen utama ini dapat menangkap sebagian besar varians dalam variabel asli. Sehingga, saat teknik PCA diterapkan pada data, PCA hanya akan menggunakan komponen utama dan mengabaikan sisanya.
### Train-Test-Split
Selanjutnya adalah membagi dataset menjadi data latih (train) dan data uji (test). Proses pembagian dataset menggunakan library sklearn yaitu train-test-split. Proporsi pembagian adalah 80:20. Dilakukan juga pemisahkan fitur dengan target (label) yaitu price_in_rp.
<!-- ![image](https://drive.google.com/file/d/19totx7iLPvLMwcDK3p0iQdL8-EvrPyqv/view?usp=drive_link) -->
Hasil pembagian dataset menghasilkan sampel untuk train dataset sebesar 2460 dan sampel untuk test dataset sebesar 616 dari total keseluruhan dataset yaitu sebesar 3076 buah sampel.

### Standarisasi
Standardisasi adalah teknik transformasi yang paling umum digunakan dalam tahap persiapan pemodelan. Untuk fitur numerik tidak akan melakukan transformasi dengan one-hot-encoding seperti pada fitur kategori, tetapi akan menggunakan teknik StandarScaler dari library Scikitlearn. StandardScaler melakukan proses standarisasi fitur dengan mengurangkan mean (nilai rata-rata) kemudian membaginya dengan standar deviasi untuk menggeser distribusi. StandardScaler menghasilkan distribusi dengan standar deviasi sama dengan 1 dan mean sama dengan 0. Sekitar 68% dari nilai akan berada di antara -1 dan 1.
<!-- ![image](https://drive.google.com/file/d/189YzqgFblz3snrjKah6xhrSSJxK_ZGZP/view?usp=drive_link) -->
Untuk menghindari kebocoran informasi pada data uji, hanya akan diterapkan fitur standarisasi pada data latih. Kemudian, setelah itu pada tahap evaluasi akan dilakukan standarisasi pada data uji.

## Modeling
Pada tahap ini, akan dikembangkan model machine learning dengan tiga algoritma. Kemudian, dilakukan evaluasi performa masing-masing algoritma dan menentukan algoritma mana yang memberikan hasil prediksi terbaik. Ketiga algoritma yang akan digunakan pada proyek kali ini antara lain:
- K-Nearest Neighbor
- Random Forest
- Boosting Algorithm
### K-Nearest Neighbor
[KNN](https://www.ibm.com/topics/knn#:~:text=Next%20steps-,K-Nearest%20Neighbors%20Algorithm,of%20an%20individual%20data%20point.) adalah algoritma yang relatif sederhana dibandingkan dengan algoritma lain. Algoritma KNN menggunakan ‘kesamaan fitur’ untuk memprediksi nilai dari setiap data yang baru. Dengan kata lain, setiap data baru diberi nilai berdasarkan seberapa mirip titik tersebut dalam set pelatihan. KNN bekerja dengan membandingkan jarak satu sampel ke sampel pelatihan lain dengan memilih sejumlah k tetangga terdekat (dengan k adalah sebuah angka positif), itulah mengapa algoritma ini dinamakan K-nearest neighbor (sejumlah k tetangga terdekat). KNN bisa digunakan untuk kasus klasifikasi dan regresi. Walaupun begitu KNN memiliki kelebihan dan kekurangan sebagai berikut:

Kelebihan KNN adalah:
- Sederhana dan Mudah Dipahami: Konsep KNN relatif mudah untuk dipahami dan diimplementasikan. Ini adalah salah satu algoritma pembelajaran mesin yang paling sederhana.
- Cocok untuk Klasifikasi Non-Linier: KNN bisa sangat efektif untuk masalah klasifikasi yang tidak memiliki batas keputusan linier yang jelas. Algoritma ini mampu menangani relasi non-linier antara fitur.
- Cocok untuk Dataset dengan Banyak Fitur: KNN dapat berfungsi dengan baik bahkan pada dataset dengan banyak fitur, asalkan jumlah tetangga (k) dipilih dengan benar.

Kelemahan KNN adalah:
- Sensitif terhadap Pemilihan Jumlah Tetangga (k): KNN sangat sensitif terhadap nilai k yang dipilih. Jika k terlalu kecil, model akan menjadi sensitif terhadap noise dan outlier. Jika k terlalu besar, model dapat kehilangan kemampuan untuk memahami struktur lokal dari data.
- Membutuhkan Memori Lebih Banyak: Algoritma KNN memerlukan penyimpanan seluruh dataset latih di memori. Untuk dataset besar, ini dapat menghabiskan banyak memori.
- Komputasi yang Tinggi pada Pengujian: Untuk memprediksi label atau nilai untuk setiap sampel baru, algoritma KNN harus menghitung jarak dari sampel baru ke semua sampel dalam set pelatihan, yang dapat memakan waktu jika dataset besar.
- Tidak Cocok untuk Data Berkasatria Tinggi (High-Dimensional Data): Ketika jumlah fitur sangat besar, ruang berkasatria menjadi sangat penuh dan mengukur jarak antara tetangga mungkin kehilangan makna.

Proses pembuatan model menggunakan algoritma KNN dimulai dengan mencari kombinasi terbaik dari hyperparameter terbaik menggunakan GridSearch. Pada tahap ini dataset yang dilatih hanya data training, sedangkan data testing digunakan nantinya untuk tahap evaluasi yang akan dibahas pada bagian evaluasi model. Proses pembuatan model menggunakan library scikit-learn bernama [KNeighborsRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsRegressor.html) dimana method ini menggunakan paramater bernama n_neighbors yang merepresentasikan jumlah nilai k tetangga serta digunakan juga metrik Mean Squared Error (MSE) sebagai metrik evaluasi model.
### Random Forest
Random forest merupakan salah satu model machine learning yang termasuk ke dalam kategori ensemble (group) learning. Random forest merupakan model prediksi yang terdiri dari beberapa model dan bekerja secara bersama-sama. Ide dibalik model ensemble adalah sekelompok model yang bekerja bersama menyelesaikan masalah. Sehingga, tingkat keberhasilan akan lebih tinggi dibanding model yang bekerja sendirian. Pada model ensemble, setiap model harus membuat prediksi secara independen. Kemudian, prediksi dari setiap model ensemble ini digabungkan untuk membuat prediksi akhir. Disebut random forest karena algoritma ini disusun dari banyak algoritma pohon (decision tree) yang pembagian data dan fiturnya dipilih secara acak.

Kelebihan Random Forest:
- Akurasi Tinggi: Random Forest adalah salah satu algoritma yang memiliki akurasi tinggi dalam masalah klasifikasi dan regresi. Karena menggabungkan banyak pohon keputusan, cenderung mengurangi overfitting.
- Tidak Sensitif terhadap Outlier dan Data Missing: Random Forest bisa menangani data yang tidak seimbang dan fitur yang hilang (missing values) tanpa memerlukan pre-processing yang ekstensif.
- Bisa Mengatasi Data Berkasatria Tinggi (High-Dimensional Data): Algoritma ini bekerja dengan baik pada data yang memiliki banyak fitur.
- Mampu Menangani Variabel Numerik dan Kategorikal: Random Forest dapat menangani baik variabel numerik maupun kategorikal tanpa memerlukan transformasi tambahan.

Kekurangan Random Forest:
- Kesulitan dalam Interpretasi Model: Random Forest adalah model ensemble kompleks, yang bisa sulit untuk diinterpretasi dan menjelaskan mengapa keputusan spesifik dibuat.
- Membutuhkan Memori Lebih Banyak: Karena Random Forest menggabungkan beberapa pohon keputusan, ia memerlukan lebih banyak memori daripada model tunggal.
- Kurang Cepat dalam Proses Prediksi: Proses prediksi dengan Random Forest mungkin lebih lambat daripada model tunggal seperti pohon keputusan karena harus menggabungkan hasil dari beberapa pohon.

Sedikit mirip dengan membuat model KNN, Proses pembuatan model menggunakan algoritma Random Forest dimulai dengan mengimpor [RandomForestRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html) dari library scikit-learn dan mengimport mean_squared_error sebagai metrik untuk mengevaluasi performa model. Kemudian dibuat juga variabel bernama RF dan memanggil RandomForestRegressor dengan beberapa nilai parameter. Berikut adalah parameter-parameter yang digunakan:
- n_estimator: jumlah trees (pohon) di forest.
- max_depth: kedalaman atau panjang pohon dan merupakan ukuran seberapa banyak pohon dapat membelah (splitting) untuk membagi setiap node ke dalam jumlah pengamatan yang diinginkan.
- random_state: digunakan untuk mengontrol random number generator yang digunakan. Pada proyek kali ini digunakan random state sebesar 55.
- n_jobs: jumlah job (pekerjaan) yang digunakan secara paralel dan merupakan komponen untuk mengontrol thread atau proses yang berjalan secara paralel. Pada proses pembuatan model kali ini ditetapkan nilai n_jobs=-1, artinya semua proses berjalan secara paralel.

### Boosting Algorithm
Boosting Algorithm adalah metode pembelajaran mesin ensemble yang berusaha meningkatkan kinerja model dengan menggabungkan sejumlah kecil model lemah (biasanya pohon keputusan dangkal atau pengklasifikasi lemah lainnya) menjadi model yang kuat. Secara umum, algoritma boosting bekerja dengan cara memberikan bobot yang berbeda pada setiap sampel dalam dataset sehingga model berfokus pada sampel yang sulit diprediksi oleh model sebelumnya.

Ada beberapa jenis algoritma boosting yang populer, tapi pada proyek ini yang digunakan adalah AdaBoost (Adaptive Boosting). AdaBoost menggunakan model lemah dan menyesuaikan bobot pada setiap sampel, memberikan lebih banyak fokus pada sampel yang salah diklasifikasikan sebelumnya.

Kelebihan algoritma boosting:
- Akurasi Tinggi: Boosting sering menghasilkan model yang memiliki akurasi yang sangat tinggi, karena mampu mengurangi bias dan varians.
- Mampu Menangani Data yang Tidak Seimbang: Boosting dapat menangani masalah klasifikasi dengan dataset yang tidak seimbang dengan baik, karena memberi bobot lebih pada sampel dari kelas yang kurang umum.
- Tidak Sensitif terhadap Data Outlier: Boosting memiliki kekebalan terhadap outlier, karena fokus pada sampel yang sulit diprediksi oleh model sebelumnya.
- Mampu Menangani Variabel Kategorikal dan Numerik: Banyak implementasi boosting dapat menangani baik variabel kategorikal maupun numerik tanpa memerlukan pre-processing tambahan.

Kelemahan algoritma boosting:
- Memerlukan Waktu Komputasi yang Lebih Lama: Training boosting algorithms mungkin memerlukan lebih banyak waktu dan sumber daya komputasi dibandingkan dengan beberapa algoritma pembelajaran mesin lainnya.
- Overfitting Jika Tidak Dikontrol: Ada kemungkinan overfitting jika parameter tidak diatur dengan benar atau jika terlalu banyak pohon digunakan dalam ensemble.
- Rentan terhadap Noise: Boosting bisa sangat sensitif terhadap noise dalam data latih.

Proses pembuatan model dengan algoritma AdaBoost dimulai dengan mengimpor [AdaBoostRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.AdaBoostRegressor.html) dari library scikit-learn serta mengimpor mean_squared_error sebagai metrik evaluasi model. Terdapat beberapa parameter yang digunakan pada method AdaBoostRegressor pada proyek ini yaitu:
- learning_rate: bobot yang diterapkan pada setiap regressor di masing-masing proses iterasi boosting.
- random_state: digunakan untuk mengontrol random number generator yang digunakan. Nilai random_state ditetapkan pada model ini adalah 55.

## Evaluation
Metrik yang digunakan pada proyek ini untuk melakukan evaluasi model adalah MSE atau [Mean Squared Error](https://en.wikipedia.org/wiki/Mean_squared_error) yang menghitung jumlah selisih kuadrat rata-rata nilai sebenarnya dengan nilai prediksi. Jika prediksi mendekati nilai sebenarnya, performanya baik. Sedangkan jika tidak, performanya buruk. Secara teknis, selisih antara nilai sebenarnya dan nilai prediksi disebut eror. Maka, semua metrik mengukur seberapa kecil nilai eror tersebut. MSE didefinisikan dalam persamaan berikut:

$$MSE = \frac{1}{N} \Sigma_{i=1}^N({y_i}- y\_pred_i)^2$$

Keterangan:
- N = jumlah dataset
- yi = nilai sebenarnya
- y_pred = nilai prediksi

Sebelum menghitung nilai MSE, dilakukan proses scaling fitur numerik pada data uji terlebih dahulu. Karena sebelumnya, hanya dilakukan proses scaling pada data latih saja. Setelah model dilatih menggunakan 3 jenis algoritma yaitu KNN, Random Forest dan AdaBoost, selanjutnya harus dilakukan proses scaling fitur pada data uji, hal ini bertujuan agar skala antara data latih dan data uji sama dan bisa melakukan proses evaluasi.

Evaluasi ketiga model menggunakan metrik MSE. Saat menghitung nilai MSE pada data train dan test dilakukan pembagian dengan bilangan 1e6, hal ini bertujuan agar nilai mse tidak terlalu besar skalanya.

Nilai MSE dari ketiga model yaitu KNN, Random Forest (RF) dan Boosting Algorithm
|          |         train         |          test         |
|:---------|----------------------:|----------------------:|
|KNN       |  759457136686991872.0 | 1030529178051947904.0 |
|RF	       |  259494600908571200.0 |  847564830124054144.0 |
|Boosting  | 1080302630727024384.0 | 1040943033786082688.0 |

<!-- ![image](https://drive.google.com/file/d/1q1ecITmyN_QytXr2118w_xgweXn5o-dz/view?usp=drive_link) -->
<!-- ![image](https://drive.google.com/file/d/1K-Y0PvkrTYK5TDHlIbJkTFHdDPZ3QDTa/view?usp=drive_link) -->
terlihat bahwa, model Random Forest (RF) memberikan skor nilai error paling kecil dibandingkan algoritma lain seperti KNN dan AdaBoost. Jadi, Model Random Forest yang akan dipilih sebagai model terbaik untuk memprediksi harga jual rumah. Untuk mengujinya, dilakukan prediksi menggunakan beberapa harga dari data test dan didapatkan output atau hasil seperti tabel berikut.

Hasil Prediksi dari ketiga model (KNN, Random Forest, dan Boosting Algorithm) pada data uji

|      |     y_true   |   prediksi_KNN |   prediksi_RF |   prediksi_Boosting |
|-----:|-------------:|---------------:|--------------:|--------------------:|
| 3137 |  960000000.0 |   1.173000e+09 |   954022231.8 |         703002012.1 |

<!-- ![image](https://drive.google.com/file/d/1TIgas29V0M91UTYKkKP4GYpBt1fMITLh/view?usp=drive_link) -->
Terlihat bahwa prediksi Random Forest (RF) memberikan hasil yang paling mendekati dengan y_true (data test). Dimana nilai y_true adalah 960000000.0 sedangkan nilai prediksi dari Random Forest adalah 954022231.8.

Bisa disimpulkan bahwa dari proses exploratory data hingga evaluasi model yang telah dilakukan bahwa fitur-fitur yang mempengaruhi harga dari rumah  di Jabodetabek antara lain maid_bedrooms dan maid_bathrooms
<!-- ![image](https://drive.google.com/file/d/1VKRAETEyn6LS2DaSMNlaOTVvdhuVaH5N/view?usp=drive_link) -->
dan hasil prediksi harga rumah juga menunjukkan keakuratan menggunakan metode Random Forest (RF).

Dari model prediksi yang telah dibangun sangat dapat membantu dalam menentukan harga jual dan beli yang wajar tetapi juga dapat mengidentifikasi faktor-faktor utama yang memengaruhi harga properti di kawasan Jabodetabek.




