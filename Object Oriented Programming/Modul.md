Agenda :
1. Pengenalan Object Oriented Programming
2. Class
3. Object
4. Inheritance
5. Iterable dan Iterators
6. Standard Javascript Classes
dll


# -------------------------------------------------------------------------- #
#                  1. PENGENALAN OBJECT ORIENTED PROGRAMMINH                 #
# -------------------------------------------------------------------------- #
 Pengenalan
 1. Object Oriented Programming adalah sudut pandang bahasa pemrograman yang berkonsep "objek".
 2. Ada banyak sudut pandang bahasa pemrograman, namun OOP adalah yang sangat populer saat ini.
 3. Ada beberapa istilah yang perlu dimengerti dalam OOP, yaitu: Object dan class.

OBJECT adalah data yang berisi field/properties/attributes dan method / function / behavior.

CLASS adalah blueprint, prototype atau cetakan untuk membuat Object.
CLASS berisikan deklarasi semua properties dan functions yang dimiliki oleh Object.
Setiap OBJECT selalu dibuat dari CLASS.
Dan sebuah CLASS bisa membuat OBJECT tanpa batas.

OOP di Javascript
Javascript sendiri sebenarnya sejak awal dibuat sebagai bahasa prosedural, bukan bahasa pemrogramman berorientasi objek.

Oleh karena itu, implementasi OOP di javascript memang tidak sedetail bahasa pemrograman lain yang memang dari awal merupakan
bahasa pemrograman OOP seperti Java dan C++.

# ---------------------------------------------------------------------------- #
#                        2. MEMBUAT CONTRUCTOR FUNCTION                        #
# ---------------------------------------------------------------------------- #
# Membuat Object :
Sebenarnya kita sudah belajar tipe data object, dengan cara membuat variable dengan tipe data object.

Namun pembuatan object menggunakan tipe data object, akan membuat object yang selalu unik,
sedangkan dalam OOP, biasanya kita akan membuat class sebagai cetakan, sehingga bisa membuat object dengan karakteriktik yang sama berkali-kali,
tanpa harus mendeklarasikan object berkali-kali seperti mengunakan tipe data object.

# Membuat Contructor function
Sebelum EcmaScript versi 6, pembuatan class, biasanya menggunakan function. Hal ini dikarenakan sebenarnya javascript bukanlah bahasa pemrograman yang fokus ke OOP

untuk membuat class di js lama, kita bisa membuat function.

Function ini kita sebut dengan Contructor Function.

# contoh Constructor Function :
function Person() {

}

** Note : Khusus untuk contructor function base practice nya diawal kata menggunakan upper case (--> Person / PremiumMember, dll).

# Membuat Object dari Contructor Function
Setelah kita membuat class, jika ingin membuat object dari class tersebut, kita bisa menggunakan kata kunci new, lalu diikuti dengan nama contructor function nya.

# Contoh Membuat Object
function Person() {

}

const eko = new Person(); // object eko
const budi = new Person(); // object budi

# ----------------------------------------------------------------------- #
#                   3. PROPERTY DI CONSTRUCTOR FUNCTION                   #
# ----------------------------------------------------------------------- #
Sebenarnya setelah kita membuat object, kita bisa dengan mudah menambahkan property ke dalam object tersebut hanya dengan menggunakan nama variable nya, diikuti tanda titik dan nama property.

Namun jika seperti itu, alhasil, constructor function yang sudah kita buat tidak terlalu berguna, karena property nya hanya ada di object yang kita tambahkan property.

Untuk menambahkan property di dalam semua object yang dibuat dari constructor function, kita bisa menggunakan kata kunci this lalu diikuti dengan nama property nya.

# Contoh Property di Contructor Function
function Person() {        // ---> Class sebagai cetakan
    this.firstName  = "";
    this.lastName   = "";
}

const eko = new Person();  // ---> object ini jadi punya 2 properti dari class / constructor function
const budi = new Person(); // ---> object ini jadi punya 2 properti dari class / constructor function


# ----------------------------------------------------------------------- #
#                    4. METHOD DI CONSTRUCTOR FUNCTION                    #
# ----------------------------------------------------------------------- #
Sama seperti pada tipe data object biasanya, kita juga bisa menambahkan method di dalam constructor function.

JIka kita tambahkan method di constructor function, secara otomatis object yang dibuat akan memiliki method tersebut.