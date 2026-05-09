UTS Teknik Kompilasi
Implementasi Fase-Fase Kompilator
Nama  : M. Sahrul Ramdani
NIM   : 231011400290
Kelas : 06TPLE006
Deskripsi Tugas
Tugas ini membahas implementasi fase-fase kompilator pada mata kuliah Teknik Kompilasi dengan topik Lexer, Parser (EBNF), Abstract Syntax Tree (AST), dan Three Address Code (TAC). Program yang dibuat merupakan sebuah Mini Compiler yang telah dikembangkan untuk mendukung operator pangkat (^).
Fase Kompilasi
1. Lexical Analysis (Lexer): Memecah kode sumber menjadi token.
2. Syntax Analysis (Parser): Membangun Abstract Syntax Tree (AST).
3. Intermediate Code Generation: Menghasilkan Three Address Code (TAC).
Tantangan Utama
Penambahan operator pangkat (^) dengan prioritas lebih tinggi dibandingkan perkalian (*) dan pembagian (/).
Perubahan Kode
Lexer: Regex diperbarui menjadi [+*/()\-^]
Parser: Menambahkan fungsi power()
Hierarki: Menghubungkan term() ke power()
Uji Coba Program
Input: a ^ 2 + b * c
Symbol Table: {'a': 5, 'b': 10, 'c': 2}
Output TAC:
t1 = a ^ 2.0
t2 = b * c
t3 = t1 + t2
