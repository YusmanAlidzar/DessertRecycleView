# DessertRecycleView

## Tugas PAM (Pengembangan Aplikasi Mobile)

**Modul 2 - Praktikum 07**

DessertRecycleView adalah aplikasi Android sederhana yang menampilkan daftar dessert menggunakan komponen `RecyclerView`. Aplikasi ini dibuat sebagai implementasi materi pembuatan list dinamis pada Android dengan Kotlin.

## Fitur

- Menampilkan judul **Droid Desserts**.
- Menampilkan daftar dessert dalam tampilan vertikal.
- Setiap item menampilkan gambar dessert dan deskripsinya.
- Menggunakan warna latar lingkaran yang berbeda untuk setiap dessert.
- Mendukung tampilan edge-to-edge dan penyesuaian inset system bar.

Daftar dessert yang tersedia:

1. Donuts
2. Ice cream sandwich
3. Froyo

## Teknologi yang Digunakan

- Kotlin
- Android SDK
- AndroidX
- `RecyclerView`
- `LinearLayoutManager`
- Gradle Kotlin DSL
- Compile SDK 37
- Minimum SDK 27
- Java 11

## Struktur Proyek

```text
DessertRecycleView/
├── app/
│   └── src/
│       ├── androidTest/       # Pengujian instrumentasi Android
│       ├── main/
│       │   ├── java/lat/pam/dessertrecycleview/
│       │   │   ├── Dessert.kt
│       │   │   ├── DessertAdapter.kt
│       │   │   └── MainActivity.kt
│       │   └── res/
│       │       ├── drawable/  # Gambar dessert
│       │       └── layout/    # Layout activity dan item RecyclerView
│       └── test/              # Pengujian unit
├── gradle/
│   └── libs.versions.toml    # Versi plugin dan dependency
├── build.gradle.kts
├── settings.gradle.kts
└── gradlew.bat
```

## Komponen Utama

### `Dessert.kt`

Mendefinisikan data model dessert yang terdiri dari:

- `description`: deskripsi dessert.
- `imageRes`: resource gambar dessert.
- `colorHex`: warna latar dalam format HEX.

### `DessertAdapter.kt`

Menghubungkan data dessert dengan layout item `RecyclerView`. Adapter mengatur teks deskripsi, gambar, dan warna latar lingkaran pada setiap item.

### `MainActivity.kt`

Membuat daftar dessert, mengatur `LinearLayoutManager`, dan memasang `DessertAdapter` pada `RecyclerView`.