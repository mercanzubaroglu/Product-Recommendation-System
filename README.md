# 🛍️ Product Recommendation System  
### Ürün Tavsiye Sistemi

This project builds a **content-based product recommendation system** using the [Amazon Fine Food Reviews dataset](https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews).  
Bu proje, [Amazon Fine Food Reviews veri seti](https://www.kaggle.com/datasets/snap/amazon-fine-food-reviews) kullanılarak oluşturulmuş **içerik tabanlı bir ürün tavsiye sistemi**dir.

The goal is to recommend similar products based on review summaries using natural language processing and cosine similarity.  
Amaç, ürün yorum özetlerini kullanarak benzer ürünleri doğal dil işleme ve kosinüs benzerliği yöntemiyle önermektir.

---

## 🔍 Project Description  
### Proje Açıklaması

### 1. Data Preparation | Veri Hazırlığı  
- The dataset is filtered to include `ProductId`, `UserId`, `ProfileName`, `Score`, and `Summary`.  
- Veri seti `ProductId`, `UserId`, `ProfileName`, `Score` ve `Summary` sütunlarıyla sınırlanmıştır.  
- Null veya eksik değerler temizlenmiştir.  

### 2. Text Vectorization with TF-IDF | TF-IDF ile Metin Vektörleştirme  
- The `Summary` (short review title) is used as the product content.  
- `Summary` sütunu (kısa yorum başlığı) ürünün metinsel içeriği olarak kullanılmıştır.  
- A TF-IDF vectorizer converts these summaries into numerical form.  
- TF-IDF yöntemiyle bu özetler sayısal vektörlere dönüştürülmüştür.

### 3. Cosine Similarity Calculation | Kosinüs Benzerliği Hesaplama  
- Cosine similarity is used to measure the similarity between product vectors.  
- Ürün vektörleri arasındaki benzerlik **cosine similarity** ile hesaplanmıştır.

### 4. Recommendation Function | Tavsiye Fonksiyonu  
- A function `recommend_product(product_name)` returns the top 10 similar products.  
- `recommend_product(product_name)` fonksiyonu, girilen ürüne en çok benzeyen 10 ürünü listeler.  
- Results are based entirely on product summaries.  
- Sonuçlar yalnızca `Summary` alanına göre oluşturulur.

---

## 🧠 Key Concepts  
### Temel Kavramlar

- **TF-IDF Vectorization**: Represents text by importance of words across documents.  
  **TF-IDF Vektörleştirme**: Kelimelerin önemine göre metinleri sayısallaştırır.

- **Cosine Similarity**: Measures how similar two vectors are.  
  **Kosinüs Benzerliği**: İki vektörün benzerliğini ölçen matematiksel yöntemdir.

- **Content-Based Filtering**: Recommends items based on their metadata or content.  
  **İçerik Tabanlı Filtreleme**: Ürünlerin içerik bilgilerine göre öneri yapar.

---

## 📌 Notes  
### Notlar

- Only the `Summary` field is used for recommendations.  
- Öneriler yalnızca `Summary` (yorum özeti) alanına dayanmaktadır.

- No user preferences or scores are used in the recommendation logic.  
- Tavsiye algoritmasında kullanıcı davranışı veya puanlar kullanılmamıştır.

- The system is interpretable, lightweight, and a good foundation for further improvement.  
- Sistem yorumlanabilir, hafif yapılı ve geliştirilmeye uygundur.

---

