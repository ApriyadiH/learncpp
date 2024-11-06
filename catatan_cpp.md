# Belajar CPP
Mulai: 2024 Oktober 28  
Selesai:   

Aku yakin proses belajar ini akan membantu di masa depan. Tidak tau butuh berapa lama, aku harap dibawah 6 bulan.  
Beberapa bagian ditulis __PELAJARI ULANG__ yang akan dipelajari kembali nanti.
Terima kasih untuk situs [Learn C+++](https://www.learncpp.com/)  

## 0 Introduction / Getting Started
Mulai: 2024 Oktober 28  
Selesai: 2024 November 6  

### 0.1 Introduction to these tutorials
Mulai: 2024 Oktober 28  
Selesai: 2024 Oktober 28  

pengenalan sekilas mengenai proses belajar di situs. Tidak ada catatan yang penting.  

### 0.2 Introduction to programming languages
Mulai: 2024 Oktober 28  
Selesai: 2024 Oktober 28    

- computer program (application) = sekumpulan perintah untuk komputer.
- programming language = bahasa yang digunakan untuk membuat program.
- source code (code) = file teks yang berisi sekumpulan perintah untuk komputer.
- running (executing) = komputer sedang menjalankan perintah
- CPU hanya dapat memahami bahasa mesin, contoh bahasa mesin adalah 10110000 01100001. 
- binary digit (bit) = digit yang terdiri dari 1 dan 0, menyusun bahasa mesin.
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

### 0.3 Introduction to C/C++
Mulai: 2024 Oktober 28  
Selesai: 2024 Oktober 29    

- Dijelaskan sejarah singkat C, C++ merupakan pengembangan dari C. 
- C dikembangkan tujuan minimalis, mudah di-compile, akses memori yg efisien, cukup high level dan portabilitas. Mungkin pada saat itu dianggap high level, tetapi setauku C dianggap mid level bagi beberapa orang. 
- buku "The C Programming Language" atau disebut juga buku K&R menjadi panduan untuk mencapai portabilitas maksimum karena compiler pada saat itu umumnya mengikuti standar ini.
- Kemudian standar tersebut dikembangkan lagi oleh ANSI dan disebut C89. Lalu ISO juga membuat standar dan disebut C90. Kemudian menjadi C99.  
- Dari sumber lain, aku ada ketemu C memiliki standar lain seperti C11, C17 dan C23. Angka diakhir menunjukkan rencana tahun dirilisnya standar tersebut. Misalnya C23 selesai dibuat tahun 2022. Namun hingga 2024, draft standar masih dianggap dalam proses. Standar tsb masih disebut C23.
- C++ dibuat tahun 1979, pada saat itu belum ada standar dan hanya ada buku K&R. C++ bisa dianggap seperti C dengan fitur tambahan. Namun tidak selalu begitu karena setelah beberapa saat misalnya C99, C memiliki fitur yang tidak dimiliki C++.
- Standar C++ dimulai tahun 1998. Kemudian muncul berikutnya dan disebut C++03, C++11, C++17, C++20 dan C++23. 
- Penjelasan yg diberikan learncpp mengenai kelebihan C++ adalah Object untuk OOP (Object oriented programming). Rasanya kurang lengkap, setelah saya cari tahu lebih lanjut. C++ lebih baik untuk hal yang lebih kompleks. Dari video yang sering aku temui, orang yang ahli dapat melakukan optimasi dan sejauh ini paling cepat melakukan operasi yang kompleks. Salah satu motivasi saya mempelajari C++. Namun perlu diketahui, realitanya mungkin kebanyakan orang akan beralih menuju No-Code, orang tidak lagi memikirkan sintaks tetapi meminta Ai untuk menulis kode. Optimasi juga menjadi tidak penting ketika kapasitas prosesor, RAM dan kecepatan internet berkembang. Sehingga kode yang tidak efisien tetapi cepat dibuat akan jauh lebih bernilai dari kode yang optimal namun perlu waktu pengembangan yang lama. Memikirkan algoritma yang optimal memerlukan waktu.
- filosofi "trust the programmer" = filosofi yang memberikan kendali penuh kepada programmer. Intinya kamu dibebaskan berjalan, namun C++ tidak akan peduli jika kamu berjalan ke arah yang salah atau jatuh ke lubang. Bahasa pemrograman lain akan membatasi akses ke memori dan melakukannya secara otomatis. Sehingga seharusnya tidak terjadi masalah. 
- Kelebihan C++ 
    - game
    - sistem real time
    - aplikasi yang butuh performa tinggi 
    - aplikasi grafis 
    - dll 
- Dari learncpp, diseebutkan C++ termasuk top 3 bahasa populer yang menggunakan compiler. Secara umum (termasuk scripting dan mengabaikan HTML, SQL, Bash) biasanya masuk juara 5 atau 6. Dari survey yang aku lihat, bahasa yang populer secara umum adalah Python, Java, JS. Sekedar pemahaman ini informasi yang aku dengar, sebagian mungkin salah karena aku belum mendalami beberapa. Alasan kenapa beberapa bahasa bertahan:
    - JS: semua browser web distandarisasi dengan Javascript. Sehingga bahasa ini tidak mungkin hilang selama pc dan internet masih digunakan. Hp juga bisa mengakses web. 
    - Python: sangat high level, mudah digunakan. Penggunanya kebanyakan mungkin bukan berasal dari orang yang pekerjaan tetapnya jadi programmer tetapi dari kalangan profesi lain. Misalnya org teknik, ilmuwan, data, peneliti. Sehingga mampu bertahan dan tetap populer.
    - Java: Java menawarkan JVM. JVM mempermudah portabilitas. Jadi berbagai platform bisa menginstall JVM. Semua program dengan Java dapat berjalan di JVM. Banyak yang sudah ketergantungan dengan JVM. Kalau sudah masuk dunia IT atau sering menginstall aplikasi/game, pasti akan menemukan kasus ketika aplikasi memerlukan instalasi Java versi tertentu.
    - C#: dikembangkan microsoft
    - C++: unggul soal adu kecepatan
    - PHP: sepertinya ini mulai ditinggalkan, mungkin di Indo masih akan populer beberapa saat. PHP memiliki keunggulan di bagian backend. Dulu front-end hanya sekedar tampilan. Tetapi seiring berkembangnya library JS, sepertinya orang akan lebih memilih JS. Di web, perang akan berlangsung antar library/framework. Misalnya antara Vue, Angular dan React. Para developer pasti lebih memilih bahasa yang lebih populer. Ketika bingung lebih mudah bertanya.
    - Golang: dikembangkan google 
    - Rust: sepertinya sangat mirip C++ kecuali bagian filosofi "trust the programmer". Namun fitur pengaman tsb dapat dihilangkan sehingga menjadi mirip C++ juga. Dari survey, sepertinya sangat disukai selama 8 tahun. Untuk orang yang belajar C++ mungkin kalau pindah bakalan ke Rust. Katanya lumayan mirip juga sintaksnya.
    - Swift: utk hp iphone. dikembangkan apple 
- Sebelum memulai tulisan ini, aku juga mempertimbangkan bahasa mana yang akan dipelajari lebih mendalam. Kandidat yang kelihatannya menarik adalah Java, Rust dan C++. Python dan JS sudah pernah aku gunakan sehingga sepertinya akan lebih mudah mengembangkannya lebih lanjut sesuai kebutuhan. Pertimbanganku sekedar C++ cepat dan lebih low level. Seharusnya setelah belajar C++, aku akan lebih mudah belajar Java ataupun Rust.

### 0.4 Introduction to C++ development
Mulai: 2024 Oktober 29  
Selesai: 2024 Oktober 29    

- Alur pembuatan program. Prosedurnya seperti ini 
    - Menentukan masalah yang ingin diselesaikan
    - Memikirkan proses penyelesaian masalah
    - Mulai koding
    - compile 
    - link object files 
    - test dan debug 
- Terkadang terdapat beberapa cara untuk menyelesaikan masalah. Penting untuk memikirkan solusi terbaik sebelum memulai. Ciri2 solusi yang baik:
    - simpel 
    - terdokumentasi rapi
    - modular, dapat digunakan kembali
    - ada error handling
- bug = kesalahan yang muncul dan mencegah program berjalan sesuai rencana. 
- debugging = proses memperbaiki / menghilangkan bug.
- learncpp menyarankan untuk menggunakan program khusus yang membantu proses penulisan kode. Yang paling terkenal secara umum adalah VS Code. Saya juga menggunakan VS Code. Tulisan selanjutnya juga berfokus pada VS Code. 
- Terdapat beberapa kelebihan program khusus code editor seperti:
    - line numbering (setiap baris dikasih nomor, berguna untuk menunjukkan posisi error)
    - highlight dan warna, VS Code akan memberikan warna khusus untuk variabel, warna khusus untuk nilai, dll
    - font khusus (monospace), sehingga mempermudah proses membaca
    - VS Code juga menyediakan beragam extension yang dapat membantu proses pengembangan, misalnya auto complete.
- tidak terdapat aturan penamaan, namun umumnya program utama disimpan dengan nama "main.cpp". Terkadang menggunakan nama yang mudah dipahami seperti "calculator.cpp". Terkadang menggunakan ekstensi yang berbeda seperti ".cc" atau ".cxx".

### 0.5 Introduction to the compiler, linker, and libraries
Mulai: 2024 Oktober 29  
Selesai: 2024 Oktober 29    

- compiler umumnya melakukan 2 hal: 
    - memeriksa kode dan memberikan error jika tidak sesuai aturan penulisan. 
    - mengubah bahasa C++ menjadi bahasa mesin. 
- object file = bahasa C++ akan diubah menjadi bahasa mesin. Peerintah untuk komputer akan disimpan dalam object file. Object file menggunakan ekstensi ".o" dengan nama file yang sesuai dgn file sumber. Misalnya "main.cpp" menjadi "main.o"
- linker = mengumpulkan semua object file dan mengubahnya menjadi executable. Proses tsb disebut linking. 
- linker bertugas untuk menyambungkan object file, kemudian memastikan semua file yang terhubung akan saling terhubung dengan baik. Selain itu juga bisa menghubungkan library. 
- C++ memiliki standard library, library yang sudah disediakan oleh C++. Diluar itu, programmer juga dapat menggunakan library buatan orang lain. 
- Building = proses mengubah kode menjadi executable secara keseluruhan. 
- Ada disebutkan tools yang umum digunakan seperti "make" dan "build2", tetapi karena bukan hal yang wajib dan bukan inti utama bahasa C++, learncpp tidak akan membahasnya. saya tambahkan tulisan ini untuk dicari kembali di masa depan. __PELAJARI ULANG__
- Integrated development environnments (IDEs) = Proses pengembangan seperti penulisan kode, compiling, linking, dan debugging dapat dilakukan di program yang terpisah. Namun bisa juga di satu program yang biasanya disebut IDE, contohnya VS Code. 

### 0.6 Installing an Integrated Development Environment (IDEs)
Mulai: 2024 Oktober 29   
Selesai: 2024 Oktober 29     

- learncpp menyarankan untuk IDE yang mengikuti setidaknya standar C++17. 
- learncpp menyarankan Visual Studio untuk Windows. Btw Visual Studio berbeda dengan VS Code. Saya yakin alasan VS disarankan karena mudah diinstal. 
- learncpp juga menyarankan Code::Blocks untuk Linux dan Windows. Dulu saya menggunakan ini ketika kuliah. 
- Terakhir disarankan juga VS Code untuk yang sudah berpengalaman. Tidak disarankan untuk pemula karena sulit diinstall.
- Tulisan ini akan menggunakan VS Code, saya sudah menggunakan VS Code utk bahasa lain seperti python dan JS. Sehingga malas menggantinya, VS juga berat, Codeblocks terbatas pada C dan C++. Silahkan cari video tutorialnya sendiri di youtube. Kurang lebih yang kalian perlukan adalah sebagai berikut:
    - Compiler, misalnya MinGW lewat situs source forge atau G++ lewat msys2.org. Dulu aku pakai MinGW tapi karena versinya C++17, aku coba ganti ke msys versinya lebih baru. Tutorial Youtube biasanya ngarahin ke MinGW. Panduan Msys bisa tinggal cek situsnya dan ikutin petunjuknya. Msys kurang menjelaskan soal pengaturan environment variables, jadi jgn lupa tambahkan Path ke folder bin compiler G++. 
    - Extension VS Code "C/C++" (yg ini biasanya disarankan secara otomatis oleh VS Code)
    - Extension VS Code "code runner". Ini perlu kalau ikuttin tutorial mingw.
- IDE lain sudah otomatis memiliki compiler yang dibutuhkan sehingga proses instalasi lebih mudah dan lebih disarankan untuk pemula. 
- Terdapat juga beberapa alternatif misalnya ngoding di Handphone atau menggunakan IDE berbasis web. Namun saya tidak tahu fitur apa saja yang terbatas. Seharusnya untuk hal yang sederhana akan aman. 

### 0.7 Compiling your first program 
Mulai: 2024 Oktober 29  
Selesai: 2024 Oktober 29   

- Projects = container keseluruhan untuk menampung kode, gambar, data lainnya. Aku belum terlalu mendalami docker/kubernetes. Tapi mungkin learncpp sengaja menggunakan istilah container karena ingin mengarah kesana. Tapi seharusnya bisa berupa folder atau repository. Sebaiknya belajar Git juga.
- disarankan membuat project untuk setiap program baru. 
- console projects = project untuk membuat program yang dapat berjalan di console Windows, Linux dan Mac. Console itu  contohnya Command prompt.
- workspace = kontainer yang lebih besar. Menyimpan beberapa project sekaligus. 
- Build = compile semua kode yang berubah (modified), linking jadi executable.
- Clean = menghilangkan semua cached object dan executables. Berikutnya kalau di build ulang semua akan di compile, linking, dan dihasilkan executable.
- Rebuild = clean lalu Build.
- Compile = recompile 1 kode file. Terlepas dari di modified atau nggak. Tidak dilanjutkan dengan linker dan tidak menghasilkan executable.
- Run/Start = menjalankan executable. Beberapa IDE ulang build.
- Biasanya orang milih Build dan Run
- Di VS Code, aku menggunakan Run.

### 0.8 A few common C++ Problems
Mulai: 2024 Oktober 29  
Selesai: 2024 Oktober 29    

- berisi beberapa masalah yang umum terjadi. Di sini ditulis dalam bentuk tips 
- terkadang program langsung dimatikan ketika selsai. Dapat ditambahkan pause atau menunggu input user. Selama menunggu, kita dapat melihat hasil. Hal ini sangat berguna untuk proses debugging. 
- Di VS Code kode dapat dijalankan dan langsung melihat hasil. Kalau buka .exe langsung tertutup setelah menjalankan semua perintah.
- terkadang antivirus menghilangkan output. Dalam kasus ini mungkin antivirus dapat dimatikan sementara. 
- semua program harus memiliki fungsi main(), fungsi main() hanya boleh berjumlah 1, tidak boleh lebih. 
- undeclared identifier = pesan error yang muncul ketika menggunakan sintaks dari library tertentu, tetapi librarynya tidak di-include. Di VS Code, pesan errornya tidak menyebutkan undeclared identifier.

### 0.9 Configuring your compiler: Build Cofigurations
Mulai: 2024 Oktober 29  
Selesai: 2024 November 5  

- build configuration (build target) = pengaturan untuk building project.
- settingannya umumnya dibiarkan dalam default, kecuali diperlukan. 
- terdapat 2 configuration.
    - debug configuration = mematikan optimisasi, menampilkan informasi debug.
    - release configuration = ada optimasi, ukuran dan performa baik. tidak ada pesan debug.
- Di awal, ntah kenapa ketika aku coba petunjuk dari learncpp, ukuran file hello worldnya sama aja. Sekitar 62KB. berdasarkan learncpp, kalau build debug ukurannya besar sektiaran 65KB dan release sekitaran 12KB. Jadi mungkin yg berhasil aku buat versi debug. Tapi ada lihat2 tutorial lain untuk versi release bisa pakai CMake extension tools.
- Kemudian aku coba2 lagi, dapatnya 18,5 KB dan 131 KB. Di build dgn command line 
    - untuk debug
    ```
    g++ main.cpp -o main
    ```
    - untuk release
    ```
    g++ -O3 -s -DNDEBUG your_code.cpp -o output_executable_name
    ```

### 0.10 Configuring your compiler: Compiler extensions
Mulai: 2024 November 5  
Selesai: 2024 November 5   

- compiler extensions = compiler mungkin memiliki perubahannya sendiri untuk kelebihan tertentu. learncpp memberikan contoh berupa kompatibilitas dengan standar lama. Tapi setelah aku cari tahu lagi, ada banyak manfaat lain seperti meningkatkan performa, fitur baru, fitur spesifik. Efeknya ada kelebihan tetapi mungkin kurang universal pada compiler lain atau tidak sesuai standar terbaru.
- fitur compiler extensions ini juga secara bawaan sudah diaktifkan, efeknya mungkin membuat pemula tidak sadar bahwa fitur yang dia gunakan bukanlah fitur yang standar.
- learncpp menganjurkan untuk mematikan fitur compiler extensions. 

### 0.11 Configuring your compiler: Warning and error levels
Mulai: 2024 November 5  
Selesai: 2024 November 5   

- diagnostic message (diagnostic) =  compiler diwajibkan mengirimakan diagnostic message ketika terjadi error. Tetapi format penulisan pesan tidak diatur dalam standar.
- error = kerusakan akibat kesalahan penulisan sehingga compiler gagal melakukan compiling. Pesan diagnostic disertai dengan angka baris error, hal yang seharusnya ada dan apa yang ditemukan.
- warning = terdapat kesalahan, namun proses compiling tetap berjalan hingga selesai. Dari pengalamanku biasanya terjadi jika ada variabel yang tidak digunakan.
- learncpp menyarankan untuk selalu membereskan warning.
- di kasus yang jarang terjadi, pesan warning perlu dimatikan. C++ secara bawaan tidak menyediakan fitur untuk mematikan pesan warning tetapi compiler biasanya ada. 
- warning levels = compiler memiliki tingkat peringatan. Semakin tinggi maka kesalahan yang kecil akan ditulis. learncpp menyarankan untuk menaikkan warning levels setinggi mungkin terutama ketika belajar.

### 0.12 Configuring your compiler: Choosing a language standard 
Mulai: 2024 November 6  
Selesai: 2024 November 6  

- seperti yang dibahas sebelumnya, C++ memiliki beberapa standar. Biasanya yang dipilih adalah 2 versi sebelum versi terbaru. Hal ini memberikan waktu untuk pembuat compiler membuat compiler versi stabil. 
- Saran learncpp ketika belajar sebaiknya pakai standar terbaru. Ini cukup masuk akal karena setelah selesai belajar, mungkin standar yang dipelajari menjadi standar yang paling umum untuk digunakan.
- Jadi kurang lebih prosedur seperti ini
    - Download compiler dari [msys](https://www.msys2.org/#installation) 
    - ikuti tahapan instalasi
    - tambahkan settingan environment variables ke folder bin
    - lalu edit file tasks.json
    ```
    {
	    "version": "2.0.0",
	    "tasks": [
	        {
		        "label": "build_debug",
                "type": "shell",
                "command": "g++",
                "args": [
                    "-fdiagnostics-color=always",
                    "-ggdb",
                    "-pedantic-errors",
                    "-Wall",
                    "-Weffc++",
                    "-Wextra",
                    "-Wconversion",
                    "-Wsign-conversion",
                    "-std=c++23",
                    "${workspaceFolder}\\${fileBasenameNoExtension}.cpp", 
                    "-o",
                    "${workspaceFolder}\\${fileBasenameNoExtension}_debug.exe"  
		        ],
		        "group": {
    		        "kind": "build",
		            "isDefault": true
		        }
	        },
	        {
                "label": "build_release",
                "type": "shell",
                "command": "g++",
                "args": [
                    "-fdiagnostics-color=always",
                    "-g",
                    "-O2",
                    "-DNDEBUG",
                    "-pedantic-errors",
                    "-Wall",
                    "-Weffc++",
                    "-Wextra",
                    "-Wconversion",
                    "-Wsign-conversion",
                    "-std=c++23",
                    "${workspaceFolder}\\${fileBasenameNoExtension}.cpp", 
                    "-o",
                    "${workspaceFolder}\\${fileBasenameNoExtension}_release.exe" 
                ],
                "group": {
                    "kind": "build"
                }
	        }
	    ]
    }
    ```
    - Lalu edit file launch.json
    ```
    {
        "version": "0.2.0",
        "configurations": [
            {
                "name": "Debug Custom",
                "type": "cppdbg",
                "request": "launch",
                "program": "${workspaceFolder}\\${fileBasenameNoExtension}_debug.exe", 
                "args": [],
                "stopAtEntry": false,
                "cwd": "${workspaceFolder}",
                "environment": [],
                "externalConsole": false,
                "MIMode": "gdb",
                "setupCommands": [
                    {
                    "description": "Enable pretty-printing for gdb",
                    "text": "-enable-pretty-printing",
                    "ignoreFailures": true
                    }
                ],
                "preLaunchTask": "build_debug",
                "miDebuggerPath": "C:\\Appplikasi\\Compiler cpp\\ucrt64\\bin\\gcc.exe", // ini disesuaikan dengan lokasi bin
                "logging": {
                    "engineLogging": false
                }
            },
            {
                "name": "Release Custom",
                "type": "cppdbg",
                "request": "launch",
                "program": "${workspaceFolder}\\${fileBasenameNoExtension}_release.exe",  
                "args": [],
                "stopAtEntry": false,
                "cwd": "${workspaceFolder}",
                "environment": [],
                "externalConsole": false,
                "MIMode": "gdb",
                "setupCommands": [
                    {
                        "description": "Enable pretty-printing for gdb",
                        "text": "-enable-pretty-printing",
                        "ignoreFailures": true
                    }
                ],
                "preLaunchTask": "build_release",
                "miDebuggerPath": "C:\\Appplikasi\\Compiler cpp\\ucrt64\\bin\\gcc.exe", // disesuaikan dengan lokasi compiler
                "logging": {
                    "engineLogging": false
                }
            }
        ]
    }
    ```
    - sisanya tinggal run code kalau mau lihat hasil, run file untuk build versi debug atau versi release
- satu hal yang aku perhatiin, argumen compiler "-s" dapat secara signifikan mengecilkan ukuran file. Misalnya dgn -s ukurannya bisa menjadi 18KB. Lalu tanpa -s hasilnya 140an KB. -s katanya menghilangkan simbol dan efeknya susah di reverse engineering.

### 0.13 What language standard is my compiler using?
Mulai: 2024 November 6  
Selesai: 2024 November 6    

- bagian ini learncpp menyediakan kode untuk memeriksa hasil.
- file disimpan dengan nama "PrintStandard.cpp"
- hasilnya kalau dijalankan jadi C++17, tapi kalau dicompile jadi release dan build, hasilnya C++23. Agak aneh dan aku gk tau cara mengubah versi singkat run. Untuk saat ini dianggap aman aja.

## 1 