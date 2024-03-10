# <h1 align="center">Laporan Praktikum Modul 1 Tipe Data</h1>
<p align="center">2311110021 / Fauzan  Arrizal / Sains Data</p>

## Dasar Teori

Tipe data adalah klasifikasi data berdasarkan jenisnya yang penting untuk memungkinkan kompiler memahami cara data tersebut akan digunakan. Jenis tipe data yang umum dipelajari meliputi tipe data primitif, abstrak, dan koleksi..

## Guided 

### 1. [Tipe Data Primitif]

C++
#include <iostream>
using namespace std;
// Main program
main()
{
    char op;
    float num1, num2;
    // It allows user enter operatoe i.e, +, -, *, /
    cin >> op;
    // It alllow user to enter the operands
    cin >> num1 >> num2;
    // switch statement begins
    switch  (op)
    
    {
    //  If user enter +
    case '+':
        cout << num1 + num2;
        break;
    // If user enter -
    case '-':
        cout << num1 - num2;
        break;
    // If user enter *
    case '*':
        cout << num1 * num2;
        break;
    // If user enter /
    case '/':
        cout << num1 / num2;
        break;
    // If the operator is other than ....
    // error message will display
    default:
        cout << "Error! operator is not correct";
    }
    return 0;
}

Kode di atas digunakan untuk mencetak teks "ini adalah file code guided praktikan" ke layar menggunakan function cout untuk mengeksekusi nya.


### 2. [Tipe Data Abstrak]

C++
#include <stdio.h>

// struct
struct Mahasiswa
{
    const char *name;
    const char *address;
    int age;
};

int main()
{
    // Using struct
    struct Mahasiswa mhs1, mhs2;
    
    // Adding values to struct
    mhs1.name = "Dian";
    mhs1.address = "Mataram";
    mhs1.age = 22;
    mhs2.name = "Bambang";
    mhs2.address = "Surabaya";
    mhs2.age = 23;

    // Printing struct contents
    printf("## Mahasiswa 1 ##\n");
    printf("Nama: %s\n", mhs1.name);
    printf("Alamat: %s\n", mhs1.address);
    printf("Umur: %d\n", mhs1.age);
    printf("## Mahasiswa 2 ##\n");
    printf("Nama:  %s\n", mhs2.name);
    printf("Alamat: %s\n", mhs2.address);
    printf("Umur: %d\n", mhs2.age);
    return 0;
}

Struct "Mahasiswa" digunakan untuk menampung data seperti nama, alamat, dan usia mahasiswa. Dalam kode tersebut, dua variabel struct "mhs1" dan "mhs2" digunakan untuk merepresentasikan informasi individu dari mahasiswa. Setelah nilai-nilai diatur untuk setiap variabel struct, informasi tersebut kemudian dicetak menggunakan printf untuk menampilkan data dari setiap mahasiswa.


### 3. [Tipe Data Koleksi]

C++
#include <iostream>
using namespace std;
int main()
{
    //Deklarasi dan inisialisasi array
    int nilai[5];
    nilai[0] = 23;
    nilai[1] = 50;
    nilai[2] = 34;
    nilai[3] = 78;
    nilai[4] = 90;

    //mencetak array
    cout << "isi array pertama :" << nilai[0] << endl;
    cout << "isi array kedua :" << nilai[1] << endl;
    cout << "isi array ketiga :" << nilai[2] << endl;
    cout << "isi array keempat :" << nilai[3] << endl;
    cout << "isi array kelima :" << nilai[4] << endl;
    return 0;
}

Kode di atas digunakan untuk mencetak teks "ini adalah file code guided praktikan" ke layar menggunakan function cout untuk mengeksekusi nya.

## Unguided 

### 1. [Buatlah program menggunakan tipe data primitif minimal dua fungsi dan bebas.
Menampilkan program, jelaskan program tersebut dan ambil kesimpulan dari
materi tipe data primitif!]


C++
#include <iostream>
using namespace std;

int hitungLuasPersegiPanjang(int panjang, int lebar) {
    return panjang * lebar;
}

float hitungLuasSegitiga(float alas, float tinggi) {
    return 0.5 * alas * tinggi;
}

int main() {
    int panjang, lebar;
    float alas, tinggi;

    // Persegi panjang
    cout << "Masukkan panjang persegi panjang: ";
    cin >> panjang;

    cout << "Masukkan lebar persegi panjang: ";
    cin >> lebar;

    cout << "Luas persegi panjang dengan panjang " << panjang << " dan lebar " << lebar << " adalah: " << hitungLuasPersegiPanjang(panjang, lebar) << endl;

    // Segitiga
    cout << "Masukkan alas segitiga: ";
    cin >> alas;

    cout << "Masukkan tinggi segitiga: ";
    cin >> tinggi;

    cout << "Luas segitiga dengan alas " << alas << " dan tinggi " << tinggi << " adalah: " << hitungLuasSegitiga(alas, tinggi) << endl;

    return 0;
}

