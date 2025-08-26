# 🚀 STM32H755 Çift Çekirdekli Eğitim Serisi

Bu depo, **STM32H755 NUCLEO-H755ZI-Q** geliştirme kartı ile **çift çekirdekli gömülü sistem geliştirmeyi öğrenmek isteyenler** için hazırlanmış **56 adımlık kapsamlı bir eğitim setini** içerir.  

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

---

### **Temel Başlangıç (Tek Çekirdek - M7)**
1. **01_Basic_Blink** → Dahili LED yakma (**M7**)  
2. **02_Button_Control** → Buton ile LED kontrolü (**M7**)  
3. **03_External_LED_Blink** → Harici LED yakma (**M7**)  
4. **04_Buzzer_Output** → Buzzer ile ses çıkarma (**M7**)  
5. **05_Debounce_Button** → Buton debounce yazılım tekniği (**M7**)  

---

### **GPIO ve Timer Uygulamaları**
6. **06_Timer_Basic_Blink** → Timer ile LED yakma (**M7**)  
7. **07_Timer_Interrupt_LED** → Timer interrupt ile LED kontrolü (**M7**)  
8. **08_PWM_Basic** → PWM ile LED parlaklık kontrolü (**M7**)  
9. **09_PWM_Buzzer_Tone** → PWM ile buzzer frekans üretimi (**M7**)  
10. **10_Input_Capture_Button** → Timer input capture ile buton ölçümü (**M7**)  

---

### **UART Haberleşme**
11. **11_UART_Send** → UART ile bilgisayara veri gönderme (**M7**)  
12. **12_UART_Receive** → UART ile bilgisayardan veri alma (**M7**)  
13. **13_UART_LED_Control** → UART üzerinden LED kontrolü (**M7**)  
14. **14_UART_Interrupt** → UART interrupt ile veri alma (**M7**)  
15. **15_UART_DMA** → UART DMA ile hızlı veri aktarımı (**M7**)  

---

### **İki STM32 Arası Haberleşme (UART / SPI / I2C)**
16. **16_UART_STM32_to_STM32** → İki STM32 arasında UART haberleşmesi  
17. **17_SPI_STM32_to_STM32** → İki STM32 arasında SPI haberleşmesi  
18. **18_I2C_STM32_to_STM32** → İki STM32 arasında I2C haberleşmesi  

---

### **SPI Haberleşme**
19. **19_SPI_Master** → SPI master ile veri gönderimi (**M7**)  
20. **20_SPI_Slave** → SPI slave ile veri alımı (**M7**)  
21. **21_SPI_OLED_Display** → SPI OLED ekran sürme (**M7**)  

---

### **I2C Haberleşme**
22. **22_I2C_Scan** → I2C cihaz taraması (**M7**)  
23. **23_I2C_LCD** → I2C LCD ekran kontrolü (**M7**)  
24. **24_I2C_EEPROM** → I2C EEPROM okuma/yazma (**M7**)  

---

### **ADC - Analog Okuma**
25. **25_ADC_Potentiometer** → Potansiyometre ADC okuma (**M7**)  
26. **26_ADC_Temperature** → Dahili sıcaklık sensörü okuma (**M7**)  
27. **27_ADC_DMA** → ADC verilerini DMA ile okuma (**M7**)  

---

### **Sensör Entegrasyonları**
28. **28_MPU6050_I2C** → MPU6050 IMU sensör entegrasyonu (**M7**)  
29. **29_HCSR04_Ultrasonic** → HC-SR04 ultrasonik mesafe sensörü (**M7**)  
30. **30_DHT11_Temperature_Humidity** → DHT11 sıcaklık & nem sensörü (**M7**)  
31. **31_BMP280_Pressure** → BMP280 basınç sensörü (**M7**)  
32. **32_LDR_Light_Sensor** → LDR ile ışık ölçümü (ADC) (**M7**)  

---

### **Harici Bellek ve SD Kart**
33. **33_SDCard_FatFS** → SD kart kullanımı, dosya yazma/okuma (**M7**)  
34. **34_Flash_Write_Read** → Harici flash hafıza kullanımı (**M7**)  

---

### **RTOS Uygulamaları (FreeRTOS - M7)**
35. **35_FreeRTOS_Basic_Task** → FreeRTOS ile LED blink task (**M7**)  
36. **36_FreeRTOS_Queue** → FreeRTOS queue kullanımı (**M7**)  
37. **37_FreeRTOS_Semaphore** → FreeRTOS semaphore ile senkronizasyon (**M7**)  
38. **38_FreeRTOS_Timer** → FreeRTOS yazılım timer kullanımı (**M7**)  

---

### **Ethernet & İnternet Bağlantısı**
39. **39_LwIP_TCP_Server** → STM32 TCP server (**M7**)  
40. **40_LwIP_TCP_Client** → STM32 TCP client (**M7**)  
41. **41_HTTP_Client** → STM32 HTTP GET isteği (**M7**)  
42. **42_MQTT_Client** → STM32 MQTT client uygulaması (**M7**)  

---

### **Çekirdekler Arası Haberleşme (M7 ↔ M4)**
43. **43_CM7_to_CM4_Message** → CM7’den CM4’e mesaj gönderme  
44. **44_CM4_to_CM7_Message** → CM4’ten CM7’ye mesaj gönderme  
45. **45_CM7_CM4_SharedMemory** → Paylaşımlı bellek ile iletişim  
46. **46_CM7_CM4_Sync_LED** → Çekirdekler arası LED senkronizasyonu  

---

### **Gelişmiş Timer Uygulamaları**
47. **47_PWM_Motor_Control** → PWM ile DC motor kontrolü (**M7**)  
48. **48_Servo_Motor_Control** → Servo motor kontrolü (PWM) (**M7**)  
49. **49_Input_Capture_Frequency** → Sinyal frekans ölçümü (Input Capture) (**M7**)  
50. **50_Quadrature_Encoder** → Enkoder ile motor konum ölçümü (**M7**)  

---

### **Son Uygulamalar**
51. **51_Remote_Sensor_Data** → UART ile sensör verilerini PC’ye gönderme (**M7**)  
52. **52_DualCore_Sensor_Fusion** → CM7 sensör okuma, CM4 veri işleme
53. **53_MultiSensor_IoT_Node** → Çok sensörlü IoT düğümü (M4 sensör verisi toplar, M7 buluta gönderir)  
54. **54_DualCore_RobotControl** → Çift çekirdekli robot/drone mimarisi (M4 sensör + M7 motor/haberleşme)  
55. **55_Smart_Home_Gateway** → STM32 tabanlı akıllı ev IoT merkezi (Ethernet/WiFi + MQTT)  
56. **56_Final_Project** → Çok çekirdekli + sensör + haberleşme içeren final proje  

---
### **Gerçek Hayat IoT Projeleri**


---

## 🛠 Kurulum
1. Depoyu klonlayın:
   ```bash
   git clone https://github.com/ibrahimaydn/STM32H755_projects.git
