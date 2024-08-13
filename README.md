# Laravel Zamanlanmış Görevleri Windows'ta Çalıştırma

Laravel belgeleri, zamanlanmış görevlerin Linux sistemlerinde cron işleri kullanılarak nasıl çalıştırılacağını açıklar. Ancak, Windows'ta cron işleri mevcut değildir. Bunun yerine, Windows Görev Zamanlayıcı'yı kullanarak zamanlanmış görevleri çalıştırabilirsiniz.

## Bir Görev Oluşturma

1. **Windost Başlattan Görev Zamanlayıcı'yı Açın**
2. **Yeni Görev Oluşturun**
   - `Görev Oluştur...` seçeneğine tıklayın.
   - Göreve bir isim ve açıklama verin.
   - Görevi arka planda çalıştırmak için `Kullanıcı oturum açmış olmasa da çalıştır` seçeneğini seçin ve `Gizli` onay kutusunu işaretleyin.

   - ![image](https://github.com/user-attachments/assets/c8da5451-98de-4971-9d6e-3b272da14862)

   - ![image](https://github.com/user-attachments/assets/abc4658d-98b3-4505-aadc-b533b1c0ba93)

3. **Tetikleyiciler**
   - Yeni bir tetikleyici oluşturun.
   - Tetikleyiciyi `Günlük` olarak ayarlayın ve her 1 gün tekrarlamasını seçin.
   - `Görevi tekrar et` seçeneğini 1 dakika olarak ayarlayın. 1 dakika seçeneği mevcut değilse, 5 dakikayı seçin ve ardından manuel olarak 1 dakika olarak değiştirin.
   - `Süre` olarak `Sonsuza kadar` seçeneğini ayarlayın.
   - `Etkin` olduğundan emin olun.
  
   - ![image](https://github.com/user-attachments/assets/26841a67-76e3-4bb7-903a-7047930987b6)


4. **Eylemler**
   - Yeni bir eylem oluşturun.
   - `Başlat` olarak PHP'nin binary yolunu girin, örneğin: `C:\php\php.exe`
   - `Argümanlar Ekle` alanına `C:\{proje-dizini}\artisan schedule:run` yazın (burada `{proje-dizini}` uygun yol ile değiştirin).
  
   - ![image](https://github.com/user-attachments/assets/c2461b7b-d161-4ab0-9ebc-098f6aca6db4)


5. **Ayarlar**
   - `Görevi talep üzerine çalıştır` seçeneğini işaretleyin.
   - `Planlanan bir başlangıç sonrası görevi mümkün olan en kısa sürede çalıştır` seçeneğini işaretleyin.
  
   - ![image](https://github.com/user-attachments/assets/aba532e4-0856-4ac4-8cb0-7b4d541732aa)



## Tamamlama

- Görevinizin çalıştığından emin olmak için Görev Zamanlayıcı Kütüphanesi'nde görevi bulun.
- Görev Durumu'nu not edin. Bu `Hazır` veya `Çalışıyor` olabilir.
- `Sonraki Çalışma Zamanı` ve `Son Çalışma Zamanı` özelliklerini kontrol edin.

- ![image](https://github.com/user-attachments/assets/4cb62ae8-e830-483c-a5ca-2507159a0a39)

