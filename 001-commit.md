# Best Practice Commit di GitHub

## Apa itu Commit?
Commit adalah sebuah "snapshot" atau rekaman perubahan kode di Git.  
Setiap commit menyimpan informasi mengenai **apa yang berubah**, **siapa yang mengubah**, dan **kapan perubahan dilakukan**.  

Dengan commit, kita dapat:
- Melacak riwayat perubahan kode.
- Membatalkan atau memperbaiki kesalahan dengan kembali ke versi sebelumnya.
- Bekerja kolaboratif tanpa kehilangan konteks perubahan.

---

## Fungsi Commit
1. **Mendokumentasikan perubahan**: Memberi catatan jelas tentang apa yang telah diubah.
2. **Memudahkan kolaborasi**: Tim bisa memahami maksud perubahan tanpa harus membaca seluruh kode.
3. **Meningkatkan traceability**: Mudah menelusuri siapa yang membuat perubahan tertentu.
4. **Mempermudah debugging**: Bisa menggunakan `git bisect` untuk menemukan commit yang menyebabkan bug.

---

## Bagaimana Cara Commit yang Baik?
Commit yang baik adalah commit yang **kecil, fokus, dan jelas**.  
Artinya setiap commit sebaiknya hanya berisi **satu tujuan perubahan**.  

**Contoh baik:**
- Commit khusus untuk memperbaiki bug.
- Commit khusus untuk menambahkan fitur.
- Commit khusus untuk memperbarui dokumentasi.

**Contoh buruk:**
- Satu commit mencampur perbaikan bug, penambahan fitur, dan perubahan konfigurasi sekaligus.

---

## Informasi yang Perlu Diperhatikan
1. **Pesan commit** harus ringkas dan deskriptif.  
2. **Bahasa yang konsisten** (disarankan Bahasa Inggris untuk kolaborasi global).  
3. **Menggunakan present tense** (misalnya: `Fix bug`, bukan `Fixed bug`).  
4. Jika perlu, tambahkan **body message** untuk detail teknis perubahan.  
5. Hindari commit dengan pesan umum seperti `update`, `fix`, atau `perubahan`.

---

## Aturan Umum Penulisan Commit
- **Gunakan format standar**:
  - `type: subject`
  - Contoh: `feat: add login functionality`
- **Gunakan prefix (conventional commits)**:
  - `feat` → untuk fitur baru.
  - `fix` → untuk perbaikan bug.
  - `docs` → untuk perubahan dokumentasi.
  - `style` → untuk formatting (tidak mengubah logika kode).
  - `refactor` → untuk perbaikan kode tanpa mengubah fungsionalitas.
  - `test` → untuk menambahkan/memperbaiki pengujian.
  - `chore` → untuk tugas lain (config, build, dll).

---

## Struktur Umum Commit Message
```txt
<type>[optional scope]: <short summary>

[optional body]

[optional footer(s)]
```


# Commit dengan Scope

## Apa itu Scope?
Scope adalah bagian opsional di dalam pesan commit yang menjelaskan **bagian atau konteks spesifik** dari perubahan.  
Biasanya ditulis di dalam tanda kurung setelah `type`.

**Struktur umum:**
```

<type>(<scope>): <summary>

```

## Kenapa Menggunakan Scope?
- Memberikan konteks tambahan di commit message.  
- Mempermudah pembacaan riwayat commit, terutama di repo besar.  
- Membantu tim cepat tahu bagian mana yang terpengaruh.

## Contoh Penggunaan Scope

### Dokumentasi
```

docs(git): catatan best practice commit github
docs(branch): tambahkan catatan tentang git merge vs rebase

```

### Fitur
```

feat(auth): implementasi login dengan JWT
feat(ui): tambah dark mode di halaman dashboard

```

### Perbaikan Bug
```

fix(api): perbaiki error 500 saat create user
fix(ui): atasi layout rusak di mobile

```

### Refactor
```

refactor(service): sederhanakan fungsi getUserData

```

---

## Tips Praktis
1. Scope boleh **singkat** (misalnya `git`, `ui`, `api`), jangan terlalu panjang.  
2. Gunakan scope kalau perubahan hanya berhubungan dengan **satu area khusus**.  
3. Kalau perubahan bersifat umum, scope bisa dikosongkan.  

---
```
