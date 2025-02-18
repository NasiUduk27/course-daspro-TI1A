## JOBSHEET 7

## PERULANGAN 1

### Tujuan

Mahasiswa mampu menyelesaikan permasalahan/studi kasus menggunakan sintaks perulangan 1 dan mengimplemantasikannya dalam bahasa pemrogaman java.

### Alat dan Bahan
+ PC/laptop
+ Browser(chrome, firefox, safari)
+ Koneksi internet

### Praktikum

#### Percobaan 1 : Penggunaan for, while dan do-while

#### Waktu percobaan : 40 menit

1. Perhatikan flowchart perulangan for dibawah ini!

    <p align="left">
    <img width="197" height="259" src="images/flowchartFaktorial.png">
    </p>
    

> Flowchart diatas digunakan untuk menghitung nilai faktorial, selanjutnya kita akan membuat programnya berdasarkan
> flowchart di atas!

2. Tambahkan library Scanner, deklarasi Scanner, dan buat variabel angka untuk menampung data yang diinput melalui keyboard




```Java
// Ketik kode program di bawah sini
        import java.util.Scanner;
        Scanner sc = new Scanner(System.in);   
       
```


```Java
3. Buatlah deklarasi dan inisialisasi variabel faktorial sesuai dengan flowchart diatas
```


```Java
// Ketik kode program di bawah sini
int angka,faktorial = 1; 
        
```

4. Tambahkan struktur perulangan untuk menghitung hasil faktorial sebuah nilai yang diinputkan menggunakan for
    
    <p align="left">
    <img width="696" height="124" src="images/for.jpg" align="left">
    </p>


```Java
// Ketik kode program di atas di bawah sini
System.out.println("=====PROGRAM MENGHITUNG NILAI FAKTORIAL DENGAN FOR=====");
System.out.println("Masukkan Bilangan: ");
angka = input.nextInt();
for (int  i=1;i<=angka;i++)
    faktorial*=i;
System.out.print("Nilai faktorial bilangan tersebut adalah : "+faktorial);

```
```
=====PROGRAM MENGHITUNG NILAI FAKTORIAL DENGAN FOR=====
Masukkan Bilangan: 
3
Nilai faktorial bilangan tersebut adalah : 6
```
```
Dengan menggunakan pengulangan for kita dapat mengecek sebuah nilai terlebih dahulu sebelum dijalankan apabila nilainya memenuhi maka program akan dijalankan dan terus berulang sampai program menemukan salah
```

5. Ubah nilai variabel faktorial seperti semula. Kemudian gunakan struktur perulangan while untuk menghitung hasil faktorial sebuah nilai yang diinputkan
    
    <p align="left">
    <img width="696" height="124" src="images/while.jpg" align="left">
    </p>


```Java
// Ketik kode program di atas di bawah sini
faktorial=1;
System.out.println("=====PROGRAM MENGHITUNG NILAI FAKTORIAL DENGAN WHILE=====");
System.out.print("Masukkan Bilangan: ");
angka=input.nextInt();
int i=1;
while(i<=angka){
    faktorial*=i;
    i++;
}
System.out.println("Nilai faktorial bilangan tersebut adalah: "+faktorial);

```
```
=====PROGRAM MENGHITUNG NILAI FAKTORIAL DENGAN WHILE=====
Masukkan Bilangan: 4
Nilai faktorial bilangan tersebut adalah: 24
```
```
Hampir sama dengan pengulangan dengan for, pengulangan dengan while inisiasi dilakukan sebelumnya dan expresi increment atau decrementnya dilakukan setelah program dijalankan. Program akan terus dijalankan selama memenuhi syarat.
```

6. Kembalikan lagi nilai variabel faktorial seperti semula. Gunakan struktur perulangan do-while untuk menghitung hasil faktorial sebuah nilai yang diinputkan
    
    <p align="left">
    <img width="696" height="124" src="images/dowhile.jpg" align="left">
    </p>
```Java
// Ketik kode program di atas di bawah sini
faktorial=1;
System.out.println("=====PROGRAM MENGHITUNG NILAI FAKTORIAL DENGAN DO-WHILE=====");
System.out.print("Masukkan Bilangan: ");
angka=input.nextInt();
int i = 1;
do{
    faktorial*=i;
    i++;
}
while(i<=angka);
System.out.println("Nilai faktorial bilangan tersebut adalah :"+ faktorial);


```
```
=====PROGRAM MENGHITUNG NILAI FAKTORIAL DENGAN DO-WHILE=====
Masukkan Bilangan: 5
Nilai faktorial bilangan tersebut adalah :120
```
```
Untuk pengulangan dengan do-while pernyataannya akan terus dijalankan dan berulang selama memenuhi syarat, pada pengulangan ini program akan dijalankan terlebih dahulu sebelum pengecekan sehingga jika nilainya false pada saat di cek setidaknya ada minimal 1 yang dijalankan.
```


