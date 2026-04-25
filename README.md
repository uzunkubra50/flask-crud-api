# 🛒 Product Management Microservice (Flask CRUD API)

Bu proje, Python ve Flask web çatısı (framework) kullanılarak geliştirilmiş, temel ürün yönetim işlemlerini gerçekleştiren bir **RESTful API** mikro hizmetidir. Bir yazılım mühendisi perspektifiyle; verilerin HTTP protokolü üzerinden nasıl yönetildiğini (CRUD operasyonları) ve API mimarisinin nasıl kurgulandığını uygulamalı olarak göstermektedir.

---

## 🚀 Proje Hakkında

Bu mikro hizmet, bir envanterdeki ürünlerin listelenmesi, yeni ürün girişi, mevcut ürünlerin güncellenmesi ve sistemden kaldırılması süreçlerini yönetir. Proje kapsamında hem **terminal (cURL)** hem de **Postman** üzerinden kapsamlı testler gerçekleştirilmiştir.

---

## ✨ Temel Özellikler (CRUD Operasyonları)

| Operasyon | Metot | Açıklama |
|-----------|-------|----------|
| **Create** | `POST` | Sisteme benzersiz ID, isim ve fiyat bilgisiyle yeni ürün ekler |
| **Read** | `GET` | Mevcut tüm ürünleri listeler veya belirli bir ürünü getirir |
| **Update** | `PUT` | Belirtilen ID'ye sahip ürünün bilgilerini revize eder |
| **Delete** | `DELETE` | Belirli bir ürünü kalıcı olarak sistemden kaldırır |

---

## 🛠️ Kullanılan Teknolojiler

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat-square&logo=python)
![Flask](https://img.shields.io/badge/Flask-Framework-black?style=flat-square&logo=flask)
![JSON](https://img.shields.io/badge/Format-JSON-orange?style=flat-square)
![Postman](https://img.shields.io/badge/Test-Postman-FF6C37?style=flat-square&logo=postman)
![Git](https://img.shields.io/badge/VCS-Git-F05032?style=flat-square&logo=git)

- **Backend:** Python 3 & Flask Framework
- **Veri Formatı:** JSON (JavaScript Object Notation)
- **API Test:** Postman & cURL
- **Versiyon Kontrol:** Git & GitHub

---

## 📡 API Uç Noktaları (Endpoints)

| Metot | Uç Nokta | İşlev |
|-------|----------|-------|
| `GET` | `/products` | Tüm ürün listesini döndürür |
| `GET` | `/products/{id}` | Belirtilen ID'deki ürünün detaylarını getirir |
| `POST` | `/products` | Yeni bir ürün nesnesi oluşturur |
| `PUT` | `/products/{id}` | Mevcut ürünün bilgilerini günceller |
| `DELETE` | `/products/{id}` | Ürünü sistemden siler |

### 📝 Örnek JSON Payload

`POST` veya `PUT` isteklerinde kullanılan veri yapısı:

```json
{
    "id": 146,
    "name": "Laptop Bag",
    "price": 42.00
}
```

---

## ⚙️ Kurulum ve Çalıştırma

### 1. Depoyu Klonlayın
```bash
git clone https://github.com/uzunkubra50/flask-crud-api.git
cd flask-crud-api
```

### 2. Gerekli Paketleri Yükleyin
```bash
pip install flask flask-cors
```

### 3. Uygulamayı Başlatın
```bash
python3 jmgdo-microservices/CRUD/products.py
```

### 4. Erişim
Sunucu varsayılan olarak aşağıdaki adreste dinlemeye başlayacaktır:
```
http://localhost:5000
```

---

## 🧪 API Test Örnekleri (cURL)

**Tüm ürünleri listele:**
```bash
curl -X GET http://localhost:5000/products
```

**Yeni ürün ekle:**
```bash
curl -X POST http://localhost:5000/products \
  -H "Content-Type: application/json" \
  -d '{"id": 146, "name": "Laptop Bag", "price": 42.00}'
```

**Ürün güncelle:**
```bash
curl -X PUT http://localhost:5000/products/146 \
  -H "Content-Type: application/json" \
  -d '{"price": 49.99}'
```

**Ürün sil:**
```bash
curl -X DELETE http://localhost:5000/products/146
```

---

## 👤 Geliştirici

**uzunkubra50**  
Bu proje, bulut tabanlı mikro hizmet mimarileri ve API geliştirme pratikleri kapsamında hazırlanmıştır.
