# 🚀 STM32H755 Çift Çekirdekli Eğitim Serisi

Bu depo, **STM32H755 NUCLEO-H755ZI-Q** geliştirme kartı ile **çift çekirdekli gömülü sistem geliştirmeyi öğrenmek isteyenler** için hazırlanmış **53 adımlık kapsamlı bir eğitim setini** içerir.  

📌 **Amacımız:**  
STM32H755 ve çift çekirdekli ARM tabanlı mikrodenetleyiciler konusunda **internetteki bilgi eksikliğini gidermek**, anlaşılır ve Türkçe bir kaynak sunmak.

---

## 📦 STM32H755 NUCLEO-H755ZI-Q Teknik Özellikler

**🔹 Mikrodenetleyici:**
- **Model:** STM32H755ZIQ
- **Çekirdek Yapısı:**
  - **Cortex-M7 @ 480 MHz** → Yüksek performans, karmaşık işlem ve hesaplamalar
  - **Cortex-M4 @ 240 MHz** → Düşük güç tüketimi, yardımcı görevler
- **Bellek:**
  - 2 MB Flash (çekirdekler arası paylaştırılabilir)
  - 1 MB SRAM (ITCM, DTCM ve AXI bölgelerine ayrılmış)
- **FPU:** Tek/çift hassasiyetli kayan nokta desteği (her iki çekirdekte)
- **DMA:** 16 kanal

**🔹 Bağlantı Arayüzleri:**
- Ethernet MAC (RMII/MII)
- USB OTG FS/HS
- 10x USART/UART
- 6x SPI / I²S
- 4x I²C
- 3x CAN FD
- SDMMC (SD kart desteği)

**🔹 Giriş/Çıkış:**
- 144 pin LQFP paket
- 5V toleranslı bazı GPIO’lar
- Harici saat kaynağı desteği

**🔹 Diğer Özellikler:**
- **IPCC** → Çift çekirdek arası iletişim
- TrustZone-M, Secure Boot
- Düşük güç modları
- RTC, Watchdog, Timer

**🔹 NUCLEO-H755ZI-Q Kart:**
- Dahili **ST-LINK/V3E** programlayıcı
- USB Type-B bağlantı
- Arduino UNO V3 ve ST morpho header pinleri
- Dahili LED, buton, reset
- Ethernet RJ45 konnektörü 

---

## 📚 Eğitim Seti Hakkında
Bu eğitim seti temelden ileri seviyeye adım adım ilerler:

- İlk projeler M7 çekirdeği üzerinde basit uygulamalar  
- Orta seviyede ADC, PWM, haberleşme protokolleri  
- İleri seviyede M7 + M4 birlikte çalışan çift çekirdekli projeler  
- Gerçek zamanlı işletim sistemi (FreeRTOS) örnekleri  
- Ethernet ve OTA (Over-The-Air) güncelleme projeleri  
- Gerçek hayat IoT uygulama projeleri  

📌 Tüm örnekler STM32CubeIDE ve STM32CubeMX üzerinde hazırlanmıştır.  
Her proje detaylı açıklama ve donanım bağlantı şeması içerir.  

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

---

### **ADC (Analog - Dijital Dönüşüm)**
6. **06_ADC_Potentiometer** → Potansiyometre okuma (**M7**)  
7. **07_ADC_Multiple_Channels** → Birden fazla ADC kanalı okuma (**M7**)  
8. **08_ADC_Temperature_Sensor** → Dahili sıcaklık sensörü okuma (**M7**)  
9. **09_ADC_DMA** → DMA ile ADC verisi okuma (**M7**)  
10. **10_ADC_LightSensor** → LDR ile ışık ölçümü (**M7**)  
11. **11_ADC_Joystick** → Joystick X-Y eksen okuma (**M7**)  

---

### **Dijital Haberleşme (Tek Kart + PC)**
12. **12_UART_Communication** → UART ile veri gönderme/alma (**M7**)  
13. **13_USART_PC_Communication** → Bilgisayar ile USART haberleşme (**M7**)  
14. **14_USART_Interrupt_DMA** → USART’ı kesme + DMA ile kullanma (**M7**)  
15. **15_I2C_LCD** → I2C ile LCD ekran kullanımı (**M7**)  
16. **16_I2C_MPU6050** → MPU6050 sensöründen veri okuma (**M7**)  
17. **17_SPI_OLED** → SPI ile OLED ekran kontrolü (**M7**)  
18. **18_SPI_FlashMemory** → SPI tabanlı flash bellek okuma/yazma (**M7**)  
19. **19_CAN_Basics** → CAN Bus ile mesaj gönderme/alma (**M7**)  
20. **20_CAN_Filtering** → CAN Bus ID filtreleme (**M7**)  
21. **21_USB_VirtualComPort** → USB üzerinden sanal seri port haberleşme (**M7**)  

