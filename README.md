# 📚 Kütüphane Yönetim Sistemi / Library Management System

Bu proje, Yönetim Bilişim Sistemleri (YBS) eğitimi kapsamında geliştirilmiş, dinamik ve tam fonksiyonel bir **Kütüphane Yönetim Sistemi** web uygulamasıdır.
Sistem kitap yönetiminden üyelik işlemlerine, kitap ödünç alma mekanizmasından sepet mantığına kadar modern bir kütüphanenin ihtiyaç duyabileceği tüm temel 
süreçleri dijitalleştirmek üzere tasarlanmıştır.

🌍 **Canlı Önizleme / Live Demo:** https://ybs7grup.page.gd

---

## 🚀 Özellikler (Features)

### 👤 Kullanıcı & Kimlik Doğrulama İşlemleri (User & Auth)
* **Kullanıcı Kaydı ve Girişi:** Güvenli şifreleme altyapısıyla kullanıcı kayıt (`register.php`) ve giriş (`login.php`) sistemleri.
* **Profil Yönetimi:** Kullanıcıların kendi hesap bilgilerini görüntüleyip güncelleyebileceği panel (`account.php`).
* **Güvenli Çıkış:** Oturum yönetimini sonlandıran güvenli çıkış mekanizması (`logout.php`).

### 📖 Kitap & Katalog Yönetimi (Book Management)
* **CRUD Operasyonları:** Sistem yöneticileri için kitap ekleme (`add_book.php`), listeleme (`books.php`), güncelleme (`guncelle.php`) ve silme (`sil.php`) yetenekleri.
* **Kapak Görseli Yükleme:** Eklenen kitaplara dinamik olarak görsel yükleme ve sunucuda depolama desteği (`assets/uploads/`).
* **Detaylı İnceleme:** Her kitabın detaylı bilgilerinin görüntülenebildiği dinamik sayfa (`book_details.php`).

### 🛒 Ödünç Alma & Sepet Sistemi (Borrowing & Cart Mechanism)
* **Kitap Sepeti:** Kullanıcıların ödünç almak istedikleri kitapları bir arada toplayabildikleri sepet yapısı (`cart.php`).
* **Ödünç Alma İşlemi:** Seçilen kitapların kullanıcı üzerine dinamik olarak kaydedilmesi (`borrow.php`).
* **Ödünç Takibi:** Kullanıcıların mevcut ödünç aldıkları kitapları görebileceği panel (`my_loans.php`).
* **İade Süreci:** Ödünç alınan kitapların kütüphaneye geri teslim edilmesi algoritması (`return_book.php`).

---

## 🛠️ Kullanılan Teknolojiler (Tech Stack)

* **Backend:** PHP (Nesne yönelimli süreçler ve session yönetimi)
* **Database:** MySQL / MariaDB (İlişkisel veritabanı mimarisi)
* **Frontend:** HTML5, CSS3, Bootstrap (Dinamik ve responsive tasarım)
* **Asset Management:** Özelleştirilmiş kütüphane logoları ve harici CSS kütüphaneleri

---

## 📂 Proje Yapısı (Directory Structure)

```text
htdocs/
│
├── assets/                  # Stil dosyaları ve statik görseller
│   ├── css/
│   │   └── style.css
│   └── images/              # Logolar ve arayüz ikonları
│   └── uploads/             # Dinamik yüklenen kitap kapak görselleri
│
├── partials/                # Tekrar kullanılabilir bileşenler
│   ├── header.php           # Üst menü ve navigasyon
│   └── footer.php           # Alt bilgi alanı
│
├── auth.php                 # Yetkilendirme ve oturum kontrolü
├── login.php / register.php # Giriş ve kayıt sayfaları
├── account.php              # Kullanıcı profil sayfası
│
├── books.php                # Kitap katalog listesi
├── book_details.php         # Kitap detay sayfası
├── add_book.php             # Kitap ekleme formu
├── guncelle.php / sil.php   # Kitap düzenleme ve silme motorları
│
├── cart.php                 # Ödünç alınacak kitap sepeti
├── borrow.php               # Ödünç alma işlem motoru
├── my_loans.php             # Kullanıcının aktif ödünç listesi
├── return_book.php          # Kitap iade işlem motoru
│
└── if0_41646798_library_system.sql # Veritabanı şeması ve örnek veriler
```

---

## 💻 Kurulum Talimatları (Local Setup)

Projeyi yerel bilgisayarınızda (Localhost) çalıştırmak için aşağıdaki adımları takip edebilirsiniz:

1. **Projeyi Klonlayın:**
   ```bash
   git clone https://github.com
   ```
2. **Lokal Sunucuya Taşıyın:**
   Klonlanan klasörü XAMPP kullanıyorsanız `htdocs` klasörünün içine, WampServer kullanıyorsanız `www` klasörünün içine taşıyın.

3. **Veritabanını İçe Aktarın:**
   * tarayıcınızdan `localhost/phpmyadmin` adresine gidin.
   * `library_system` adında yeni bir veritabanı oluşturun.
   * Proje klasöründeki `.sql` uzantılı dosyayı seçerek **İçe Aktar (Import)** deyin.

4. **Veritabanı Bağlantısını Yapılandırın:**
   * `db.php` veya veritabanı bağlantısını sağlayan ilgili dosyayı açarak yerel veritabanı kullanıcı adınızı ve şifrenizi girin.

5. **Çalıştırın:**
   Tarayıcınızdan `http://localhost/proje_klasor_adi/index.php` adresine giderek projeyi test edin.

---

## 👤 Proje Geliştiricileri
Bu proje **YBS 7. Grup** tarafından bir takım çalışması ürünü olarak geliştirilmiştir.
