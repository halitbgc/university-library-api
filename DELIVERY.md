# **OpenAPI Tasarımı Ödevi Teslim Raporu**

## 👤 Öğrenci Bilgileri

- **Ad Soyad**: Halit Bağcı  
- **Öğrenci Numarası**: 170423841

---

## **📂 OpenAPI YAML Dosyası**

- **openapi.yaml** dosyasını GitHub repoma yükledim. Swagger Editör üzerinde test edilmiştir ve çalışmaktadır.

### **🔗 GitHub Repo Linki**

\[GitHub projenizin linkini buraya yazınız\]

---

## **📝 API Açıklaması**

Aşağıda tasarladığınız API’nin genel yapısını ve önemli noktalarını açıklayınız:

Bu proje, üniversiteye ait çevrimiçi bir kütüphane sistemine yönelik bir REST API tanımıdır.

**📦 Varlıklar**  
\- Book: Kitap bilgileri (başlık, yazar vs.)  
\- Student: Öğrenci bilgileri (isim, numara, email vs.)  
\- Loan: Ödünç alma işlemleri (kitap, öğrenci, tarih vs.)

**🔄 CRUD İşlemleri**  
\- \`books\`, \`students\` ve \`loans\` için \`GET\`, \`POST\`, \`PUT\`, \`DELETE\`, \`PATCH\` endpointleri eksiksiz tanımlanmıştır.  
\- Özellikle \`PATCH /loans/{id}/return\` ile kitap iade işlemi yapılabilir.

**🧩 Kullanılan OpenAPI Bileşenleri**  
\- \`components/schemas\` altında her varlık için detaylı veri modeli tanımlanmıştır.  
\- \`parameters\` ile hem \`path\` hem \`query\` parametreleri kullanılmıştır (\`id\`, \`page\`, \`size\` gibi).  
\- \`requestBody\` kullanımı ile \`POST\` ve \`PUT\` işlemleri sağlanmıştır.  
\- \`responses\` alanında \`200\`, \`201\`, \`204\`, \`400\`, \`404\` durumları örneklenmiştir.  
**📖 Ek Özellikler**  
\- \`GET /books\` endpointinde sayfalama parametreleri (\`page\`, \`size\`) tanımlanmıştır.  
\- Tüm endpointlerde \`summary\` ve \`tags\` alanları kullanılmıştır.  
\- Swagger Editor ile manuel olarak test edilmiştir ve geçerli yapıdadır.

---

## 🧪 **Test Notları (Opsiyonel)**

Swagger Editor üzerinden test ettiğiniz örnek istek/yanıtları özetleyebilirsiniz:

\- GET /books → Tüm kitaplar JSON listesi olarak döner.  
\- POST /students → Gönderilen örnek \`Student\` verisi ile öğrenci eklenir.  
\- PATCH /loans/{id}/return → İlgili ödünç işlemine "iade edildi" olarak işaretleme yapılır.  
