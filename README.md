# Module 5

## Reflection
1. What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?

   Performance testing dengan JMeter tidak sangat fokus pada internal dari aplikasi atau program, dan sering disebut sebagai metode pengujian blackbox. Hal ini karena JMeter hanya bertugas untuk mengirim permintaan ke endpoint yang telah ditentukan, sesuai dengan jumlah yang diminta pengujinya. JMeter hanya bertindak dengan mengevaluasi apakah permintaan tersebut dapat dijalankan dengan sukses dan mendapatkan respons. Sebaliknya, pendekatan profiling lebih dalam dalam memeriksa proses internal program saat menerima suatu permintaan. Melalui profiling, saya dapat mengidentifikasi bagian mana dari program yang membutuhkan waktu paling lama untuk dieksekusi dibandingkan dengan bagian lain, memungkinkan optimisasi yang lebih efektif terhadap kode.
2. How does the profiling process help you in identifying and understanding the weak points in your application?

   Melalui profiling, saya dapat mengidentifikasi komponen mana dalam program yang memperlambat performa aplikasi secara umum. Ini memungkinkan saya untuk fokus mengoptimalkan komponen tersebut, yang pada gilirannya akan meningkatkan efisiensi keseluruhan aplikasi tanpa harus mengubah banyak aspek lainnya.
3. Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?

   Benar, seperti yang dijelaskan dalam tutorial tersebut, dengan menggunakan Intellij profiler, saya dapat mengungkap bahwa bagian program yang paling memboroskan waktu, misalnya metode getAllStudentWithCourse yang memperlukan loop terlalu berlebih. Profiler ini bahkan memungkinkan saya untuk melihat baris kode mana dalam metode tersebut yang paling mempengaruhi efisiensi metode. Dengan informasi tentang berapa lama waktu yang dibutuhkan untuk menjalankan setiap pemanggilan fungsi, saya menjadi lebih mudah untuk mengidentifikasi komponen mana dalam program yang menjadi hambatan utama bagi kinerja aplikasi secara keseluruhan.
4. What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?

   Kesulitan terbesar yang saya hadapi dalam pengujian performa dan profiling terletak pada kemampuan untuk menginterpretasikan output yang relevan dan mengidentifikasi komponen mana dalam program yang bertindak sebagai penghambat utama. Untuk mengatasi ini, solusinya adalah dengan mempelajari dan memahami hasil output dari JMeter atau profiler secara lebih teliti. Ini mungkin memerlukan waktu untuk terbiasa dengan teknologi baru tersebut agar dapat lebih mudah memahami informasi yang cukup detail.
5. What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?

   Seperti yang telah dibahas sebelumnya, menggunakan profiler dari IntelliJ memungkinkan saya untuk mengidentifikasi komponen program yang mengalami kebuntuan, mengetahui durasi yang dibutuhkan untuk menjalankan sebuah pemanggilan metode, dan menentukan frekuensi pemanggilan metode tersebut. Dengan informasi ini, kita dapat menargetkan area spesifik untuk optimasi dan membedakan mana yang tidak perlu diutak-atik. Penting untuk diingat bahwa "optimasi prematur merupakan sumber segala masalah" karena optimasi yang tergesa-gesa tidak hanya bisa mengurangi keterbacaan kode, tetapi juga dapat menyebabkan komplikasi yang tidak perlu.
6. How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?

Setelah mengerjakan sejauh ini, belum terdapat ke tidak konsistenan dalam hasil performance testing yang dikeluarkan oleh IntelliJ Profiler dengan JMeter. Ini menunjukkan bahwa kedua aplikasi tersebut telah memberikan pandangan yang konsisten tentang bagaimana performa aplikasi dalam konteks pengujian kode saya.

7. What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?
   
Berdasarkan strategi nomor 2, setelah melakukan tes dan profiling, langkah yang saya ambil adalah mengevaluasi durasi yang dibutuhkan oleh program untuk merespons permintaan melalui JMeter. Bila respons terasa lambat, saya akan menggunakan profiler untuk mengidentifikasi bagian kode mana yang menyebabkan penundaan dan kemudian mencari solusi

## Dokumentasi
1. Hasil JMeter GUI sebelum profiling
+ /all-student
<img width="960" alt="all-student request" src="https://github.com/henrysoed/exercise-profiling/assets/119393904/3864e0ec-178a-41ed-a926-2b0de541fc57">

+ /all-student-name
<img width="960" alt="all-student-name request" src="https://github.com/henrysoed/exercise-profiling/assets/119393904/f194b122-fdc2-42d6-af71-bdf14cd81a2a">

+ /highest-gpa
<img width="960" alt="highest-grade request" src="https://github.com/henrysoed/exercise-profiling/assets/119393904/357313e4-0f38-4968-962e-e78ad3a849f6">

2. Hasil JMeter CLI sebelum profiling
+ /all-student
![1-before](https://github.com/henrysoed/exercise-profiling/assets/119393904/c908661c-6cf8-4cfe-839a-74febca795bc)

+ /all-student-name
![2-before](https://github.com/henrysoed/exercise-profiling/assets/119393904/7d1d6c71-e9b3-4a56-a919-e44a30dacce9)

+ /highest-gpa
![3-before](https://github.com/henrysoed/exercise-profiling/assets/119393904/d7dd213a-7588-47e2-9edc-f4d8ff710df7)

3. Hasil JMeter CLI setelah profiling
+ /all-student
<img width="953" alt="1-after" src="https://github.com/henrysoed/exercise-profiling/assets/119393904/82966a67-e5a4-42eb-9195-04693b2f64f4">

+ /all-student-name
<img width="960" alt="2-after" src="https://github.com/henrysoed/exercise-profiling/assets/119393904/ed7cbd56-3ac5-4c97-892f-2183e0991e77">

+ /highest-gpa
<img width="955" alt="3-after" src="https://github.com/henrysoed/exercise-profiling/assets/119393904/ae488b09-5bef-4732-94cc-2377c2e24f28">