##### Pertanyaan
1. Pada program diatas, apakah kegunaan baris berikut?
<p align="left">
    <img src="images/hitungFaktorial.jpg" align="left">
    </p>


```
// Ketik jawaban disini
kegunaan baris tersebut adalah untuk membuat rumus dari faktorial yaitu mengalikan dengan bilangan sebelumnya, i berasal dari bilangan yang sebelumnya telah dikeluarkan

```

2. Modifikasi program diatas dibagian struktur pemilihannya sehingga hasilnya menjadi seperti di bawah ini:
<p align="left">
    <img src="images/modifP1.jpg" align="left">
    </p>


```Java
// Ketik kode program di atas di bawah sini
import java.util.Scanner;
Scanner input = new Scanner(System.in);  
int angka,faktorial = 1;

        System.out.println("=====PROGRAM MENGHITUNG NILAI FAKTORIAL=====");
        System.out.print("Masukkan Bilangan : ");
        
        angka = input.nextInt();
        System.out.print(angka + "Faktorial = ");
        for(int i = 1; i <= angka; i++) {
            System.out.print(i);
            
            if(i<angka){
                System.out.print("x");
            }
            
            faktorial *= i;
        }
        
        System.out.print(" = " + faktorial);

```
```
=====PROGRAM MENGHITUNG NILAI FAKTORIAL=====
Masukkan Bilangan : 5
5Faktorial = 1x2x3x4x5 = 120
```
```
Dengan menambahkan pemilihan if maka angka yang kurang dari angka yang diinputkan jika benar akan ditambahkan string x, kemudian jika dijalankan akan menghasilkan keluaran seperti yang di atas
```

#### Percobaan 2 : Keluar dari perulangan menggunakan break

#### Waktu percobaan : 40 menit

1. Buatlah perulangan dengan menggunakan for yang memanfaatkan keyword break
<p align="left">
    <img width="696" height="124" src="images/for2.jpg" align="left">
    </p>


```Java
// Ketik kode program di atas di bawah sini
 import java.util.Scanner;
 Scanner input = new Scanner(System.in);   
       
        int angka,total;
        System.out.println("===PROGRAM FOR LOOP DENGAN BREAK===");
        for(total=0;true;){
            System.out.print("Masukkan Bilangan : ");
            angka = input.nextInt();
            total+=angka;
            if(total>50)break;
        }
        System.out.println("Jumlah angka-angka yang telah dimasukkan : "+total);

```
```
===PROGRAM FOR LOOP DENGAN BREAK===
Masukkan Bilangan : 10
Masukkan Bilangan : 20
Masukkan Bilangan : 50
Jumlah angka-angka yang telah dimasukkan : 80
```
```
Dengan menggunakan statement break kita dapat keluar dari pengulangan yang terjadi, jadi jika masukan salah akan menuju ke break untuk dikeluarkan dari pengulangan tersebut.
```

2. Buat perulangan yang sama dengan struktur perulangan while
<p align="left">
    <img width="696" height="124" src="images/while2.jpg" align="left">
    </p>


```Java
// Ketik kode program di atas di bawah sini
import java.util.Scanner;
Scanner input = new Scanner(System.in);   
       
        int angka,total;
        System.out.println("===PROGRAM WHILE LOOP DENGAN BREAK===");
        total=0;
        while(true){
            System.out.print("Masukkan Bilangan : ");
            angka = input.nextInt();
            total+=angka;
            if(total>50)break;
        }
        System.out.println("Jumlah angka-angka yang telah dimasukkan : "+total);

```
```
===PROGRAM WHILE LOOP DENGAN BREAK===
Masukkan Bilangan : 10
Masukkan Bilangan : 35
Masukkan Bilangan : 78
Jumlah angka-angka yang telah dimasukkan : 123
```

3. Tuliskan perulangan diatas dalam struktur do-while
    <p align="left">
    <img width="696" height="124" src="images/dowhile2.jpg" align="left">
    </p>


```Java
// Ketik kode program di atas di bawah sini
import java.util.Scanner;
Scanner input = new Scanner(System.in);   
       
        int angka,total;
        System.out.println("===PROGRAM DO-WHILE LOOP DENGAN BREAK===");
        total=0;
        do
        {
            System.out.print("Masukkan Bilangan : ");
            angka = input.nextInt();
            total+=angka;
            if(total>50)break;
        }
        while(true);
        System.out.println("Jumlah angka-angka yang telah dimasukkan : "+total);

```
```
===PROGRAM DO-WHILE LOOP DENGAN BREAK===
Masukkan Bilangan : 25
Masukkan Bilangan : 24
Masukkan Bilangan : 41
Jumlah angka-angka yang telah dimasukkan : 90
```

