![image](https://github.com/user-attachments/assets/b8851185-169c-4de2-a30d-20200f4607fc)# Laravel Zamanlanmış Görevleri Windows'ta Çalıştırma

Laravel belgeleri, zamanlanmış görevlerin Linux sistemlerinde cron işleri kullanılarak nasıl çalıştırılacağını açıklar. Ancak, Windows'ta cron işleri mevcut değildir. Bunun yerine, Windows Görev Zamanlayıcı'yı kullanarak zamanlanmış görevleri çalıştırabilirsiniz.

## Bir Görev Oluşturma

1. **Windost Başlattan Görev Zamanlayıcı'yı Açın**
2. **Yeni Görev Oluşturun**
   - `Görev Oluştur...` seçeneğine tıklayın.
   - Göreve bir isim ve açıklama verin.
   - Görevi arka planda çalıştırmak için `Kullanıcı oturum açmış olmasa da çalıştır` seçeneğini seçin ve `Gizli` onay kutusunu işaretleyin.
  
   - ![image](https://github.com/user-attachments/assets/8509f0c1-5555-4103-9074-13b880c976a9)

3. **Tetikleyiciler**
   - Yeni bir tetikleyici oluşturun.
   - Tetikleyiciyi `Günlük` olarak ayarlayın ve her 1 gün tekrarlamasını seçin.
   - `Görevi tekrar et` seçeneğini 1 dakika olarak ayarlayın. 1 dakika seçeneği mevcut değilse, 5 dakikayı seçin ve ardından manuel olarak 1 dakika olarak değiştirin.
   - `Süre` olarak `Sonsuza kadar` seçeneğini ayarlayın.
   - `Etkin` olduğundan emin olun.

4. **Eylemler**
   - Yeni bir eylem oluşturun.
   - `Başlat` olarak PHP'nin binary yolunu girin, örneğin: `C:\php\php.exe`
   - `Argümanlar Ekle` alanına `C:\{proje-dizini}\artisan schedule:run` yazın (burada `{proje-dizini}` uygun yol ile değiştirin).

5. **Ayarlar**
   - `Görevi talep üzerine çalıştır` seçeneğini işaretleyin.
   - `Planlanan bir başlangıç sonrası görevi mümkün olan en kısa sürede çalıştır` seçeneğini işaretleyin.

## Tamamlama

- Görevinizin çalıştığından emin olmak için Görev Zamanlayıcı Kütüphanesi'nde görevi bulun.
- Görev Durumu'nu not edin. Bu `Hazır` veya `Çalışıyor` olabilir.
- `Sonraki Çalışma Zamanı` ve `Son Çalışma Zamanı` özelliklerini kontrol edin.
