### capstone project module 2 AirBnb

# **Latar Belakang**

> Airbnb, yang didirikan pada tahun 2008, adalah sebuah platform online yang menghubungkan penyewa akomodasi dengan penyedia tempat hunian, seperti rumah atau apartemen, kamar pribadi, hotel, dan kamar bersama. Kehadiran Airbnb telah mengubah cara orang mencari dan memesan tempat tinggal sementara, dengan pengguna terdiri dari host (pemilik properti) dan guest (tamu).

> Menurut data Airbnb yang dikutip oleh juru bicara pemerintah, jumlah wisatawan India yang memesan akomodasi melalui Airbnb meningkat sekitar 60%. Fitur akomodasi yang paling dicari oleh wisatawan India melalui Airbnb adalah kolam renang, pantai, taman nasional, dan kota-kota terkenal. Hal ini mengindikasikan bahwa pengguna aplikasi berpeluang semakin bertambah dengan standar keinginan yang semakin tinggi. Persaingan yang semakin ketat juga memaksa pemilik properti untuk lebih kreatif dan strategis dalam menarik tamu.

> Selain itu, regulasi pemerintah, perubahan tren wisata, dan perkembangan teknologi turut mempengaruhi keberhasilan bisnis di Airbnb. Oleh karena itu, memahami dinamika pasar, serta faktor-faktor yang mempengaruhi penawaran dan permintaan, sangat penting bagi pemilik properti dan investor untuk memaksimalkan keuntungan mereka di platform ini.
[Bangkok post](https://www.bangkokpost.com/business/general/2803770/indians-airbnb-bookings-in-thailand-soar)

# **Rumusan Masalah**

>1.  Bagaimana perkembangan Airbnb telah mempengaruhi dinamika pasar akomodasi di Bangkok?

>2. Apa faktor utama yang mendorong peningkatan jumlah wisatawan memesan akomodasi melalui Airbnb, dan bagaimana preferensi akomodasi mereka mempengaruhi strategi pemilik properti dalam menarik tamu?

>3. Apa strategi yang dapat diterapkan oleh pemilik properti di Airbnb untuk tetap kompetitif dalam pasar yang semakin ketat dan dinamis?

# **Data Understanding**
Dataset terdiri atas 17 kolom yang berisi daftar yang berisi informasi `listing` Airbnb yang ada di kota Bangkok dengan kolom utama sebagai berikut:

| **Fitur**                          | **Deskripsi**                            |
|------------------------------------|------------------------------------------|
| **id**                             | Kode unik listing Airbnb.|
| **name**                           | Nama listing.|
| **host_id**                        | Kode unik host Airbnb.                 |
| **host_name**                      | Nama dari host (pemilik) yang menawarkan listing.                     |
| **neighborhood**                   | Lingkungan atau kawasan di Bangkok dimana listing itu berada. |
| **latitude**                       | Garis lintang dari lokasi listing, yang menunjukkan posisi utara-selatan pada peta.                              |
| **longitude**                      | Garis bujur dari lokasi listing, yang menunjukkan posisi timur-barat pada peta.                               |
| **room_type**                      | Jenis kamar yang ditawarkan, misalnya "Entire home/apt" (seluruh rumah/apartemen), "Private room" (kamar pribadi), dan sebagainya. |
| **price**                          | Harga sewa per malam dalam mata uang lokal.|
| **minimum_nights**                 | Jumlah minimal malam untuk menginap dalam listing |
| **number_of_reviews**              | Total jumlah ulasan yang diterima oleh listing dari tamu sebelumnya. |
| **last_review**                    | Tanggal ulasan terakhir yang diterima oleh listing tersebut. |
|**reviews_per_month** | Rata-rata jumlah ulasan yang diterima per bulan.|
| **calculated_host_listings_count** | Jumlah total listing yang dimiliki oleh host tersebut di platform Airbnb.|
| **availability_365**               |  Jumlah hari dalam setahun di mana listing tersebut tersedia untuk dipesan.|
| **number_of_reviews_ltm**          | Jumlah ulasan yang diterima dalam 12 bulan terakhir. |

# **Load Data**
Dataset dapat diakses pada https://drive.google.com/file/d/1c6FJdItxs3SSWrEx5EajEKKd1SgzqJDT/view?usp=drive_link

# **Kesimpulan**
>- Jumlah listing terbanya berada pada area Urban

>- Area urban di Bangkok, seperti Vadhana, Khlong Toei, dan Huai Khwang, mendominasi pasar Airbnb dengan jumlah listing yang signifikan dan tingkat hunian yang tinggi. Ini menandakan bahwa kawasan perkotaan ini merupakan pilihan utama bagi wisatawan.

>- Area suburban dan rural memiliki jumlah listing dan tingkat hunian yang lebih rendah dibandingkan area urban. Namun, terdapat beberapa kawasan suburban, seperti Phra Khanong, yang menunjukkan performa lebih baik. Daerah rural cenderung memiliki performa yang lebih rendah, namun ada listing unik di wilayah ini yang menunjukkan potensi besar.

>- Preferensi Akomodasi: Di wilayah urban, "Entire Home/Apartment" adalah pilihan yang paling populer, sementara di wilayah suburban dan rural, "Private Room" menjadi pilihan dominan. Ini mencerminkan perbedaan preferensi penyewa di berbagai jenis lingkungan, di mana penyewa di area urban cenderung mencari privasi dan kenyamanan.

>- Terdapat perbedaan harga yang signifikan antara wilayah urban, suburban, dan rural. Wilayah urban secara keseluruhan memiliki harga yang lebih tinggi, kecuali untuk shared room di wilayah rural yang memiliki harga yang sangat tinggi. Hal ini menunjukkan adanya fitur unik atau kelangkaan pilihan di daerah tersebut. Harga untuk entire home/apartment yang tinggi di semua wilayah menunjukkan permintaan yang konsisten untuk tipe properti ini.

>- 80% dari harga per listing berada pada harga 3588 baht, sementara rata-rata tarif per malamnya berada pada 1757 baht

# **Rekomendasi Bisnis**
>- Optimalisasi Harga dan Penawaran

Sebaiknya tiap host menetapkan harga yang kompetitif berdasarkan analisis mendalam terhadap tarif rata-rata per listing dan per malam di berbagai Neighbourhood. Pemilik properti dapat menggunakan strategi penetapan harga dinamis yang menyesuaikan tarif berdasarkan permintaan, musim, dan acara lokal, atau menyediakan diskon untuk pemesanan jangka panjang atau menawarkan paket spesial selama musim rendah (low season) untuk menarik lebih banyak tamu. 

Melalui analisa, mayoritas tarif berdasarkan `Neighbourhood` berada di kisaran 80% dari rata-rata tarif per listing adalah 3588 bahtdan rata-rata tarif per malam 1757 Bath. Angka ini dapat dijadikan patokan bagi para host untuk menentukan harga pasar.

>- Kolaborasi dengan Bisnis Lokal

Hasil analisa yang mengerucut pada harga listing tertinggi berada pada area yang jauh dari pusat kota `rural`, namun juga memiliki occupancy hingga 75%, maka sebaiknya host menjalin  kerjasama dengan tempat kuliner, tempat wisata, atau penyedia layanan lokal, bisnis Airbnb Bangkok dapat memberikan customer touchpoint yang berkesan dengan keunikan atau ciri khas area Bangkok. Salah satu caranya adalah dengan mengikuti acara lokal atau festival dengan menawarkan paket khusus yang menggabungkan penginapan dengan akses ke acara-acara tersebut.
    
>- Pemasaran Digital dan Branding

Menargetkan kelompok wisatawan tertentu melalui pemasaran digital, dan membangun merek yang kuat di pasar lokal dan internasional. Misalnya wisatawan backpacker mungkin lebih tertarik pada akomodasi yang terjangkau dan berlokasi dekat dengan tempat-tempat menarik, sementara pelancong bisnis mungkin memprioritaskan fasilitas kerja dan kenyamanan, mementingkan eksklusifitas. Pertimbangan harga rata-rata tarif per malam yang dapat dijadikan patokan adalah:
>- Entire home/apt = 1694 baht
>- Hotel room = 2347 baht
>- Private room = 2044 baht
>- shared room = 958 baht

# **Tableu**
https://public.tableau.com/views/v1_M2_Airbnb_Listings_Bangkok_Irma/Pricedistribution?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link


