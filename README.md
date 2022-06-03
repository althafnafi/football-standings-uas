# :soccer: Football Standings Calculator/Program
## *About*
Proyek ***Football Standings*** ini dibuat sebagai tugas untuk Proyek Akhir Semester (PAS) 2 dari mata kuliah Pemrograman Lanjut Kelas 01 . Berfungsi untuk melakukan kalkulasi dari hasil suatu turnamen dan menunjukkan ranking akhir dalam bentuk tabel. Modifikasi yang diberikan pada program ini adalah penambahan struktur data *binary search tree* yang digunakan untuk ranking *TISS*, yang juga menjadi salah satu poin penilaian untuk PAS semester ini.
 
Program ini dibuat oleh:
1. Adrien Ardra Ramadhan (2106731485)
2. Althaf Nafi Anwar (2106634881)
3. Muhammad Suhaili (2106731535)

## Fungsi
Program ini dapat memudahkan user yang ingin menghitung klasemen dari suatu turnamen bola dengan mudah. Program ini juga memiliki fitur untuk mencatat waktu dan pemain yang mencetak gol jika user menginginkan detail yang lebih pada database klasemennya. Selain itu, dalam program ini juga terdapat suatu *ranking system* yang dapat menilai kualitas dari suatu tim berdasarkan performa mereka pada turnamen-turnamen sebelumnya, yang dinamakan *"Team Index Scoring System"*.

## Fitur
### Menghitung klasemen
Program ini dapat menghitung klasemen dengan mudah, pada menu (1) user akan diminta untuk menginput details dari tim dan gol seperti kapan/siapa yang mencetak gol tersebut. Setelah itu akan muncul tabel yang menunjukkan semua data seperti *Wins*, *Losses*, *Goal Against*, *Goal Difference*, dan masih banyak lainnya. Tabel akan disortir berdasarkan akumulasi poin akhir masing-masing tim, dan tim akan diberi peringkat. Pada menu tabel juga terdapat fungsi untuk mencari berdasarkan nama dan ranking tim, selain itu juga program memiliki fitur untuk melihat detail lebih lanjut pada masing-masing match ataupun turnamen tersebut.

### Melihat klasemen sebelumnya
Pada menu bagian (2), user dapat melihat klasemen-klasemen pada turnamen yang telah diinput sebelumnya.

### Ranking berdasarkan *Team Index Scoring System*
Pada menu ketiga (3), program akan menampilkan ranking dari semua tim yang telah diinput pada program (walaupun berbeda turnamen), dan diurutkan berdsarkan poin yang diperoleh dari sistem penilaian *TISS*. Pada menu ini user dapat meng-*exclude* tim dari klasemen, dan juga diberikan fitur untuk mencari berdasarkan nama dan peringkat tim pada pemeringkatan tersebut.

### *Menu help*
Program ini juga menyediakan menu help pada menu-menu utamanya agar memudahkan user untuk mencari jalannya ataupun mereka yang hanya ingin mencari tahu lebih lanjut tentang fitur-fitur yang ada.

## Cara mengcompile
Masuk terlebih dahulu ke folder src lalu compile programnya
```
cd src
```
```
gcc -Wall -c functions.c && gcc -Wall -c main.c && gcc -o program functions.o main.o && program
```

## Video Penjelasan
<a href="https://www.youtube.com/watch?v=oBVMBGhNN0E" target="_blank">YouTube</a>


## Komponen Penilaian
| No.|            Komponen yang dinilai                | Keterangan |
|---:|                    :---                         |    :--- |
| 1  | Kompleksitas pekerjaan                          |  |
| 2  | Manfaat aplikasi                                | Memudahkan menghitung klasemen |
| 3  | Keunikan ide                                    |   |
| 4  | Penjelasan di Github dan Video                  |   |
| 5  | Error/crash free                                |   |
| 6  | Function dengan argumen berupa address          | **- Function**: *calcStandings, standingsMenu, ...* (hampir semua) |
| 7  | Function dengan argumen berupa array            | **- Function**: *maxLength, search, clearAndPrintHeader, ...* |
| 8  | Function dengan argumen berupa addres ke struct | **- Function**: *sortTeamsByRank, showPrevStandings, ...* (hampir semua) |
| 9  | Function dengan argumen berupa struct           | **- Function**: showMatchDetails |
| 10 | Menambahkan node ke suatu data structure        | Node akan secara otomatis diinsert ketika user selesai menginput data turnamen<br> **- Function**: *insertNode* |
| 11 | Membaca/menghapus node dari suatu data structure| Fitur *exclude* a team from rankings menggunakan deletion<br>**- Function**: *deleteNode (delete), printCombinedRankings (read)* |

## *Functions*
### *showCombinedRankings*
Menampilkan menu ranking berdasarkan *Team Index Ranking System (TISS)*, terdapat opsi untuk mencari tim berdasarkan nama, rank dan juga meng-*exclude* tim dari klasemen
### *printCombinedRankings*
Menampilkan list tim pada klasemen gabungan dengan melakukan traversal secara inorder pada binary search tree
### *helpTISS*
Menampilkan menu help untuk klasemen berdasarkan *TISS*
### *searchNameBst*
Mencari nama pada binary search tree dengan membandingkan string target dengan semua node yang ada pada binary tree
### *searchRankBst*
Mencari tim berdasarkan rank pada binary tree dengan memanfaatkan counter dan inorder traversal
### *newNode*
Membuat node baru dan mereturn addressnya ke caller
### *insertNode*
Melakukan insertion node baru pada binary search tree
### *minValueNode*
Mencari nilai paling kecil pada suatu subtree alias node paling kiri
### *deleteNode*
Menghapus node dari binary tree
### *deallocate*
Mendealokasikan memori yang telah digunakan pada binary search tree
