# Belajar CPP
Mulai: 2024 Oktober 28  
Selesai:   

aku yakin proses belajar ini akan membantu di masa depan.  
Terima kasih untuk situs [Learn C+++](https://www.learncpp.com/)  

## 0.1 Introduction to these tutorials
Mulai: 2024 Oktober 28  
Selesai: 2024 Oktober 28  

pengenalan sekilas mengenai proses belajar di situs. Tidak ada catatan yang penting.  

## 0.2 Introduction to programming languages
Mulai: 2024 Oktober 28  
Selesai: 2024 Oktober 28    

- computer program / application = sekumpulan perintah untuk komputer.
- programming language = bahasa yang digunakan untuk membuat program.
- source code / code = file teks yang berisi sekumpulan perintah untuk komputer.
- running / executing = komputer sedang menjalankan perintah
- CPU hanya dapat memahami bahasa mesin, contoh bahasa mesin adalah 10110000 01100001. 
- binary digit / bit = digit yang terdiri dari 1 dan 0, menyusun bahasa mesin.
- Terdapat beberapa arsitektur CPU, umumnya x86 dan Arm64. Setiap arsitektur CPU memiliki bahasa mesinnya sendiri. Istilah teknisnya adalah ISA (instruction set architecture).
- assembly language = bahasa mesin tetapi menggunakan alfabet. Sehingga lebih mudah dipahami manusia (tapi masih kelihatan susah). Contohnya "mov al, 061h". Instruksi ini berisi perintah menyimpan nilai 061h (97 dalam desimal) ke dalam register al (semacam tempat penyimpanan informasi di CPU)
- assembler = program untuk mengubah assembly menjadi bahasa mesin.
- assembly memiliki kelemahan yg mirip dengan bahasa mesin. Sulit dipahami dan tidak portable (sintaks assembly di x86 berbeda dengan assembly di arm64).
- Bahasa pemrograman baru dikembangkan untuk mengatasi masalah dari bahasa pemrograman lama. 
- low level dan high level languages = kalau rendah, bahasanya mudah dipahami mesin. Contohnya assembly, machine language. Kalau high lebih mudah dipahami manusia seperti python, java, dll. Bahasa yang lebih mudah dipahami manusia, nantinya akan dikonversi menjadi bahasa yang lebih rendah. Proses konversi umumnya dilakukan dengan compiler dan interpreter.
- compiler = C++ menggunakan compiler. Compiler akan mengumpulkan semua perintah di source code, mengubahnya menjadi bahasa mesin dalam bentuk file executablee. File executable dapat dijalankan tanpa compiler dan mudah disebarkan.
- seiring berkembangnya zaman, compiler dapat membuat bahasa assembly atau bahasa mesin yang baik, bahkan mungkin lebih baik dari manusia.
- interpreter = tidak menunggu semua kode selesai ditulis, langsung mengonversi. Efeknya jadi lebih fleksibel tetapi kurang efisien karena mengonversi terus.
- terdapat beberapa contoh arsitektur lain yg disebutkan di diagram seperti MIPS, PowerPC. Intinya high level language bisa dipakai di berbagai arsitektur CPU.
- Beberapa hal yg mungkin mengganggu portabilitas (portability):
    - beberapa OS menyediakan fitur spesifik (tidak portable, tapi terintgrasi dengan baik)
    - beberapa library dari luar (misalnya dari komunitas) terkadang hanya tersedia untuk platform tertentu.
    - compiler menyediakan ekstensi untuk compiler tertentu.
- Sangat disarankan untuk memikirkan portabilitas di awal. Pembelajaran di learncpp juga akan menghindari kode yang tidak spesifik terhadap platform tertentu.


