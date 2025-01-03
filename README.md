[https://www.kaggle.com/code/mehmetgktugke/nlp-haber-anal-z](https://www.kaggle.com/code/mehmetgktugke/nlp-haber-anal-z)

# Afyon Kocatepe Üniversitesi  
## Mühendislik Fakültesi | Bilgisayar Mühendisliği  

---

## 📘 SD433 Doğal Dil İşleme  
Bu proje, **SD433 Doğal Dil İşleme** dersi kapsamında hazırlanmıştır. Projenin temel referansı, **Doğal Dil İşleme Proje Rapor Dosyası**dır.

### 💻 Teknoloji  
- **Programlama Dili:** Python

---

### ✍️ Hazırlayan  
- **Ad-Soyad:** Mehmet Göktuğ Gökçe  
- **Öğrenci No:** 212923025  

# 📚 Anlamsal Benzerliğe Duyarlı Arama Motoru Projesi

## 🌍 Proje Konusu
Bu proje, kullanıcı tarafından girilen bir metni, veri tabanında bulunan haber kaynaklarıyla **anlamsal bağlamı dikkate alarak** eşleştirip, arama işlemi gerçekleştirmeyi amaçlamaktadır. Kullanıcı, belirli bir konu hakkında bilgi ararken, arama motoru sadece kelime eşleşmesine dayalı değil, **anlam temelli** bir sıralama sunacaktır. Ayrıca, belirli tarih aralıklarında en fazla hangi konu başlıklarında haber üretildiği analiz edilerek, haberlerin **kategorize edilmesi** sağlanacaktır. 

Veri seti üzerinde yapılacak bu analiz, haberlerin **tarihsel eğilimlerini** ve hangi konuların daha fazla ilgi gördüğünü gösterecektir.

## 🎯 Proje Amacı
Günümüzde haber siteleri sayısız haber metniyle doludur. Bu projedeki amaç, kullanıcıların bu kadar büyük bir bilgi yığınından **en alakalı ve anlamlı** olanları hızlı ve doğru bir şekilde bulabilmelerini sağlamaktır. Projenin temel hedefi, **anlamsal benzerliğe dayalı bir arama motoru** sunarak, haber içeriklerini en doğru biçimde **sıralamak ve sunmak** olacaktır.

Sunulacak projenin, akademik bir katkı sağlayacağı düşünülmektedir.

## 🗂️ Kullanılacak Veri Seti
**Adı:** Turkish News Article  
**İçeriği:** Bu veri seti, **Türkçe haber kaynakları** içeren 204 yazardan ve 2415 makaleden oluşmaktadır. Veri seti, haberin **tarihi ve bağlantı adreslerini** içermektedir. Haberler farklı kategorilere dağılmakta ve **zengin bir içerik** sunmaktadır, bu da projede kullanılacak olan analizlerin çeşitliliğini artırmaktadır.

## 🔧 Kullanılacak Yöntemler

### 1) 🧹 Veri Ön İşleme
Veri setindeki gereksiz karakterler, semboller, sayılar ve boşluklar temizlenecektir. Metinler küçük harfe dönüştürülerek tutarsızlıklar giderilecektir. Bu adım, verilerin daha düzenli ve işlemeye uygun hale gelmesini sağlayacaktır. Böylece, doğru analiz sonuçlarına ulaşmak daha kolay olacaktır. 

### 2) 🔤 Word2Vec ile Metin Vektörleştirme
Kullanıcı sorgusu ve haber metinleri, **Word2Vec** algoritması kullanılarak anlam temelli vektörlere dönüştürülecektir. Bu dönüşüm, kelimelerin anlamsal benzerliklerini daha iyi temsil etmeye olanak sağlar. **Word2Vec**, kelimeler arasındaki anlam ilişkilerini öğrenerek, vektörler üzerinden daha doğru eşleşmeler yapmamıza olanak verir. 📊

### 3) 🔍 Kosinüs Benzerliği ile Anlamsal Yakınlık Ölçümü
Word2Vec ile elde edilen vektörler arasında **kosinüs benzerliği** hesaplanacaktır. Bu yöntem, vektörler arasındaki açıyı dikkate alarak, iki metin arasındaki anlamsal benzerliği ölçer. Kosinüs benzerliği kullanılarak, kullanıcı sorgusu ve haber metinleri arasındaki **anlam benzerliği** değerlendirilecektir. Bu sayede, anlam bakımından **en yakın** sonuçlar daha yüksek sıralarda yer alacaktır. 💡

### 4) 📊 TF-IDF ile Sonuç Sıralama
Arama sonuçları, kelime frekansı ve kelimelerin **önemine** göre sıralanması düşünülmüştür. **TF-IDF (Term Frequency-Inverse Document Frequency)**, her kelimenin ne kadar önemli olduğunu ve belgedeki **eşsizliğini** dikkate alır. Bu yöntem, kullanıcıya en alakalı sonuçların en üstte **listelenmesini** sağlar. Bu adım, arama sonuçlarının doğruluğunu artırarak kullanıcı deneyimini iyileştirir.

### 5) 🧠 LDA (Latent Dirichlet Allocation) ile Konu Modelleme
Veri setindeki haberler, belirli tarih aralıklarında hangi konu başlıklarının daha fazla üretildiğini analiz etmek amacıyla **LDA** (Latent Dirichlet Allocation) modeline tabi tutulacaktır. Bu model, haberleri **konu başlıkları** altında gruplayarak, haber üretim eğilimlerini gözler önüne serecektir. LDA ile, hem geçmiş dönemde popüler olan konular hem de **güncel eğilimler** hakkında bilgi edinilecektir. 📅

# 📚 **Kullanılan Kütüphaneler**  

Proje kapsamında aşağıdaki kütüphaneler kullanılmıştır:

- **pandas (pd):** Veri manipülasyonu ve analizinde kullanılır. Veri çerçeveleri (DataFrame) ile işlem yapmayı sağlar.  
- **numpy (np):** Sayısal hesaplamalar ve veri işleme için kullanılır.  
- **re:** Düzenli ifadelerle metin işleme ve temizleme işlemleri için kullanılır.  
- **gensim.models.Word2Vec:** Metin verilerinde kelime gömme (word embedding) işlemleri için kullanılır.  
- **sklearn.metrics.pairwise.cosine_similarity:** Kosinüs benzerliği hesaplamak için kullanılır.  
- **sklearn.feature_extraction.text.TfidfVectorizer:** Metin verilerinin TF-IDF (Term Frequency-Inverse Document Frequency) vektörlerine dönüştürülmesi için kullanılır.  
- **sklearn.decomposition.LatentDirichletAllocation:** Latent Dirichlet Allocation (LDA) ile konu modellemesi yapılmasını sağlar.  
- **sklearn.feature_extraction.text.CountVectorizer:** Kelime sayımlarını (bag of words) çıkaran bir vektörleştirici kullanılır.  
- **matplotlib.pyplot (plt):** Veri görselleştirmeleri yapmak için kullanılır.  
- **collections.Counter:** Veri kümelerindeki öğelerin sıklığını saymak için kullanılır.  
