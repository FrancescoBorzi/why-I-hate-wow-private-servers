# Mengapa saya benci kebanyakan pelayan peribadi WoW

*Ditulis oleh Francesco Borzi' aka Shin*

Mengapa masih terdapat banyak bug di pelayan peribadi WoW, walaupun telah wujud bertahun-tahun?

![Wow-facepalm](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-facepalm.jpeg)

Jangan risau, ini bukan kuliah hak cipta yang biasa mengenai Blizzard.
Saya hanya ingin menjelaskan mengapa saya benci sebahagian besar pelayan peribadi [World of Warcraft](https://en.wikipedia.org/wiki/World_of_Warcraft)'

## Pengenalan

Saya terpesona dengan penyamaan WoW sejak saya berusia 14 tahun. Saya masih ingat lagi pertama kali saya menyertai salah satu "alam istimewa" ini, terdapat banyak bug, tetapi sekurang-kurangnya anda boleh bermain secara percuma. Anda tahu, saya tidak mempunyai satu sen pun ketika itu, jadi saya tidak mempunyai alternatif. 

Pada usia 15 tahun saya mula bertanya-tanya bagaimana pelayan peribadi benar-benar berfungsi dan boleh wujud, terutama dari perspektif teknikal. Mungkin ada seseorang yang mencuri kod dari [Blizzard](https://en.wikipedia.org/wiki/Blizzard_Entertainment)? Saya tidak tahu - saya begitu muda dan tidak berpengalaman pada masa itu! Walaupun begitu, saya mula bermain-main dan dengan bantuan rakan lama saya (Fabio), saya akhirnya berjaya memasang pelayan WoW pada PC saya sendiri.

Ketika itu saya tidak dapat membayangkan kepuasan yang saya dapat dan berapa banyak perkara yang akan saya pelajari berkat dunia ajaib ini.

Ini mungkin kedengaran pelik, tetapi dunia ini masih menarik perhatian saya sampai sekarang sebagai orang dewasa, sehingga saya mendedikasikan keseluruhan [Tesis Sarjana dalam Sains Komputer untuk topik ini](https://community.trinitycore.org/topic/13025-just-thank-you-wow-emulation).

![wow-emulation-thesis](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-emulation-thesis.jpeg)

Tetapi masih: **Saya benci kebanyakan pelayan peribadi dan saya benar-benar ingin menjelaskan mengapa.**

## Beberapa istilah teknikal

![Wow-sleeping](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-sleeping.jpg)

Untuk membuat anda memahami pandangan saya, saya perlu menjelaskan kurungan teknikal kecil mengenai proses kerja WoW, yang akan saya cuba jelaskan dengan kata-kata mudah.

### Bagaimana World of Warcraft yang asal berfungsi

Pada peringkat perisian, terdapat dua program yang dapat dianggap sebagai pelakon utama permainan ini:

- **APLIKASI KLIEN** - yang merupakan program "World of Warcraft" sebenar yang dipasang oleh setiap pemain di komputer mereka untuk mengakses permainan.

- **APLIKASI PELAYAN**: yang merupakan program yang dijalankan pada mesin pelayan.

Prosesnya sangat mudah: semua Klien (pemain) menyambung ke Pelayan untuk berinteraksi antara satu sama lain. Klien mengetahui alamat pelayan kerana disimpan di dalam fail "**realmlist.wtf**" yang terkenal (sebab itulah anda harus mengubah suai fail ini untuk beralih ke pelayan lain).

![Client-server](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/client-server.png)

### Bagaimana pelayan peribadi WoW berfungsi

Semasa bermain di pelayan peribadi, prinsipnya sama. Perbezaannya terletak pada perisian yang anda gunakan.

![Wow-Defias](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-defias.jpg)

**KLIEN**. Setiap orang mempunyai akses kepada klien World of Warcraft yang asal. Anda boleh mendapatkannya dengan mudah dengan membelinya atau memuat turunnya dalam talian. Program ini adalah sama dengan program yang akan anda gunakan untuk bermain di pelayan rasmi. Jelas pelayan peribadi yang berbeza mempunyai versi klien yang berbeza, tetapi mereka selalu merujuk kepada klien asal. Anda hanya perlu membuat sedikit perubahan pada fail "realmlist.wtf", menggantikan alamat alamat pelayan runcit dengan alamat pelayan peribadi. Itu sahaja.

**PELAYAN**. Ini sama sekali berbeza. Tidak ada orang di luar Blizzard yang mempunyai akses ke perisian asal yang menjalankan pelayan World of Warcraft rasmi. Jadi aplikasi ini sama sekali berbeza dengan yang asli.

### Kejuruteraan balikan

![Reverse engineering](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/reverse-engineering.jpeg)

Setiap perisian yang menjalankan pelayan peribadi telah dibuat melalui teknik "kejuruteraan balikan", dalam kata mudah, bermaksud "Saya cuba menulis program yang meniru tingkah laku program lain, tanpa melihat kod asalnya".

Persoalannya sekarang: siapa yang menerapkan perisian ini dan bilakah ia berlaku?


#### Pelencongan mengenai hak cipta

*Seluruh bahan berhak cipta (gambar, bunyi, model 3D, logo, dll ...) terletak di dalam aplikasi pelanggan.
Aplikasi pelayan hanya mengandungi nombor dan teks. Oleh itu, adalah sah sekiranya anda menggunakannya untuk tujuan pendidikan.*

## Aplikasi pelayan WoW tidak rasmi

Siapakah yang membuat aplikasi perisian yang menjalankan pelayan peribadi WoW (biasanya disebut "emulator")? Dan bagaimana mereka melakukannya?



### Kerumitan

![Complex](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/complex.jpg)

Anda tidak perlu menjadi pakar untuk memahami bahawa menulis aplikasi pelayan untuk MMORPG dengan ruang lingkup besar seperti World of Warcraft bukanlah sebuah permainan kanak-kanak.

Blizzard adalah sebuah syarikat yang besar dengan ribuan pekerja. Menulis program yang "menyamaai" operasi aplikasi pelayan mereka bukan sesuatu yang remeh atau layak untuk satu individu (atau sekumpulan kecil pengaturcara).

Dan ia bukan hanya masalah kerumitan. Mari fikirkan tugas-tugas yang sangat remeh tetapi berulang-ulang, seperti menambahkan setiap NPC ke dunia, termasuk setiap item barang rampasan mereka dengan peratusan peluangnya sendiri, dll. Pekerjaan yang hebat pada dasarnya. Belum lagi semua tugas yang sangat rumit yang memerlukan berjam-jam belajar dan ujian, seperti mekanik sihir, mekanik bos, dll.

Pendek kata .... bahkan pengaturcara terbaik di dunia pun tidak dapat melakukan semua kerja ini sendiri.

Namun ada pelayan peribadi, dan perisian yang dapat menjalankannya. Dan beberapa pelayan peribadi kini dapat menawarkan kualiti permainan yang tidak jauh dari yang asli (di sini saya merujuk terutamanya kepada pengembangan lama).

Bagaimana kemungkinan ini terjadi?

### MaNGOS dan model pembangunan sumber terbuka

> Sekiranya anda mempunyai sebiji epal dan saya mempunyai sebiji epal dan kami menukar epal ini, maka anda dan saya masing-masing masih mempunyai satu epal. Tetapi jika anda mempunyai idea dan saya mempunyai idea dan kami bertukar idea ini, maka masing-masing akan mempunyai dua idea. (George Bernard Shaw)

Untuk menjadikannya mudah: program sumber terbuka adalah program yang kodnya adalah umum.

Dalam konteks pelayan peribadi, sumber terbuka memainkan peranan asas.

Beberapa pemain veteran mungkin ingat lagi ketika kualiti permainan di pelayan peribadi benar-benar buruk. Hampir tidak ada yang berjaya.
Sebagai contoh, jika anda seorang penyamun yang tersembunyi anda boleh menjadi sasaran oleh sesiapa sahaja yang menulis `/target Yourname`. Cuba teka kelas mana yang saya pilih untuk watak pertama saya ...

![Mangos-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/mangos-logo.gif)

Revolusi sebenarnya adalah [MaNGOS](https://it.wikipedia.org/wiki/MaNGOS), sebuah projek sumber terbuka yang dibuat pada tahun 2005, yang bertujuan untuk menyediakan aplikasi pelayan untuk World of Warcraft.
Berita baik dari MaNGOS, serta kekuatannya, adalah kenyataan bahawa sebagai sebuah aplikasi sumber terbuka, kodnya benar-benar umum, dan mana-mana pengguna dari seluruh dunia dapat mempelajarinya dan menawarkan sumbangan mereka sendiri (baik dari segi penambahan atau memperbaiki mekanik permainan, tetapi juga dari segi melaporkan bug).

Hanya dengan cara ini, berkat sumbangan banyak sukarelawan dari pelbagai bangsa, berjaya untuk mengembangkan aplikasi pelayan yang mampu meniru World of Warcraft dengan kualiti permainan yang lebih tinggi.

Pada tahun 2009, satu lagi projek penting dilahirkan [TrinityCore](https://www.trinitycore.org/), berdasarkan MaNGOS.

![Trinitycore-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/trinitycore-logo.png)

Sehingga kini, sebilangan besar pelayan peribadi dijalankan pada aplikasi berasaskan MaNGOS/TrinityCore.

Selama bertahun-tahun, [projek yang berbeza](http://mangosrumors.org/best-wow-emulator-2020/) telah dilahirkan, dan adalah berdasarkan kod MaNGOS/TrinityCore, yang berbeza mengikut versi WoW yang disokong.
Contohnya [AzerothCore](https://www.azerothcore.org/) untuk 3.3.5, [OregonCore](https://github.com/OregonCore) untuk 2.4.3, [SkyFire](https://www.projectskyfire.org/) untuk 5.4.3, [CMaNGOS](https://cmangos.net/) untuk Classic/TBC/WOTLK, dan banyak lagi yang lain ... Semuanya berdasarkan MaNGOS dan/atau TrinityCore.

![Azerothcore-authserver](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/azerothcore-authserver.png)

### Ringkasan

Oleh itu, pelayan peribadi mencapai kualiti seperti itu dengan berterima kasih kepada banyak penyumbang yang telah menambahkan lebih banyak ciri permainan selama ini (dari tahun 2005 hingga hari ini).

Hari ini mana-mana pengguna PC yang berpengalaman dapat memasang pelayan WoW dengan mudah, tanpa menjadi seorang pengaturcara.

## Sumber terbuka vs pelayan peribadi

![Alice-and-bob](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/alice-and-bob.jpg)

### Senario hipotesis

Katakan bahawa Alice dan Bob mempunyai pelayan peribadi masing-masing, dan anggap mereka menggunakan versi permainan yang sama.
Kedua-dua Alice dan Bob ingin melepaskan kandungan baru kepada pemain mereka, yang telah ditutup sampai sekarang kerana bos `A`,` B`, `C` dan` D` cukup bermasalah.

- Alice adalah pembangun yang sangat baik dan dapat memperbaiki kedua-dua bos `A` dan` B`
- Bob masih baru dan hanya dapat memperbaiki bos `C`

### Dalam dunia yang ideal

Alice dan Bob bekerjasama dan berkongsi pembetulan mereka. Akibatnya, kedua-dua pelayan mereka akan mempunyai bos `A`,` B` dan `C` yang sempurna.
Selain itu, Alice dan Bob akan berkerjasama untuk mengerjakan `D` juga.

Hasilnya, pemain di kedua-dua pelayan sangat gembira kerana mereka memainkan kandungan yang betul-betul berfungsi.

### Di dunia nyata

Alice dan Bob adalah pesaing dan mereka saling berperang. Di pelayan Alice, hanya bos `A` dan` B` yang berfungsi dan di pelayan Bob hanya `C` berfungsi.
Beberapa pemain beralih dari pelayan Bob ke Alice. Pelayan Bob ditutup selepas beberapa ketika. Sebilangan pemain pelayan Alice berhenti bermain kerana mereka bosan selalu melakukan `A` dan` B` keran `C` dan` D` tidak berfungsi.

Kesannya, pemain di kedua-dua pelayan kurang senang berbanding dengan senario sebelumnya. Alice menjana lebih banyak duit melalui sumbangan pemain daripada Bob.

### Lesen emulator WoW

Sebenarnya, kod MaNGOS/TrinityCore (dan projek terbitannya) dikeluarkan di bawah [lesen GNU GPL](https://en.wikipedia.org/wiki/GNU_General_Public_License).

Dengan kata mudah, lesen ini mengatakan perkara berikut: gunakan kod untuk melakukan apa sahaja yang anda mahukan, tanpa membayar apa-apa, selagi mana-mana pengubahsuaian pada kod asal juga dikeluarkan di bawah lesen yang sama.
Pada dasarnya, lesen projek-projek ini memerlukan mereka yang menggunakannya untuk menerbitkan sebarang perubahan kepada orang ramai.

Sudah tentu, kebanyakan pelayan peribadi menggunakan lesen ini sebagai **kertas tandas**. Jika tidak, tidak seharusnya ada pelayan peribadi yang "lebih baik diperbaiki" daripada yang lain.

![Toilet-paper](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/toilet-paper.jpg)

## Pembohongan mengenai pelayan peribadi

Berikut adalah senarai pembohongan yang sering diberitahu oleh pentadbir pelayan peribadi WoW kepada pemain mereka:


### "Kami menulis teras ini"

Berita palsu. Tidak kira berapa banyak perubahan yang "anda" buat. Namun, anda memulakan dengan projek berasaskan MaNGOS.

Mungkin anda telah membuat beberapa penambahbaikan, tetapi sebahagian besar kodnya masih MaNGOS/TrinityCore.

Mungkin anda benar-benar baik dan anda telah menulis semula sebahagian besar kod selama ini. Namun, anda bermula dari MaNGOS. Tanpa itu, pada hari pertama anda tidak akan mempunyai ciri log masuk yang berfungsi.

### "Kami telah membetulkan X"

Dalam sebilangan besar kes, tidak ada yang betul-betul memperbaiki sesuatu.
Mereka memuat turun sahaja perbaikan yang berasal dari komuniti sumber terbuka dan menerapkannya ke teras mereka.
Kemudiannya mereka mengambil semua kredit.

### "Kami (benar-benar) membetulkan X"

Sesetengah pelayan peribadi betul-betul membetulkannya sendiri. Mereka sering mempunyai pasukan pengembangan yang berdedikasi dengan duit yang berasal dari sumbangan pemain.

Sebilangan besar daripada mereka tidak berkongsi pembaikan ini dengan komuniti pembangunan.

Baiklah, komuniti yang memberikan (secara percuma) perisian yang anda gunakan untuk menjalankan pelayan anda, meminta anda untuk menkongsikannya, tetapi anda tetap perlu merahsiakannya. Jadi saya tetap benci awak.

![Pinocchio](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/pinocchio.jpeg)

## "Justifikasi" pelayan peribadi


### "Saya menyimpannya secara peribadi untuk menjadikan pelayan saya sebagai tempat yang istimewa, lebih baik daripada yang lain"

Baiklah juara. Cuba fikirkan perkara ini: sekiranya SEMUA pemaju berbuat seperti anda, anda dan pelayan peribadi anda tidak akan wujud.

Kenapa? Kerana MaNGOS (atau TrinityCore, AzerothCore, dll ...) tidak akan wujud.
Projek ini wujud terima kasih kepada pembangun yang, tidak seperti anda, berkongsi kod mereka.

Sekiranya semua pembangun menyimpan kod mereka secara peribadi, kami tidak akan mempunyai emulator WoW yang bagus dan anda tidak dapat membuka pelayan peribadi anda, kerana tidak ada perisian yang tersedia.


### "Sekiranya saya berkongsi pembaikan saya, pesaing akan mencurinya"

Tidak ada apa yang "dicuri". Mereka tidak dapat "mencuri" kod itu kerana itu bukan "milik" anda. Tidak, walaupun anda betul-betul menulisnya.

Falsafah sumber terbuka jelas: anda boleh menggunakan kod tersebut secara percuma, dengan syarat sebarang pengubahsuaiannya WAJIB dibuat untuk umum.

Oh anda tidak setuju? Baiklah. Oleh itu, jangan gunakan kod sumber terbuka dan tulis emulator WoW anda sendiri dari awal.

## Bagaimana ini mempengaruhi pemain

![Wow-Dranei-crying](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-dranei-crying.jpg)

Saya benar-benar memahami bahawa keseluruhan cerita mengenai etika dan lesen ini tidak penting bagi rata-rata pemain World of Warcraft.
Pemain hanya mahu bermain di pelayan yang stabil dan tetap, mereka tidak begitu peduli sama ada pelayan ini bekerjasama dengan sumber terbuka atau tidak.

Tetapi ... cubalah sebentar untuk melihatnya dari perspektif lain.

Pembangun projek sumber terbuka (MaNGOS, TrinityCore, AzerothCore, dll ...) pada dasarnya tidak begitu peduli dengan apa yang dilakukan oleh pelayan peribadi.
Sudah tentu, sebagai pembangun, anda kesal melihat beberapa pentadbir pelayan rawak mengambil kredit untuk kerja anda, tetapi pada akhirnya ia tidak mengubah hidup anda.
Banyak pembangun sumber terbuka melakukannya untuk tujuan keseronokan dan pendidikan.

Sebenarnya, jika SEMUA pelayan peribadi berkolaborasi dengan sumber terbuka, kehidupan pemain akan berubah sama sekali!
Anda tahu, dalam hal ini, setiap pelayan akan memberikan pengalaman permainan yang jauh lebih baik untuk pengembangan apa pun. Contoh Alice dan Bob yang disebutkan sebelumnya dapat diterapkan dalam kes ini juga.

Walau bagaimanapun, kenyataannya adalah: terdapat banyak pelayan peribadi di seluruh dunia, masing-masing selalu mengerjakan perkara yang sama, berlumba untuk melakukannya dengan lebih cepat dan lebih baik.
Sekiranya mereka berkolaborasi antara satu sama lain, mereka akan menghindari melakukan kerja yang tidak perlu dan akan mempunyai lebih banyak masa dan tenaga kerja. Oleh itu mereka pasti dapat mencapai lebih banyak lagi.

*Catatan: kualiti (dan persaingan antara) pelayan peribadi tidak seharusnya (hanya) mengenai pembaikan, tetapi juga mengenai faktor lain seperti kemahiran pentadbir dalam menguruskannya. Kualiti komuniti juga memainkan peranan penting, sama seperti yang berlaku di pelayan Blizzard (yang semuanya sama dari perspektif teknikal).*

Sekiranya pelayan persendirian ditutup, dan pembangunnya tidak berkongsi karya mereka, kerja itu akan hilang selamanya.

## Mendedahkan pembohongan

### Senarai pengarang rasmi

Perkara yang paling menarik adalah bahawa semua projek berasaskan MaNGOS adalah terbuka untuk umum, jadi ada kemungkinan untuk mengesahkan secara tepat siapa yang menyumbang kepada mereka.

Akibatnya, semua senarai penyumbang projek-projek ini terbuka dan SESIAPA sahaja dapat mengesahkan siapa yang betul-betul memperbaiki apa.

Sebagai contoh:

- Senarai rasmi penyumbang MaNGOS: https://github.com/cmangos/mangos-wotlk/blob/master/AUTHORS.md
- Senarai rasmi penyumbang TrinityCore https://github.com/TrinityCore/TrinityCore/blob/3.3.5/AUTHORS
- Senarai rasmi penyumbang AzerothCore https://github.com/AzerothCore/azerothcore-wotlk/graphs/contributors

PS: anda boleh menemui pengarang artikel ini dalam semua senarai ini

### Senarai rasmi commit

Sebarang projek sumber terbuka (umumnya dihoskan di GitHub) mempunyai senarai commit yang dilaksanakan oleh pemaju yang berbeza. Untuk setiap commit, pengarang dan tarikhnya ada.

Ia sangat mudah untuk mengesahkan maklumat ini, hanya buka repositori rasmi mana-mana emulator. Google misalnya "TrinityCore github" atau "AzerothCore github" dan hanya melihat.

Anda akan melihat siapa-yang-benar-benar-buat-apa. Anda akan melihat semua baris kod, pengarangnya, komen pembangun lain, dll. Anda akan melihat semuanya. Tiada penipuan lagi!


## Apa yang boleh saya lakukan sebagai pemain?

Nasihat saya adalah anda bermain/menyokong pelayan peribadi yang bekerjasama dengan sumber terbuka, walaupun jenis pengembangan dan emulator yang mereka gunakan.

Atau, sekurang-kurangnya, elakkan pelayan yang menjajakan karya orang lain sendiri, membuang kredit dari pengarang asalnya.


### Ketahui lebih lanjut mengenai perisian percuma

- https://www.gnu.org/software/software.en.html
- https://www.fsf.org/about/what-is-free-software


## Terima kasih

Terima kasih khas kepada *Laura Bartiromo*
