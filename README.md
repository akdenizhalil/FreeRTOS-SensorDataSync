# FreeRTOS-SensorDataSync

**FreeRTOS-SensorDataSync**, FreeRTOS üzerinde sensör verilerinin toplanması ve işlenmesini gösteren bir örnek projedir.  
Bu projede:
- **Mutex** kullanılarak sensöre eşzamanlı erişim engellenir.  
- **Counting Semaphore** ile alınan veriler işlenmek üzere sıraya alınır.  
- **UART (HAL kütüphaneleri)** üzerinden debug ve bilgilendirme mesajları gönderilir.

## Özellikler
- Sensör verisi alma (simülasyon).
- Verileri işleme (temel olarak ekrana/loga yazdırma).
- FreeRTOS görevleri arasında senkronizasyon ve karşılıklı dışlama.

## Nasıl Çalışır?
1. **Sensor Acquisition Task:** Sensör verisini okur (rastgele sıcaklık değerleriyle simüle edilir) ve verinin hazır olduğunu semaphore ile bildirir.
2. **Sensor Processing Task:** Semafor üzerinden yeni verinin geldiğini anlar ve işleme fonksiyonunu çağırır.

## Gereksinimler
- STM32 HAL kütüphaneleri (UART2 konfigürasyonu).
- FreeRTOS çekirdeği.
- STM32CubeIDE veya benzeri bir geliştirme ortamı.

## Kurulum ve Kullanım
1. Projeyi klonlayın veya indirin.
2. STM32CubeIDE ile açıp, kendi kartınıza göre UART vb. ayarları güncelleyin.
3. Derleyip kartınıza yükleyin.
4. UART üzerinden sensör veri mesajlarını gözlemleyebilirsiniz.


