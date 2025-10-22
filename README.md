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

Geliştirme süreci Python dilinde ve Google Colab ortamında gerçekleştirilmiştir.

Veri Seti Hakkında Bilgi
Bu projede, halka açık ve kapsamlı bir kokteyl veri seti (final_cocktails.csv) kullanılmıştır.

İçerik, Kokteyl adı, alkollü durumu, kategorisi, kullanılan malzemeler, ölçüleri, talimatları ve görsel URL'si gibi alanları içerir.
Hazırlanış, Veri seti hazır olarak temin edilmiştir. Proje kapsamında, arama işlemlerini hızlandırmak için ingredients sütunu küçük harfe çevrilerek temizlenmiştir.
Kullanım,Pandas DataFrame olarak yüklenir ve RAG'ın Retrieval  aşamasında bir Knowledge Base olarak kullanılır.

Elde Edilen Sonuçlar

Dinamik Türkçe Çıktı: Gemini API sayesinde, veri setinde İngilizce olan tüm bilgiler (malzeme adları, talimatlar, kategoriler) başarılı bir şekilde Türkçe'ye çevrilerek sunulmuştur.
Esnek Arama: Kullanıcılar, Vodka, Lime, Mint gibi virgülle ayrılmış birden fazla malzemeyi arayabilir ve bu malzemelerden en az birini içeren uygun bir tarif alabilirler.
Geliştirilmiş Kullanıcı Deneyimi: Gradio arayüzü, metin çıktısı ve görsel çıktıyı düzenli bir şekilde yan yana göstererek okunabilirlik sorununu gidermiştir.
WEB SİTESİ LİNKİ:

https://1d97d9f3ea96ec3969.gradio.live/

<img width="1918" height="901" alt="image" src="https://github.com/user-attachments/assets/fddec34c-9df4-4011-866d-5093929ec1d7" />
<img width="1918" height="896" alt="image" src="https://github.com/user-attachments/assets/dbd42c67-3443-4228-8876-ca6fc3245c0a" />


