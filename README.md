# Kafka Exercise 03 – Java Producer & Consumer

##  Proje Açıklaması
Bu projede Apache Kafka üzerinde Java ile Producer ve Consumer uygulamaları geliştirildi. Kafka broker Docker üzerinde Google Cloud VM ile çalıştırıldı. Producer mesaj gönderirken, Consumer gelen mesajları dinleyip terminale yazdırmaktadır.

---

##  Kullanılan Teknolojiler
- ☁️ Google Cloud VM (Debian)
- 🐳 Docker & Kafka (Confluentinc/cp-kafka)
- ☕ Java (OpenJDK 11)
- Apache Kafka Java Client Library (`kafka-clients-3.7.0.jar`)

---

##  Proje Yapısı
kafka-java-ex03/
├── libs/
│   └── kafka-clients-3.7.0.jar
├── ProducerExample.java
├── ConsumerExample.java
├── README.md
└── screenshots/ (Terminal çıktıları)

---

## ⚙ Kurulum ve Çalıştırma

### 1️⃣ Docker Kafka Broker'ı Başlat
```bash
sudo docker ps
```
2️⃣ Java Dosyalarını Derle
```bash
javac -cp ".:libs/*" ProducerExample.java
javac -cp ".:libs/*" ConsumerExample.java
```
3️⃣ Consumer’ı Başlat (Ayrı Terminal)
```bash
java -cp ".:libs/*" ConsumerExample
```
4️⃣ Producer’ı Başlat (Ayrı Terminal)
```bash
java -cp ".:libs/*" ProducerExample
```
Producer terminalinde şu mesajı göreceksiniz:
Message sent successfully!
Consumer terminalinde ise gönderilen mesaj görüntülenir.

