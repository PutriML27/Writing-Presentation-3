# Minggu 3 - JavaScript Intermediate 
## Array
**Array** adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya seperti tipe data String, Number, Boolean dan lainnya.

Contoh Array sebagai berikut:
``` 
    Let contohData = ['data string', 45, false];
    console.log(contohData);
```
**Memanggil Array**, array pada javascript dihitung dari index data ke-0. Jadi data pertama adalah index ke-0.
``` 
    let list = {
        "Belajar";
        "Nyuci";
        "Masak";
    }
    console.log(list[0]);
    // Output: "Belajar
```
**Mengupdate data pada Array**, Bisa menggunakan let dan const. Const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update konten nilai di dalam array (mutable).
Yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const.

Ex:
```
    let warna =['merah','kuning','hijau'];
    warna[0] ='biru';
    console.log(warna);
    //Output: ['biru','kuning','hijau'];
```
**Array Properties**, Array memiliki 5 properti yang sering digunakan yaitu constructor, length, index, input, dan prototype. seperti contoh .length, length akan mengembalikan nilai dari jumlah panjang data suatu array.
```
    let warna =['merah','kuning','hijau'];
    console.log(warna.length);
    //Output: 3
```
**Array Method**, Array memiliki method atau biasa disebut built-in methods. Contoh:
- .push() adalah method untuk menambahkan item  array pada urutan yang paling akhir.
``` 
    let list = {
        "Belajar";
        "Nyuci";
        "Masak";
    }
    list.push{"Mandi"};
    console.log(list);
    // Output: "Belajar","Nyuci","Masak", "Mandi"
```
- .pop() adalah method yang menghapus item array index terakhir.
``` 
    let list = {
        "Belajar";
        "Nyuci";
        "Masak";
    }
    list.pop();
    console.log(list);
    // Output: "Belajar","Nyuci";
```
- .shift() adalah method untuk menghapus item Array pada index pertama
``` 
    let list = {
        "Belajar";
        "Nyuci";
        "Masak";
    }
    list.shift();
    console.log(list);
    // Output: "Nyuci","masak";
```
- .unshift() adalah method untuk menambahkan item Array pada index pertama
``` 
    let list = {
        "Belajar";
        "Nyuci";
        "Masak";
    }
    list.unshift{"Mandi"};
    console.log(list);
    // Output: "Mandi","Belajar","Nyuci","Masak";
```
- .sort() adalah method untuk mengurutkan secara Ascending atau Descending Alphanumeric
```
    const number =[1,2,3,4];
    number.sort()
    console.log(number);
    //Output: [1,3,5,2,4]
```
**Looping pada Array**, Array memiliki built in methods untuk melakukan looping yaitu .map() dan .forEach()
- .forEach() adalah method untuk melakukan looping pada setiap elemen array. Gunakan .forEach() jika hanya memerlukan looping untuk menampilkan saja atau menyimpan ke database.

```
    let fish = [ "piranha", "barracuda", "cod", "eel" ];
    fish.forEach(individualFish => {
	console.log(individualFish);})
    //Output: piranha,barracuda,cod,eel
```
- .map() melakukan perulangan/looping dengan membuat array baru. Gunakan .map() jika akan melakukan operasi pada array seperti yang dapat mengubah nilai array sebelumnya.

```
    let fish = [ "piranha", "barracuda", "cod", "eel" ];
    let printFish = fish.map(individualFish => {
	console.log(individualFish);});

printFish;
    //Output: piranha,barracuda,cod,eel
```
## Multidimensional Array
Multidimensional Array bisa dianalogikan dengan array of array (Ada array didalam array). Sama seperti array satu dimensi, multidimensional array juga dapat menggunakan Property dan Method built-in Array.

## JavaScript Object
**Object** adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method). **Properti** adalah data lengkap dari sebuah object. **Method** adalah action dari sebuah object. Apa saja yang dapat dilakukan dari suatu object.

*Contoh Object person dengan properti*
```
    let person = {
        name : 'Putri',
        age : 20,
        isVerified: true,
    }
```
**Mengakses Object dan Property Object**
```
    let person = {
        name : 'Putri',
        age : 20,
        isVerified: true,
    }
    console.log(person.name); //Putri
```
Kita dapat melakukan update pada variabel dengan tipe data Object serta dapat menghapus properti dari object menggunakan delete operator.

**Looping Object**, Jika kita ingin menampilkan seluruh object properti. Kita bisa menggunakan looping.
```
    for (let data in object) {
        console.log(data[object]);
    }
```
## Git & GitHub Lanjutan 
- **Git log**, unttuk melihat perubahan pada suatu project
- **Git Checkout**, untuk berpindah branch atau membuat branch baru
- **Git Reset**, untuk mengembalikkan ke commit sebelumnya
- **Git Revert**, untuk membatalkan perubahan tanpa menghapus git commit sebelumnya
- **Clone**, untuk mengcopy codigan
- **Fork**, mengambil langsung file dari repository git.

## Javascript - Recursive
**Recursive**, adalah function yang memanggil dirinya sendiri sampai kondisi tertentu. ciri-ciri:
- Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. 
- Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. 

Contoh Mencari hasil dari nilai pangkat dengan rekursif
```
    function pow(x,n) {
        if (n=1){
            return x;
        } else {
            return x * pow(x, n-1);
        }
    }
    console.log(pow(2,3)) // 8
```
## JAVASCRIPT REGEX
**Regex**, adalah susunan karakter/deretan karakter spesial yang menggambarkan pattern/pola untuk pencarian text pada sebuah string atau document.
> REGEX = Text Matching

Contoh penggunaan Regex :
- Validasi input dari sebuah form
- Mencari keyword tertentu pada email atau halaman web
- Mencari IP adress dalam kisaran tertentu

Javascript regex punya beberapa built-in methods untuk Regex. Sala satunya adalah test(). test() mengembalikan nilai BOOLEAN (TRUE/FALSE) untuk kecocokan sebuat text yang dicari.
``` 
    let regex1 = new RegExp('Putri');
    console.log(regex1.test('Putri'))
    // true
```

## JavaScript - OOP
Object Oriented Programming (OOP) adalah suatu paradigma dalam pemrograman. OOP adalah principle. Jadi dapat diterapkan pada bahasa programming selain Javascript seperti Ruby, Python, dan Java.

Ada 4 hal pilar dalam OOP:
- Encapsulation, cara untuk membatasi akses langsung ke properti atau method dari sebuah objek.
- Abstraction, adalah sebuah teknik untuk menyembunyikan detail tertentu dari sebuah objek/method dan hanya menampilkan fungsionalitas atau fitur penting dari objek tersebut.
- Inheritance, sebuah proses dimana sebuah class mewariskan property dan methodnya ke class lain atau childnya.
- Polymorpishm, kemampuan dari suatu objek untuk memiliki banyak bentuk
