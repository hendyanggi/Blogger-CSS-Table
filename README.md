![Blogspot Tabel Responsif dengan CSS](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjYugzbbsK-vze93MsFZcTXT7vHUZP1ACrAWnROI1AIMI3S1U8A_G-iTjS8KUN7l0kRdxLi4JeY4PUq0czvogo5ZdhMgbkojcXulOSQjN9AQ665QvPxgo3WWMSTnZLxrIPNhpPb2SRLTwjAfMPSh3lJiA78ZiS87In5FR5FhQFg_0HylswpN9Hb1LfMjtdh/s763/Screenshot%202025-07-20%20at%2004-15-18%20.png "Blogspot Tabel Responsif dengan CSS")
# Blogger/Blogspot Tabel Responsif dengan CSS

Proyek ini menyediakan gaya CSS untuk membuat tabel yang menarik dan responsif. Tabel ini dirancang untuk beradaptasi dengan berbagai ukuran layar, memastikan pengalaman pengguna yang baik di perangkat mobile serta desktop.

## Fitur

- **Tampilan Menarik**: Menggunakan warna latar belakang, padding, dan hover effects untuk meningkatkan keterbacaan.
- **Responsif**: Tabel akan menyesuaikan tampilannya di layar kecil dengan menggunakan teknik CSS yang sesuai.
- **Mudah Digunakan**: Cukup salin dan tempel CSS dan markup HTML yang disediakan untuk mulai menggunakan.

# Memasang CSS Tabel Responsif di Blogger

## Penjelasan

Tabel responsif memungkinkan konten tabel ditampilkan dengan baik di berbagai ukuran layar. Dengan menggunakan CSS yang tepat, Anda dapat membuat tabel yang tidak hanya menarik, tetapi juga mudah dibaca di perangkat mobile.

## Cara Memasang CSS Tabel Responsif di Blogger

### 1. Masuk ke Dasbor Blogger

- Buka [Blogger](https://www.blogger.com) dan masuk ke akun Anda.

### 2. Pilih Blog Anda

- Dari dasbor, pilih blog yang ingin Anda edit.

### 3. Buka Tema

- Di menu sebelah kiri, klik pada **Tema**.

### 4. Edit HTML

- Klik pada tombol **Edit HTML**.

### 5. Tempelkan CSS

- Cari tag `<head>` di dalam kode HTML.
- Tempelkan kode CSS berikut sebelum tag penutup `</head>`:

```css
/* Gaya umum untuk tabel */
table {
    width: 100%;
    border-collapse: collapse;
    margin: 20px 0;
    font-size: 18px;
    text-align: left;
}

/* Gaya untuk header tabel */
th {
    background-color: #4CAF50; /* Warna latar belakang hijau */
    color: white;
    padding: 12px 15px;
}

/* Gaya untuk sel tabel */
td {
    border: 1px solid #ddd; /* Garis batas abu-abu */
    padding: 12px 15px;
}

/* Gaya untuk baris genap */
tr:nth-child(even) {
    background-color: #f2f2f2; /* Warna latar belakang abu-abu muda */
}

/* Gaya saat hover pada baris */
tr:hover {
    background-color: #ddd; /* Warna latar belakang saat hover */
}

/* Responsif untuk layar kecil */
@media (max-width: 600px) {
    table, thead, tbody, th, td, tr {
        display: block; /* Menjadikan elemen blok */
    }

    th {
        display: none; /* Menyembunyikan header pada layar kecil */
    }

    tr {
        margin-bottom: 15px; /* Jarak antar baris */
    }

    td {
        text-align: right; /* Rata kanan untuk sel */
        position: relative;
        padding-left: 50%; /* Ruang untuk label */
    }

    td::before {
        content: attr(data-label); /* Menambahkan label sebelum nilai */
        position: absolute;
        left: 0;
        padding-left: 15px; /* Jarak label dari kiri */
        font-weight: bold;
        text-transform: uppercase; /* Huruf kapital */
    }
}
