# n8n İş Akışı Projeleri

Bu klasör, farklı görevleri otomatikleştiren n8n iş akışlarının JSON dışa aktarımlarını içerir. Her proje kendi klasöründedir.

## Projeler

### Ders Asistan Sohbet Botu

[İş akışı JSON'u](./ders-asistan-sohbet-botu/Ders%20Asistan%20Sohbet%20Botu.json)

PDF ders notlarını bir form üzerinden alır, metne dönüştürür ve bellekteki vektör deposuna ekler. Sohbet botu, soruları bu notlara dayanarak yanıtlar; notlarda bulunmayan konularda tahmin yürütmemesi için yapılandırılmıştır. Gemini gömmeleri, Groq sohbet modeli ve konuşma belleği kullanır.

### Haftalık Haber Bülteni

[İş akışı JSON'u](./haftalık-haber-bülteni/Haftalık%20Haber%20Bülteni.json)

Zamanlanmış tetikleyiciyle RSS kaynağından haberleri alır, haberleri bir araya getirir ve yapay zekâ ile bülten içeriği oluşturur. Sonuç Gmail üzerinden gönderilir.

### Müşteri Yorum Sınıflandırma

[İş akışı JSON'u](./müsteri-yorum-siniflandirma/Müşteri%20Yorum%20Sınıflandırma.json)

Google Sheets'teki yorumları izler, yorumları sınıflandırır ve sınıflandırma sonucunu tabloya yazar. Yapılandırılmış koşula bağlı olarak e-posta da gönderir.

### Sosyal Medya İçerik Üretimi

[İş akışı JSON'u](./sosyal-medya-içerik-yonetim/Sosyal%20Medya%20İçerik%20Üretimi.json)

Zamanlanmış akışta Telegram üzerinden konu/yanıt alır, Perplexity ile araştırma yapar ve Gemini ile LinkedIn paylaşım taslağı oluşturur. Taslak Telegram üzerinden onaya sunulur; onaylanırsa LinkedIn API'sine gönderilir.

### Toplantı Notu Görev Listesi

[İş akışı JSON'u](./toplanti-notu-gorev-listesi/Toplantı%20Notu%20Görev%20Listesi.json)

Toplantı notlarını PDF olarak alır ve metne dönüştürür. Google Sheets'teki mevcut bilgilerle birlikte Gemini kullanarak görevleri yapılandırılmış biçimde çıkarır; görevler Trello kartlarına dönüştürülür ve ilgili akış e-posta bildirimi gönderir.

## Kurulum ve paylaşım notları

- JSON dosyalarını n8n'e içe aktarın; gerekli Google Gemini, Groq, Gmail, Google Sheets, Perplexity, Telegram, LinkedIn ve Trello kimlik bilgilerini kendi hesabınızla yeniden bağlayın.
- Paylaşım için hassas kaynak kimlikleri ve kimlik bilgisi referansları maskelenmiştir. Google Sheets, Telegram ve Trello alanlarını kendi kaynaklarınızla güncelleyin.
- Haftalık Haber Bülteni'ndeki RSS adresi örnek bir adresle değiştirilmiştir; akışı çalıştırmadan önce gerçek RSS adresinizi girin.
- Ders Asistan Sohbet Botu ve Toplantı Notu Görev Listesi PDF yükleme formları kullanır. Akışları etkinleştirmeden önce n8n'de formları ve tetikleyicileri yapılandırıp test edin.