#### Output:
![Screenshot (334)](https://private-user-images.githubusercontent.com/161549586/311273233-626e955f-fb5f-46a3-b183-17a5bd573440.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDk5MTMxNDQsIm5iZiI6MTcwOTkxMjg0NCwicGF0aCI6Ii8xNjE1NDk1ODYvMzExMjczMjMzLTYyNmU5NTVmLWZiNWYtNDZhMy1iMTgzLTE3YTViZDU3MzQ0MC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwMzA4JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDMwOFQxNTQ3MjRaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT00ZDExY2Y1YmEyOTFlYjllMDkwZmY4NTBlYWIxMDJjMWNiMjliZjQ1YmQxYTQxM2JmMGY3ODZiYjdhYzg2NzE1JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.uKpTg8njZVXew5uKkk0kp8jwBOF-vbAq6TS1cRVVcVw)



Penjelasan program:
Program ini meminta pengguna untuk memasukkan nilai panjang dan lebar persegi panjang menggunakan fungsi input cin, yang kemudian disimpan dalam variabel panjang dan lebar. Selanjutnya, program menghitung luas persegi panjang dengan memanggil fungsi hitungLuasPersegiPanjang menggunakan nilai panjang dan lebar yang dimasukkan pengguna, dan hasilnya ditampilkan. Setelah itu, program meminta pengguna untuk memasukkan nilai alas dan tinggi segitiga, kemudian menghitung luas segitiga berdasarkan input tersebut menggunakan fungsi hitungLuasSegitiga, dan menampilkan hasil perhitungannya. Kesimpulannya, program ini memungkinkan pengguna untuk menghitung luas persegi panjang dan segitiga berdasarkan input yang mereka berikan.

### 2. [Jelaskan fungsi dari class dan struct secara detail dan berikan contoh programnya]

-Class:
Class adalah struktur yang digunakan untuk merepresentasikan objek dalam pemrograman berorientasi objek. Class mengelompokkan data bersama dengan metode yang beroperasi pada data tersebut.

Contoh code:

C++
#include <iostream>
using namespace std;

class Person {
public:
    string name;
    int age;
};

int main() {
    // Membuat objek dari class Person
    Person person1;
    person.name = "Ojan";
    person.age = 19;

    // Menampilkan informasi person1
    cout << "Name: " << person.name << ", Age: " << person.age << endl;

    return 0;
}


#### Output:

Penjelasan:
class Person: Mendefinisikan class Person dengan dua atribut, yaitu name bertipe string dan age bertipe integer.
Person person;: Membuat objek person dari class Person.
person.name = "Ojan"; dan person.age = 19;: Menginisialisasi nilai atribut name dan age dalam objek person.
cout: Menampilkan informasi yang terdapat pada objek person.

-Struct:
Struct (singkatan dari "structure") adalah sebuah tipe data yang digunakan untuk mengelompokkan beberapa variabel dengan tipe data yang berbeda dalam satu unit.

Contoh code:

C++
#include <iostream>
using namespace std;

struct Point {
    int x;
    int y;
};

int main() {
    // Membuat objek 
    Point p1;
    p1.x = 10;
    p1.y = 30;

    // Koordinat p1
    cout << "Point coordinates: (" << p1.x << ", " << p1.y << ")" << endl;

    return 0;
}

Penjelasan:
struct Point: Mendefinisikan struct Point dengan dua variabel bertipe integer, yaitu x dan y.
Point p1;: Membuat objek p1 dari struct Point.
p1.x = 10; dan p1.y = 30;: Menginisialisasi nilai dari variabel x dan y dalam objek p1.
cout: Menampilkan koordinat yang terdapat pada objek p1.

### 3. [Buat dan jelaskan program menggunakan fungsi map dan jelaskan perbedaan dari
array dengan map.
]

C++
#include <iostream>
using namespace std;

int main() {
    cout << "ini adalah file code unguided praktikan" << endl;
    return 0;
}

#### Output:
![240302_00h00m06s_screenshot](https://github.com/FauzanArrizal/Laprak-Modul-1.git)

Kode di atas digunakan untuk mencetak teks "ini adalah file code guided praktikan" ke layar menggunakan function cout untuk mengeksekusi nya.

## Kesimpulan
Ringkasan dan interpretasi pandangan kalia dari hasil praktikum dan pembelajaran yang didapat[1].

## Referensi
[1] I. Holm, Narrator, and J. Fullerton-Smith, Producer, How to Build a Human [DVD]. London: BBC; 2002.