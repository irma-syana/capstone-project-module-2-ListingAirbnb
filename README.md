### capstone project module 2 AirBnb

# Import libraries
import pandas as pd
import numpy as np
import missingno
import matplotlib.pyplot as plt
import seaborn as sns

from scipy import stats #kolmogorov smirnov
from statsmodels.stats.diagnostic import lilliefors #uji lilliefors
from scipy.stats import shapiro #uji shapiro wilk
from scipy.stats import normaltest #uji D'Agustino Pearson

# **Latar Belakang**

> Airbnb, yang didirikan pada tahun 2008, adalah sebuah platform online yang menghubungkan penyewa akomodasi dengan penyedia tempat hunian, seperti rumah atau apartemen, kamar pribadi, hotel, dan kamar bersama. Kehadiran Airbnb telah mengubah cara orang mencari dan memesan tempat tinggal sementara, dengan pengguna terdiri dari host (pemilik properti) dan guest (tamu).

> Menurut data Airbnb yang dikutip oleh juru bicara pemerintah, jumlah wisatawan India yang memesan akomodasi melalui Airbnb meningkat sekitar 60%. Fitur akomodasi yang paling dicari oleh wisatawan India melalui Airbnb adalah kolam renang, pantai, taman nasional, dan kota-kota terkenal. Persaingan yang semakin ketat juga memaksa pemilik properti untuk lebih kreatif dan strategis dalam menarik tamu.

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


