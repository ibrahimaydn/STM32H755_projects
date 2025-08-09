# STM32H755 Çift Çekirdekli Eğitim Serisi 🚀

Bu depo, **STM32H755 NUCLEO-H755ZI-Q** geliştirme kartı ile gömülü yazılım öğrenmek isteyenler için hazırlanmış **30 adımlık kapsamlı bir eğitim serisini** içerir.  
**STM32H755**, **çift çekirdekli** bir mikrodenetleyicidir:
- **Cortex-M7 @ 480 MHz** → Yüksek performans, karmaşık işlemler
- **Cortex-M4 @ 240 MHz** → Düşük güç tüketimi, yardımcı görevler

Bu eğitim setinde:
- İlk projeler **M7 çekirdeği** üzerinde çalışır (temel öğrenme)
- Son projelerde **her iki çekirdek** birlikte kullanılır (**Inter-Processor Communication Controller - IPCC** ile veri paylaşımı)

---

## 📌 Gereksinimler
- STM32H755 NUCLEO-H755ZI-Q kartı
- STM32CubeIDE ve STM32CubeMX
- USB Type-A → Micro-B kablo
- Temel elektronik bileşenler (LED, direnç, buton, potansiyometre vb.)
- Geliştirme için bilgisayar

---

## 📚 Proje Listesi (Çekirdek Bilgisi ile)

### **Temel Başlangıç (Tek Çekirdek - M7)**
1. **01_Basic_Blink** → Dahili LED yakma (**M7**)
2. **02_Button_Control** → Buton ile LED kontrolü (**M7**)
3. **03_External_LED_Blink** → Harici LED yakma (**M7**)
4. **04_Buzzer_Output** → Buzzer ile ses çıkarma (**M7**)
5. **05_Debounce_Button** → Buton debounce yazılım tekniği (**M7**)

### **ADC (Analog - Dijital Dönüşüm)**
6. **06_ADC_Potentiometer** → Potansiyometre okuma (**M7**)
7. **07_ADC_Multiple_Channels** → Birden fazla ADC kanalı okuma (**M7**)
8. **08_ADC_Temperature_Sensor** → Dahili sıcaklık sensörü okuma (**M7**)
9. **09_ADC_DMA** → DMA ile ADC verisi okuma (**M7**)
10. **10_ADC_LightSensor** → LDR ile ışık ölçümü (**M7**)

### **Dijital Haberleşme**
11. **11_UART_Communication** → UART ile veri gönderme/alma (**M7**)
12. **12_USART_PC_Communication** → Bilgisayar ile USART haberleşme (**M7**)
13. **13_I2C_LCD** → I2C ile LCD ekran kullanımı (**M7**)
14. **14_SPI_OLED** → SPI ile OLED ekran kontrolü (**M7**)
15. **15_I2C_MPU6050** → MPU6050 sensöründen veri okuma (**M7**)

### **PWM ve Motor Kontrol**
16. **16_PWM_LED_Dimming** → PWM ile LED parlaklık kontrolü (**M7**)
17. **17_PWM_Servo** → Servo motor kontrolü (**M7**)
18. **18_DC_Motor_Driver** → L298N ile DC motor sürme (**M7**)
19. **19_Stepper_Motor** → Step motor kontrolü (**M7**)
20. **20_Brushless_ESC** → ESC ile fırçasız motor sürme (**M7**)

### **Kesme ve Zamanlayıcılar**
21. **21_Timer_Interrupt_LED** → Timer kesmesi ile LED blink (**M7**)
22. **22_EXTI_Button** → Harici kesme ile buton kontrolü (**M7**)
23. **23_Timer_Input_Capture** → PWM sinyal frekans ölçümü (**M7**)
24. **24_RTC_Clock** → RTC ile saat-tarih uygulaması (**M7**)
25. **25_Watchdog_Timer** → Watchdog ile sistem resetleme (**M7**)

### **Çift Çekirdekli ve Gelişmiş Projeler**
26. **26_FreeRTOS_Basics** → FreeRTOS ile temel task kullanımı (**M7**)
27. **27_M7M4_LED_UART** → **M7** LED kontrol, **M4** UART haberleşme (**M7 + M4**)
28. **28_M7M4_SensorProcessing** → **M4** sensör verisi toplar, **M7** işler ve ekrana yazar (**M7 + M4**)
29. **29_Ethernet_WebServer** → Ethernet web sunucusu (**M7**) + arka plan veri toplama (**M4**) (**M7 + M4**)
30. **30_Firmware_Update_OTA** → **M7** ana yazılım, **M4** güncelleme yönetimi (**M7 + M4**)

---

## 🛠 Kurulum
1. Depoyu klonlayın:
   ```bash
   git clone https://github.com/kullaniciadi/STM32H755-Tutorials.git
