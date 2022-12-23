# Ujian Akhir Semester 
<br>Mata Kuliah 	: Dasar Pemrograman
<br> Nama		: CITRA AULIA
<br>NIM		:	1227050030
<br>Jurusan		:[Teknik Informatika](http://if.uinsgd.ac.id/) [UIN Sunan Gunung Djati Bandung](https://uinsgd.ac.id/) 

## Deskripsi Umum
<br> Kali ini Kita akan membuat program menampilkan matriks beserta bilangan deret aritmatika yang tidak habis dibagi 3, 5, dan 7 dengan menggunakan bahasa c++. Untuk membuat program ini, Kita dapat menggunakan array, pengulangan for, dan if else.

<br> Pada langkah awal, program meminta 2 inputan berupa jumlah baris dan kolom untuk membuat matriks pada array, kemudian program akan meminta untuk memasukkan satu per satu angka untuk baris dan kolom pada array sesuai dengan jumlah baris dan kolom tadi.

<br> Selanjutnya program akan menampilkan hasil inputan tadi berupa matriks, lalu program juga menampilkan angka-angka yang tidak habis dibagi 3,5, dan 7 sesuai dengan inputan untuk matriks.

## Source Code
```cpp
#include <iostream>
#include <iomanip>
using namespace std;
 
int main()
{
	int matriks[100][100];
	int baris, kolom, i, j;
  
	cout << "Program Menampilkan Matriks dan Deret Aritmatika yang Habis Dibagi 3, 5, dan 7\n" << endl;
	
	cout << "Masukkan jumlah baris : "; cin >> baris;
	cout << "Masukkan jumlah kolom : " ; cin >> kolom ;
	cout << endl;
	
	for (i=0;i<=baris-1;i++) {
		for(j=0;j<=kolom-1;j++) {
			cout << "Baris " <<i+1<<", kolom "<<j+1<< " = ";
			cin >> matriks[i][j];
		}
	}
	
	cout << endl;
	cout << "Nilai Input: \n";
	for(int i = 0; i < baris; i++){
		for(int j = 0; j < kolom; j++){
			cout<< matriks[i][j]<<"\t";
		}
		cout<<endl;
	}
	
	int angka[20];
	int index = 0;
	for(i=0; i<baris; i++){
		for(j=0; j<kolom; j++) {
			if (matriks[i][j]%3 != 0 && matriks[i][j]%5 != 0 && matriks[i][j]%7 != 0){
				angka[index] = matriks[i][j];
				index++;
			}
		}
	}
	
	cout << endl;
	cout << "Bilangan yang tidak habis dibagi 3, 5, 7 sebagai berikut: ";
	for(int i = 0; i < index; i++){
		cout << angka[i] <<", ";

	}


  return 0;
}
```

## Output
![img 2](https://user-images.githubusercontent.com/121267209/209329789-aba86de2-51e2-462a-8947-d62fdb5ee6c1.png)
