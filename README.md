# Petualangan Air

Media Pembelajaran Interaktif IPAS Kelas V, Bab 4 **Air Sumber Kehidupan**.

Pengembang pembelajaran: **Arga Widyatama**, SDN Bandarharjo 02. Aplikasi dan ilustrasi dikembangkan dengan bantuan AI dan penelaahan guru.

## Membuka MPI

Unduh repositori melalui **Code → Download ZIP**, lalu ekstrak seluruh isinya. Buka `dist/index.html` menggunakan Chrome atau Edge. Pertahankan susunan folder agar gambar dan audio dapat ditemukan.

Untuk menjalankan lewat server lokal, dari folder repositori jalankan:

```sh
python3 -m http.server 8000 --directory dist
```

Kemudian buka `http://localhost:8000`. Pada Windows, perintah Python dapat berupa `python` atau `py`.

## Isi pembelajaran

- Tujuan pembelajaran dan cek awal.
- Tiga misi tentang aliran air, siklus air, serta resapan dan tindakan menjaga air.
- Pengelompokan kartu, permainan pasangan, dan kegiatan mengambil keputusan.
- Evaluasi, refleksi, rencana tindakan, serta sertifikat hasil belajar yang dapat dicetak.
- Layar penuh, pengaturan suara, pengurangan gerak, dan tombol peserta baru.

Versi awal repositori ini memuat MPI **2.9**, termasuk **12 gambar PNG** dan **8 audio WAV**. Berkas gambar dipertahankan pada resolusi aslinya. Musik serta efek suara disintesis khusus untuk aplikasi; pemutaran tidak menggunakan YouTube.

## Struktur proyek

```text
dist/                      Aplikasi HTML, CSS, dan JavaScript
  assets/                  Ilustrasi PNG
  audio/                   Musik dan efek suara WAV
checks/                    Pemeriksaan fungsi aplikasi
scripts/package_offline.py Pembuat paket HTML offline
scripts/create_audio.py    Pembuat aset audio
.openai/hosting.json        Identitas proyek pada ChatGPT Sites
```

## Membuat paket offline

Dari folder repositori, jalankan:

```sh
python3 scripts/package_offline.py
```

Skrip mencetak lokasi hasil `Petualangan-Air-Offline.zip` pada folder `deliverables` di sebelah folder repositori. Ekstrak ZIP lalu buka `Petualangan-Air.html`. Paket ini menyertakan gambar, audio, dan kode aplikasi di dalam HTML.

Tunggu pemuatan aset sebelum memulai. Suara diaktifkan setelah pengguna berinteraksi dengan aplikasi. Fitur pembacaan teks bergantung pada dukungan suara peramban atau perangkat.

## Data peserta

Nama, jawaban, dan kemajuan belajar disimpan pada perangkat yang digunakan. Data tidak otomatis dikirim kepada guru. Simpan hasil sebelum menggunakan **Peserta baru / Ulang dari awal**, karena tindakan tersebut mengosongkan data peserta sebelumnya.

## Pengembangan

Sumber awal diambil dari proyek Petualangan Air pada commit `8a28ac19c184308f19c62229e595e40b5685f33a`.

Repositori ini menyimpan kode sumber dan aset. Publikasi melalui ChatGPT Sites dikelola terpisah; perubahan di GitHub tidak otomatis menerbitkan ulang situs. Penggunaan pada IFP tetap perlu diperiksa di perangkat kelas.

Acuan materi: buku siswa IPAS Kelas V edisi revisi 2024, Bab 4 Air Sumber Kehidupan.