##### Pertanyaan
1. Jelaskan fungsi kode program yang telah dibuat pada percobaan diatas!


```
// Ketik jawaban disini
fungsi dari semua statement break yang berada pada setiap pengulangan tersebut adalah untuk keluar dari loop yang terjadi jika statement yang dijalankan. 

```

2. Jelaskan fungsi kode berikut!
    <p align="left">
    <img src="images/forPertanyaan2.jpg" align="left">
    </p>



```
// Ketik jawaban disini
fungsi dari total = 0 adalah sebuah iniasi yang akan dijalankan nantinya oleh program dan jika true maka kode program akan dijalankan
```


#### Percobaan 3 : Keluar dari step perulangan menggunakan continue

#### Waktu percobaan : 40 menit

1. Buat program looping menggunakan struktur perulangan for seperti di bawah ini: 
<p align="left">
    <img src="images/forContinue.jpg" align="left">
    </p>



```Java
// Ketik kode program di atas di bawah sini
Scanner input = new Scanner(System.in);
int angka, total, count;
        double avg;
        total = 0;
        count = 0;
               System.out.println("===PROGRAM FOR LOOP DENGAN CONTONUE===");
           
           for (int i = 0; i<5; i++){    
               System.out.print("Masukkan Bilangan: ");
               angka = input.nextInt();
               
               if (angka>=50) continue;
               total += angka;
               count++;
               
               
           }
               System.out.println("Jumlah angka-angka kurang dari 50: " +total);
               avg=(double)total/count;
               System.out.println("Rata-rata angka yang kurang dari 50: " + avg);

```


```
5. Jalankan program. Amati apa yang terjadi!
===PROGRAM FOR LOOP DENGAN CONTONUE===
Masukkan Bilangan: 40
Masukkan Bilangan: 20
Masukkan Bilangan: 20
Masukkan Bilangan: 10
Masukkan Bilangan: 10
Jumlah angka-angka kurang dari 50: 100
Rata-rata angka yang kurang dari 50: 20.0
```

##### Pertanyaan
1. Jelaskan Perbedaan dari percobaan 2 dan percobaan 3


```
// Ketik jawaban disini
Perbedaannya terletak pada statement break dan continue, pada saat statement break dijalankan maka dipergunakan untuk keluar dari loop tersebut sedangkan pada statement continue nilai yang berada pada kondisi tersebut tidak akan dijalankan atau dilewati ke kondisi berikutnya
```


2. Jelaskan apa fungsi perintah kode program dibawah ini?
<p align="left">
    <img width="352" height="79" src="images/continuePertanyaan.jpg" align="left">
    </p>


```
// Ketik jawaban disini
if berarti kondisi pemilihan dan mempunyai kondisi jika angka tersebut nilainya kurang dari sama dengan 50 maka dilewati kemudian masuk ke dalam rumus dan yang terakhir setelah semuanya dijalankan maka akan di increment yaitu menaikkan nilainya agar tidak menjadi infinity loop

```

### Tugas

#### Waktu pengerjaan Tugas: 140 menit

1. Buatlah program yang meminta masukan user sebuah bilangan bulat N (N > 0). Program kemudian menampilkan penjumlahan N bilangan genap positif pertama (bilangan genap ≥ 0).
Contoh: 
    •	Jika user memasukkan N = 10, program akan menghitung banyaknya jumlah bilangan positive di dalam range bilangan 1-10   kemudian menampilkan penjumlahan bilangan positive bilangan bilangan diantara 1-10 yaitu : 
        0 + 2 + 4 + 6 + 10 = 30. 
        Setelah itu program akan menampilkan rata-rata dari bilangan positive yang telah dijumlahkan tadi.
    •	Contoh output program dan flowchart
<br/><img width="303" height="529" src="images/hasilTugasFc.jpg" align="left"><br/>
  

<br/><img width="303" height="529" src="images/fcTugasJS7.png" align="left">



