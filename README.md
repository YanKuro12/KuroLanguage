Masih Dalam Tahap Pengerjaan!
# KuroLangX
**KuroLangX** (KLX) adalah bahasa pemrograman scripting modern dan ringan yang dirancang untuk automation, bot scripting, dan manipulasi file.  
File KuroLangX menggunakan ekstensi `.kuro` (script) dan `.kuroc` (compiled).

---

## Fitur Utama

### Priv Module
- Sistem keamanan built-in.
- Kontrol akses runtime untuk file yang diimport.
- Memungkinkan developer menentukan siapa yang bisa mengakses resource tertentu.

### Built-in Modules
- **storage** → simpan, ambil, hapus, cek, backup data.  
- **fs** → API File System: baca, tulis, append, cek file/folder, buat folder, list folder, ukuran file.  
- **log** → logging: info, warn, error, debug, trace.  
- **bot** → event-driven bot framework: kirim pesan, reply, onMessage, onReady.

### Runtime
- Variabel, assignment, konstanta.
- Fungsi dengan parameter & return.
- Control flow: if, oneif, loops.
- Operator matematika dan logika.
- Konversi tipe: string ↔ number.

---
### Contoh Pemakaian Yang Benar
### Print
Console.print("Hello, KuroLangX!");
### Input
Console.input("Hello, Ingin Nomer Berapa?");
### variable
var nama = "YanKuro"
var umur = 15
### import
import math as m #modules
import main.kuro
### Fungsi
FuncGroup tambah(a, b) {
    return a + b
}
### Pemanggilan Fungsi
OpenGroup tambah(a, b)
