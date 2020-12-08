# Tugas 16 MySQL (MongoDB)

#### 1. Buat database dengan nama matkul dan insert 5 buah data yang jika ditampilkan akan seperti gambar dibawah ini!
![Tugas 16](https://lh3.googleusercontent.com/NfnNwzIourBSUDOBJTtS2A4WToSp8dY3ooHQOevXPsccslT9YEY6N5SOpg5mqkYv-z71oADv8peyI8QL0LloLJ_OncVBY16-noYQMxYr34AlzC27PhZ9T32bw5dH3P-A41YAG0gQ)
```
use matkul

db.matkul.save({matkul:"Algoritma & Pemrograman", kode_matkul:"1234567", nama_dosen:"Jamal Kosasih"});
db.matkul.save({matkul:"Rekayasa Perangkat Lunak", kode_matkul:"1234568", nama_dosen:"Ivan Bagus"});
db.matkul.save({matkul:"Sistem Basis Data", kode_matkul:"1234569", nama_dosen:"Anida Nur Afika"});
db.matkul.save({matkul:"Pengantar Ilmu Komputer", kode_matkul:"1234561", nama_dosen:"Nico Ariesto"});
db.matkul.save({matkul:"Bahasa Indonesia", kode_matkul:"1234562", nama_dosen:"Fifi Meilani"});
```

#### 2. Ubah nama_dosen menjadi Sekar Wandansari untuk kode_matkul = 1234562.
```
db.matkul.update({kode_matkul:"1234562"},{$set:{nama_dosen:"Sekar Wandansari"}},false,true);
```

#### 3. Hapus data nama dosen a/n Jamal Kosasih dan Ivan Bagus dari tabel matkul!
```
db.matkul.remove({kode_matkul:"1234562"});
```

#### 4. Hapus database matkul!
```
use matkul
db.dropDatabase()
```