---

### **İki STM32 Arasında Haberleşme**
22. **22_UART_STM32toSTM32** → İki STM32 arasında UART ile haberleşme  
23. **23_USART_STM32toSTM32_DMA** → UART + DMA ile yüksek hızlı haberleşme  
24. **24_I2C_MasterSlave** → Bir STM32 Master, diğeri Slave olarak I2C haberleşmesi  
25. **25_SPI_MasterSlave** → SPI Master-Slave haberleşmesi  
26. **26_CAN_STM32Network** → 2 veya daha fazla STM32 ile CAN Bus ağı kurma  
27. **27_Ethernet_ClientServer** → İki STM32 arasında TCP/IP haberleşmesi (Ethernet)  
28. **28_IPCC_InterCore** → M7 ↔ M4 çekirdek arası IPCC ile veri paylaşımı  

---

### **PWM ve Motor Kontrol**
29. **29_PWM_LED_Dimming** → PWM ile LED parlaklık kontrolü (**M7**)  
30. **30_PWM_Servo** → Servo motor kontrolü (**M7**)  
31. **31_DC_Motor_Driver** → L298N ile DC motor sürme (**M7**)  
32. **32_Stepper_Motor** → Step motor kontrolü (**M7**)  
33. **33_Brushless_ESC** → ESC ile fırçasız motor sürme (**M7**)  

---

### **Kesme ve Zamanlayıcılar**
34. **34_Timer_Interrupt_LED** → Timer kesmesi ile LED blink (**M7**)  
35. **35_EXTI_Button** → Harici kesme ile buton kontrolü (**M7**)  
36. **36_Timer_Input_Capture** → PWM sinyal frekans ölçümü (**M7**)  
37. **37_RTC_Clock** → RTC ile saat-tarih uygulaması (**M7**)  
38. **38_Watchdog_Timer** → Watchdog ile sistem resetleme (**M7**)  

---

### **Gelişmiş Projeler ve Çift Çekirdek**
39. **39_FreeRTOS_Basics** → FreeRTOS ile temel task kullanımı (**M7**)  
40. **40_FreeRTOS_MultiTask** → FreeRTOS ile sensör + UART + LED task yönetimi  
41. **41_M7M4_LED_UART** → **M7** LED kontrol, **M4** UART haberleşme  
42. **42_M7M4_SensorProcessing** → **M4** sensör verisi toplar, **M7** işler ve ekrana yazar  
43. **43_M7M4_SharedMemory** → Paylaşımlı RAM üzerinden çekirdekler arası veri değişimi  
44. **44_M7M4_IPCC_DMA** → IPCC + DMA ile yüksek hızlı inter-core iletişim  
45. **45_Ethernet_WebServer** → Ethernet web sunucusu (**M7**) + arka plan veri toplama (**M4**)  
46. **46_MQTT_Client** → STM32’den MQTT broker’a veri gönderme (Ethernet/WiFi)  
47. **47_Firmware_Update_OTA** → **M7** ana yazılım, **M4** güncelleme yönetimi  
48. **48_SDCard_FATFS** → SD kart üzerinden dosya yazma/okuma (FatFS)  
49. **49_USB_HID_Device** → STM32’yi USB klavye/fare gibi göstermek  
50. **50_AI_TinyML** → STM32 üzerinde TensorFlow Lite ile küçük bir ML modeli çalıştırma  

---

### **Gerçek Hayat IoT Projeleri**
51. **51_MultiSensor_IoT_Node** → Çok sensörlü IoT düğümü (M4 sensör verisi toplar, M7 buluta gönderir)  
52. **52_DualCore_RobotControl** → Çift çekirdekli robot/drone mimarisi (M4 sensör + M7 motor/haberleşme)  
53. **53_Smart_Home_Gateway** → STM32 tabanlı akıllı ev IoT merkezi (Ethernet/WiFi + MQTT)  

---

## 🛠 Kurulum
1. Depoyu klonlayın:
   ```bash
   git clone https://github.com/ibrahimaydn/STM32H755_projects.git
