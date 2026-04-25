# 🛒 Product Management Microservice (Flask CRUD API)

Bu proje, Python ve Flask web çatısı (framework) kullanılarak geliştirilmiş, temel ürün yönetim işlemlerini gerçekleştiren bir **RESTful API** mikro hizmetidir. Bir yazılım mühendisi perspektifiyle; verilerin HTTP protokolü üzerinden nasıl yönetildiğini (CRUD operasyonları) ve API mimarisinin nasıl kurgulandığını uygulamalı olarak göstermektedir.

## 🚀 Proje Hakkında
Bu mikro hizmet, bir envanterdeki ürünlerin listelenmesi, yeni ürün girişi, mevcut ürünlerin güncellenmesi ve sistemden kaldırılması süreçlerini yönetir. Proje kapsamında hem **terminal (cURL)** hem de **Postman** üzerinden kapsamlı testler gerçekleştirilmiştir.

## ✨ Temel Özellikler (CRUD Operasyonları)
Uygulama, standart HTTP metotlarını kullanarak şu işlemleri destekler:
* **Create (Oluştur):** Sisteme benzersiz ID, isim ve fiyat bilgisiyle yeni ürün ekler (`POST`).
* **Read (Oku):** Mevcut tüm ürünleri listeler veya belirli bir ürünü getirir (`GET`).
* **Update (Güncelle):** Belirtilen ID'ye sahip ürünün fiyat bilgisini revize eder (`PUT`).
* **Delete (Sil):** Belirli bir ürünü kalıcı olarak sistemden kaldırır (`DELETE`).

## 🛠️ Kullanılan Teknolojiler ve Araçlar
* **Backend:** Python 3 & Flask Framework
* **Veri Formatı:** JSON (JavaScript Object Notation)
* **API Test:** Postman & cURL (Command Line Interface)
* **Versiyon Kontrol:** Git & GitHub

## 📡 API Uç Noktaları (Endpoints)

| Metot | Uç Nokta (Endpoint) | İşlev |
| :--- | :--- | :--- |
| `GET` | `/products` | Tüm ürün listesini döndürür. |
| `GET` | `/products/{id}` | Belirtilen ID'deki ürünün detaylarını getirir. |
| `POST` | `/products` | Yeni bir ürün nesnesi oluşturur. |
| `PUT` | `/products/{id}` | Mevcut ürünün bilgilerini günceller. |
| `DELETE` | `/products/{id}` | Ürünü veri tabanından siler. |

### 📝 Örnek JSON Gövdesi (Payload)
`POST` veya `PUT` isteklerinde kullanılan veri yapısı:
```json
{
    "id": 146,
    "name": "Laptop Bag",
    "price": 42.00
}
⚙️ Kurulum ve Çalıştırma
Projeyi yerel makinenizde çalıştırmak için:

Depoyu Klonlayın:

Bash
git clone [https://github.com/uzunkubra50/flask-crud-api.git](https://github.com/uzunkubra50/flask-crud-api.git)
Gerekli Paketleri Yükleyin:

Bash
pip install flask flask-cors
Uygulamayı Başlatın:

Bash
python3 jmgdo-microservices/CRUD/products.py
Erişim: Sunucu varsayılan olarak http://localhost:5000 adresinde dinlemeye başlayacaktır.

Geliştirici: uzunkubra50

Bu proje, bulut tabanlı mikro hizmet mimarileri ve API geliştirme pratikleri kapsamında hazırlanmıştır.
