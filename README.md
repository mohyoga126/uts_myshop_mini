# DOKUMENTASI WIDGET - MyShop Mini

## Daftar Widget yang Digunakan dan Fungsinya

---

## 1️⃣ **HOME SCREEN**

### Widget Utama:
- **Scaffold**: Widget dasar yang menyediakan struktur visual material design (AppBar, Body, dll)
- **AppBar**: Menampilkan bar di bagian atas aplikasi dengan judul "MyShop Mini"
- **Container**: Pembungkus widget dengan dekorasi gradient background
- **SafeArea**: Memastikan konten tidak tertutup oleh notch atau system UI
- **Column**: Menyusun widget secara vertikal (icon, text, cards)
- **Icon**: Menampilkan ikon shopping bag sebagai header
- **Text**: Menampilkan teks "Selamat Datang!" dan deskripsi
- **Row**: Menyusun 3 Card kategori secara horizontal
- **Card**: Menampilkan kategori dalam bentuk kartu dengan efek elevation
- **GestureDetector**: Mendeteksi tap/sentuhan pada kategori untuk navigasi
- **Expanded**: Membuat widget mengisi ruang yang tersedia
- **SizedBox**: Memberikan jarak/spacing antar widget

### Fitur Dekorasi:
- **BoxDecoration**: Memberikan gradient, border radius pada container
- **LinearGradient**: Membuat efek gradasi warna background
- **BorderRadius**: Membuat sudut card melengkung

---

## 2️⃣ **PRODUCT LIST SCREEN**

### Widget Utama:
- **Scaffold**: Struktur dasar halaman
- **AppBar**: Menampilkan nama kategori di header
- **Column**: Menyusun header info dan grid produk
- **Container**: Wrapper untuk header dengan background biru
- **GridView.builder**: Menampilkan produk dalam bentuk grid 2 kolom secara dinamis
- **SliverGridDelegateWithFixedCrossAxisCount**: Mengatur jumlah kolom (2) dan spacing grid
- **Card**: Kartu untuk setiap item produk
- **GestureDetector**: Mendeteksi tap pada produk untuk navigasi ke detail
- **Icon**: Menampilkan ikon produk
- **Text**: Menampilkan nama dan harga produk

### Parameter GridView:
- **crossAxisCount: 2**: Membuat 2 kolom
- **crossAxisSpacing**: Jarak horizontal antar item
- **mainAxisSpacing**: Jarak vertikal antar item
- **childAspectRatio**: Rasio lebar/tinggi setiap item

---

## 3️⃣ **PRODUCT DETAIL SCREEN**

### Widget Utama:
- **Scaffold**: Struktur dasar halaman detail
- **AppBar**: Header dengan judul "Detail Produk"
- **Container**: Wrapper utama dengan gradient background
- **Column**: Menyusun elemen secara vertikal di tengah
- **Icon**: Menampilkan ikon produk berukuran besar (120px)
- **Text**: Menampilkan nama produk
- **Container**: Wrapper untuk price dengan background hijau
- **ElevatedButton**: Tombol untuk kembali ke ProductList
- **BoxShadow**: Memberikan efek bayangan pada icon dan button

### Alignment:
- **MainAxisAlignment.center**: Menyusun widget di tengah layar secara vertikal

---

## 4️⃣ **NAVIGASI**

### Widget Navigasi:
- **Navigator.push()**: Berpindah ke halaman baru dengan animasi
- **MaterialPageRoute**: Membuat route dengan animasi material design
- **Navigator.pop()**: Kembali ke halaman sebelumnya

### Flow Navigasi:
```
HomeScreen 
    → ProductListScreen (dengan parameter category)
        → ProductDetailScreen (dengan parameter product)
            → kembali dengan Navigator.pop()
```

---

## 5️⃣ **MODEL DATA**

### Class Product:
```dart
- name: String (nama produk)
- price: String (harga produk)
- icon: IconData (ikon produk)
- color: Color (warna tema produk)
```

---

## 6️⃣ **STYLING & THEME**

### Widget Styling:
- **MaterialApp**: Root widget dengan konfigurasi theme global
- **ThemeData**: Mengatur tema aplikasi (warna primary, background, AppBar)
- **TextStyle**: Styling untuk text (fontSize, fontWeight, color)
- **BoxDecoration**: Dekorasi container (gradient, border, shadow)
- **BorderRadius.circular()**: Membuat sudut melengkung
- **BoxShadow**: Efek bayangan untuk depth/kedalaman visual

---

## 7️⃣ **WIDGET HELPER**

### Widget Pembantu:
- **Padding**: Memberikan padding/jarak dalam widget
- **SizedBox**: Memberikan jarak vertikal/horizontal tetap
- **Expanded**: Membuat widget mengisi ruang tersedia
- **Flexible**: Alternatif Expanded dengan flex factor

---

## 🎨 **FITUR KREATIF TAMBAHAN**

1. **Gradient Background**: Menggunakan LinearGradient untuk visual menarik
2. **Shadow Effects**: BoxShadow untuk kedalaman visual
3. **Color Coding**: Setiap kategori/produk punya warna tema tersendiri
4. **Rounded Corners**: BorderRadius untuk desain modern
5. **Icon Variety**: Icon berbeda untuk tiap produk
6. **Responsive Layout**: Grid yang adaptif
7. **Interactive Feedback**: Card elevation berubah saat ditekan
8. **Professional UI**: Spacing, alignment, dan typography yang konsisten

---

## 📊 **STRUKTUR WIDGET TREE**

```
MyShopMiniApp (MaterialApp)
└── HomeScreen (Scaffold)
    ├── AppBar
    └── Body (Container + Column)
        ├── Icon
        ├── Text (Title + Subtitle)
        └── Row (3x Category Cards)
            └── GestureDetector → Navigator.push()

ProductListScreen (Scaffold)
├── AppBar
└── Body (Column)
    ├── Container (Header Info)
    └── GridView.builder (2 columns)
        └── Card Products
            └── GestureDetector → Navigator.push()

ProductDetailScreen (Scaffold)
├── AppBar
└── Body (Container + Column)
    ├── Icon (Large)
    ├── Text (Name)
    ├── Container (Price Badge)
    └── ElevatedButton → Navigator.pop()
```

---

## ✅ **KESESUAIAN DENGAN SOAL UTS**

✓ Halaman Home dengan 3 kategori (Makanan, Minuman, Elektronik)
✓ Navigasi dari kategori ke ProductList
✓ Grid 2 kolom untuk menampilkan produk
✓ Detail produk menampilkan icon, nama, dan harga
✓ Navigasi back menggunakan Navigator.pop()
✓ Semua widget tercantum dengan fungsi lengkap
