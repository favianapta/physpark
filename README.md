# physpark

<a name="readme-top"></a>

# System Commands Return Code
  - Kode tersebut menggunakan library sys.process di Scala untuk menjalankan perintah shell, dengan variabel res yang menampung hasil perintah "ls /tmp", kemudian cetak output dengan nilai variabel res, yang akan berupa 0 jika perintah berhasil dan non-0 jika gagal.
  
![images]( images/Executing_system.png )

# System Commands Output

![images]( images/SystemCommandsOutput.png )

# BroadCast

![images]( images/BroadCast.png )

   - broadcast <br>
     Penjelasan :
     ```sh
     untuk mengirim variabel yang tidak berubah (immutable) ke setiap worker node hanya sekali, 
     sehingga menghemat penggunaan memori dan waktu komputasi.
     ```
     
   - list <br>
     Penjelasan :
     ```sh
     tipe data di Python yang digunakan untuk menyimpan kumpulan data dalam satu variabel.
     ```
     
   - range <br>
     Penjelasan :
     ```sh
     fungsi bawaan di Python yang digunakan untuk membuat urutan bilangan bulat 
     dengan parameter awal, akhir, dan increment.
     ```

# Accumulator

![images]( images/Accumulator.png )

   - sc <br>
     Penjelasan :
     ```sh
     objek SparkContext yang digunakan untuk menghubungkan kode Python dengan mesin Spark.
     ```
     
   - accumulator <br>
     Penjelasan :
     ```sh
     fitur di Apache Spark yang digunakan untuk mengumpulkan nilai-nilai dari 
     setiap worker node yang menjalankan sebuah operasi tertentu pada sebuah RDD.
     ```
     
   - parallelize <br>
     Penjelasan :
     ```sh
     method pada objek SparkContext yang digunakan untuk membuat sebuah RDD 
     dari data yang sudah ada pada driver program.
     ```
     
   - lambda <br>
     Penjelasan :
     ```sh
     fitur di Python yang digunakan untuk membuat sebuah fungsi tanpa harus 
     menentukan nama fungsi secara eksplisit.
     ```
     
   - value <br>
     Penjelasan :
     ```sh
     method pada objek Accumulator yang digunakan untuk mengambil nilai akhir dari 
     sebuah accumulator setelah diisi dengan nilai-nilai dari RDD.
     ```
<p align="right">(<a href="#readme-top">back to top</a>)</p>

# PairRDD

![images]( images/PairRDD.png )

- map <br>
     Penjelasan :
     ```sh
     operasi yang diterapkan pada RDD, yang mengubah setiap elemen RDD menjadi 
     elemen baru dengan mengikuti suatu fungsi tertentu.
     ```
     
- collect <br>
     Penjelasan :
     ```sh
     operasi yang mengembalikan seluruh elemen dari RDD ke driver program sebagai array atau list.
     ```
     
- len <br>
     Penjelasan :
     ```sh
     fungsi yang mengembalikan jumlah karakter dalam sebuah string.
     ```
     
- keys <br>
     Penjelasan :
     ```sh
     operasi yang mengembalikan kumpulan kunci dari setiap pasangan kunci-nilai dalam Pair RDD.
     ```
     
- values <br>
     Penjelasan :
     ```sh
     operasi yang mengembalikan kumpulan nilai dari setiap pasangan kunci-nilai dalam Pair RDD.
     ```
     
    
# Log Analytics

![images]( images/LogAnalytics.png )

   - textFile <br>
     Penjelasan :
     ```sh
     untuk membaca file teks dan mengubahnya menjadi RDD (Resilient Distributed Dataset) di Spark.
     ```
     
   - filter <br>
     Penjelasan :
     ```sh
     untuk menyaring elemen RDD dengan kriteria tertentu dengan menggunakan sebuah fungsi lambda.
     ```
     
   - cache <br>
     Penjelasan :
     ```sh
     untuk menyimpan RDD di memori, sehingga RDD tersebut bisa digunakan 
     kembali tanpa harus dibaca ulang dari sumbernya.
     ```
     
   - count <br>
     Penjelasan :
     ```sh
     untuk menghitung jumlah elemen dalam RDD. Fungsi ini merupakan tipe action di Spark, 
     yang mengakibatkan Spark menjalankan komputasi dan mengembalikan hasil ke driver program.
     ```

# Understanding RDDs

![images]( images/UnderstandingRDD.png )

   - defaultParallelism <br>
     Penjelasan :
     ```sh
     variabel yang mengembalikan jumlah default dari partisi RDD yang dibuat di SparkContext.
     ```
     
   - getNumPartitions <br>
     Penjelasan :
     ```sh
     method yang digunakan untuk mengembalikan jumlah partisi dari RDD.
     ```
     
   - mapPartitionsWithIndex <br>
     Penjelasan :
     ```sh
     method yang mengembalikan RDD baru dengan menerapkan fungsi pada setiap partisi, 
     dengan mempertahankan indeks partisi.
     ```
     
   - repartition <br>
     Penjelasan :
     ```sh
     method yang digunakan untuk menyeimbangkan kembali data pada RDD dengan mengubah jumlah partisi.
     ```
     
   - coalesce <br>
     Penjelasan :
     ```sh
     method yang digunakan untuk mengurangi jumlah partisi RDD dengan menggabungkan partisi 
     yang saling berdekatan menjadi satu.
     ```
     
   - toDebugString <br>
     Penjelasan :
     ```sh
     method yang digunakan untuk mengembalikan deskripsi teks dari RDD, 
     termasuk informasi tentang partisi, ketergantungan, dan transformasi yang dijalankan pada RDD.
     ```

# WordCount

![images]( images/WordCount.png )

- flatMap <br>
     Penjelasan :
     ```sh
     sebuah operasi pada RDD di Spark yang bertujuan untuk mengekspansi baris RDD dengan memisahkan setiap baris 
     menjadi kata-kata terpisah berdasarkan separator yang ditentukan, sehingga setiap kata yang diperoleh kemudian 
     akan dijadikan elemen yang berbeda-beda pada RDD baru. Pada kode di atas, operasi flatMap digunakan untuk 
     memisahkan setiap baris dalam RDD lines menjadi kata-kata terpisah dengan separator spasi (' ').
     ```
     
   - reduceByKey <br>
     Penjelasan :
     ```sh
     merupakan sebuah operasi pada RDD di Spark yang bertujuan untuk mengelompokkan pasangan kunci-nilai 
     berdasarkan kunci, dan kemudian menjumlahkan nilai-nilai yang sesuai dengan kunci yang sama. Dalam kode di atas, 
     operasi reduceByKey digunakan untuk menjumlahkan nilai 1 yang dihasilkan oleh operasi map pada setiap kunci kata yang sama, 
     sehingga menghasilkan jumlah kemunculan kata tersebut pada RDD yang dihasilkan.
     ```
     
   - split <br>
     Penjelasan :
     ```sh
     merupakan sebuah fungsi bawaan Python yang digunakan untuk memisahkan sebuah string menjadi beberapa bagian, 
     berdasarkan separator yang ditentukan. Pada kode diatas, fungsi split digunakan untuk memisahkan setiap baris 
     RDD lines menjadi kata-kata terpisah dengan separator spasi (' '), sehingga setiap kata tersebut kemudian 
     dijadikan elemen pada RDD baru setelah dilakukan operasi flatMap.
     ```