```Java
// Ketik kode program disini
import java.util.Scanner;
Scanner input = new Scanner(System.in);
        
        int bil, jmlBilGenap;
        int totalGenap=0;
        double avg = 0;
        
        System.out.print("Masukkan angka : ");
        bil = input.nextInt();
        jmlBilGenap=bil/2;
        System.out.println("Banyaknya bilangan genap dari 1 sampai 10 adalah "+jmlBilGenap);
        
        System.out.print("Angka Genap dalam range tersebut adalah "); 
       for(int i=1;i<=bil;i++){
          
           if(i%2!=0){
                  continue;
              
              
          }else{
               
             System.out.printf("%d,", i);   
              
           }
           totalGenap += i;
           avg = totalGenap / jmlBilGenap;
           
       }
        
       System.out.printf("%n");
       System.out.println("Hasil pemjumlahan bilangan genap dari 1 sampai 10 adalah " + totalGenap);
       System.out.println("Rata-rata bilangan genap dari 1 sampai 10 adalah " + avg);
}

```
```
Masukkan angka : 10
Banyaknya bilangan genap dari 1 sampai 10 adalah 5
Angka Genap dalam range tersebut adalah 2,4,6,8,10,
Hasil pemjumlahan bilangan genap dari 1 sampai 10 adalah 30
Rata-rata bilangan genap dari 1 sampai 10 adalah 6.0
```
```
1. memanggil library scanner agar user dapat menginputkan nilai dari keyboard mereka
2. mendeklarasi tipe data integer dan double precision
3. menginputkan sebuah nilai kemudian akan masuk dalam rumus dan ditampilkan
4. masuk ke dalam pengulangan yang mengulang sebuah nilai yang dinputkan dan dicek sesuai pernyataan yang kita masukkan dalam
5. setelah tampil bilangan genap yang kita input di awal akan langsung ke else karena yang di rumus menggunakan statement continue yang artinya mengebaikan nilai yang asli
6. setelah diseleksi maka akan masuk ke rumus total dari semua bilangan yang ada di range tersebut dan kemudian di tampilkan
```

2. Buatlah program untuk menampilkan angka 1 hingga angka masukan pengguna secara berurutan dan melompati angka kelipatan 5. Seperti tampilan di bawah ini
<p align="left">
<img width="184" height="328" src="images/tugas1.jpg" align="left">
</p>


```Java
// Ketik kode program disini
import java.util.Scanner;
Scanner input = new Scanner(System.in);
       
        int angka;
        System.out.print("Masukkan angka: ");
        angka = input.nextInt();

        for(int i = 0; i <=angka; i++) {
            if(i%5==0)
            continue;
            System.out.println(i);
        }
```
```
Masukkan angka: 19
1 
2 
3 
4 
6 
7 
8 
9 
11
12
13
14
16
17
18
19
```
```
1. memanggil library scanner agar user dapat menginputkan nilai dari keyboard mereka
2. mendeklarasikan tipe data integer
3. menginputkan sebuah nilai dan masuk ke dalam pengulangan dan akan di cek
4. jika pernyataan tersebut benar akan masuk kepada pemeilihan jika nilai tersebut dibagi 5 dan bersisa 0 maka akan di abaikan dengan statement continue
```

3. Buatlah sebuah program yang menampilkan deret bilangan fibonacci sebagai berikut. Dimana bilangan yang terletak di sebelah kanan adalah hasil penjumlahan dari 2 bilangan sebelumnya
 <p align="left">
    <img width="451" height="226" src="images/fibo.png" align="left">
    </p>



```Java
// Ketik kode program disini
import java.util.Scanner;
Scanner input = new Scanner(System.in);  
int batas, awal, akhir, hasil;
        
        System.out.print("Masukan banyak bilangan yang ingin ditampilkan: ");
        
        batas = input.nextInt();
        awal = 0;
        akhir = 1;
        hasil = 1;
        for (int i =1; i<=batas; i++){
            
            
            System.out.print("Sum of: ");
            System.out.printf("%s + %s = %s %n", awal, akhir, hasil);
            
            awal = akhir;
            akhir = hasil;
            hasil = awal + akhir;
            
        } 
        
```
```
Masukan banyak bilangan yang ingin ditampilkan: 10
Sum of: 0 + 1 = 1 
Sum of: 1 + 1 = 2 
Sum of: 1 + 2 = 3 
Sum of: 2 + 3 = 5 
Sum of: 3 + 5 = 8 
Sum of: 5 + 8 = 13 
Sum of: 8 + 13 = 21 
Sum of: 13 + 21 = 34 
Sum of: 21 + 34 = 55 
Sum of: 34 + 55 = 89
```
```
1. memanggil library scanner agar user dapat menginputkan nilai dari keyboard mereka
2. kemudian mendeklarasikan tipe data dan memasukkan bilangan yang akan ditampilkan
3. dengan nilai awal 0,akhir 1, dan hasil 1
4. kemudian masuk kepada pengulangan yang memiliki pernyataan jika i = 1 dan nilai i kurang dari batas maka akan di increment 1 kali
5. memunculkan semua nilai yang telah di proses kemudian di deklarasi nilai awal sama dengan akhir nya, nilai akhirnya sama dengan hasil, dan hasil adalah berupa nilai awal ditambahkan dengan nilai akhir 
```
