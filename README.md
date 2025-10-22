# barbot
ne içsek ya
🍸 Kokteyl Tarif Chatbot'u (RAG Destekli)
Projenin Amacı
Bu projenin temel amacı, geniş bir kokteyl tarifi veri setini kullanarak kullanıcılara hızlı, doğru ve tamamen Türkçe kokteyl tarifleri sunan bir GenAI chatbot geliştirmektir.

Proje, geleneksel veritabanı sorgulama yeteneğini (Retrieval - Geri Çekme) gelişmiş bir Büyük Dil Modeli (LLM) olan Gemini API'nin üretim yeteneği (Generation - Üretim) ile birleştirerek bir RAG (Retrieval Augmented Generation) mimarisini temel alır.


Temel Kabiliyetler:

Kullanıcının girdiği bir veya birden fazla malzemeye göre ilgili tarifi bulur.
Bulunan tarifin tüm detaylarını (talimatlar, malzemeler, kategoriler) anlık olarak Türkçe'ye çevirir.
Tarifin görselini web arayüzünde görüntüler.
Google Colab ortamında gerçekleştirilmiştir.

Veri Seti Hakkında Bilgi
Bu projede, halka açık ve kapsamlı bir kokteyl veri seti (final_cocktails.csv) kullanılmıştır.

İçerik, Kokteyl adı, alkollü durumu, kategorisi, kullanılan malzemeler, ölçüleri, talimatları ve görsel URL'si gibi alanları içerir.
Hazırlanış, Veri seti hazır olarak temin edilmiştir. Proje kapsamında, arama işlemlerini hızlandırmak için ingredients sütunu küçük harfe çevrilerek temizlenmiştir.
Kullanım,Pandas DataFrame olarak yüklenir ve RAG'ın Retrieval  aşamasında bir Knowledge Base olarak kullanılır.

Elde Edilen Sonuçlar
Dinamik Türkçe Çıktı: Gemini API sayesinde, veri setinde İngilizce olan tüm bilgiler (malzeme adları, talimatlar, kategoriler) başarılı bir şekilde Türkçe'ye çevrilerek sunulmuştur.
Esnek Arama: Kullanıcılar, Vodka, Lime, Mint gibi virgülle ayrılmış birden fazla malzemeyi arayabilir ve bu malzemelerden en az birini içeren uygun bir tarif alabilirler.

# 🍸 B-A-R*BOT: Yapay Zeka Destekli Kokteyl Tarif Chatbot'u

B-A-R*BOT, elinizdeki malzemelere göre anında kokteyl tarifleri bulmanızı sağlayan yapay zeka destekli bir Gradio uygulamasıdır. Kullanıcılar, birden fazla malzemeyi Türkçe veya İngilizce olarak girebilirler. Sistem, girdiğiniz malzemeleri içeren en uygun tarifi bulur, tüm detayları Türkçe'ye çevirir ve Gemini API'si sayesinde tarife uygun bir görsel sunar (veya oluşturur).

## 🚀 Özellikler

* **Akıllı ve Esnek Arama:**
    * Tek malzeme aramasında esnektir (örn: "Çikolata" ile "Çikolata Likörü"nü bulur).
    * Birden fazla malzeme aramasında hassastır (girdiğiniz tüm malzemelerin olmasını zorunlu kılar).
* **Çok Dilli Giriş:** Türkçe (örn: "Viski, Limon") veya İngilizce malzeme girişini destekler.
* **Tam Türkçe Çıktı:** Kokteyl adı, kategorisi, malzemeleri, ölçüleri ve **yapılış talimatları** dahil tüm çıktıları profesyonel bir dille Türkçe'ye çevirir.
* **Görsel Desteği:** Veri setindeki görseli gösterir; görsel yoksa veya API etkinse Gemini'nin Imagen modelini kullanarak tarife özel bir görsel oluşturur.

WEB SİTESİ LİNKİ:

(https://2a83995eef06a1adfd.gradio.live/)

<img width="1918" height="901" alt="image" src="https://github.com/user-attachments/assets/fddec34c-9df4-4011-866d-5093929ec1d7" />
<img width="1918" height="896" alt="image" src="https://github.com/user-attachments/assets/dbd42c67-3443-4228-8876-ca6fc3245c0a" />

## ⚙️ Gereksinimler

Bu projeyi yerel olarak veya Google Colab'de çalıştırmak için aşağıdaki kütüphanelere ve API anahtarına ihtiyacınız vardır.

### Kütüphane Gereksinimleri

Gerekli tüm kütüphaneler `requirements.txt` dosyasında listelenmiştir.

```bash
pip install -r requirements.txt
API Anahtarı Gereksinimi (Zorunlu)
Uygulamanın çeviri ve görsel oluşturma (Gemini/Imagen) özelliklerini kullanabilmesi için bir Google Gemini API anahtarı gereklidir.

Google AI Studio adresinden bir API anahtarı alın.

Anahtarınızı ayarlama adımlarını takip edin.

💻 Kurulum ve Çalıştırma Adımları
1. Dosyaları Hazırlama
Ana Python kodunuzu (chatbot.py veya barbot.ipynb), requirements.txt dosyasını ve bu README.md dosyasını tek bir klasöre taşıyın.

Veri Seti: final_cocktails.csv adlı veri setinizin de aynı klasörde veya Colab çalışma dizininde olduğundan emin olun.

2. Kütüphaneleri Kurma
Terminali açın ve projenizin olduğu klasöre gidin. Gerekli kütüphaneleri yükleyin:

Bash

pip install -r requirements.txt
3. API Anahtarını Ayarlama (Çok Önemli!)
API anahtarınızı projeye tanıtmak için en kesin yöntem, doğrudan kodu düzenlemektir.

chatbot.py (veya kullandığınız ana kod dosyası) dosyasını açın.

1. VERİ YÜKLEME VE API İSTEMCİSİ AYARLARI bölümünde bulunan aşağıdaki satırı bulun ve kendi anahtarınızla değiştirin:

Python

API_KEY_SABİT = 'SİZİN_API_ANAHTARINIZI_BURAYA_YAZIN' # <-- Anahtarınızı buraya yapıştırın
4. Uygulamayı Başlatma
Terminalde veya Colab hücresinde ana Python dosyanızı çalıştırın:

Bash

python chatbot.py 
# veya Colab'de iseniz, tüm hücreleri çalıştırın
Uygulama, Gradio arayüzünü başlatacak ve size bir URL verecektir (örneğin: https://...gradio.live).



