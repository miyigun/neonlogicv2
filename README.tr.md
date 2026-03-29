# Neon Logic: Matrix Puzzle

**Neon Logic: Matrix Puzzle**, klasik “Lights Out” mantığından ilham alan, tarayıcıda çalışan **desen eşleştirme** tabanlı bir mantık oyunudur.

Solda **HEDEF (TARGET)** deseni gösterilir. Sağdaki **KONTROL / INPUT** ızgarasında hamle yaparak aynı deseni oluşturmanız gerekir.  
Her tıklama, seçilen hücreyi ve **4 komşusunu** (üst, alt, sağ, sol) birlikte tersine çevirir.

---

## Özellikler

### 1. Lights-Out Mekaniği (5×5)
- Yan yana iki 5×5 ızgara:
  - **HEDEF (TARGET):** kopyalanacak desen
  - **KONTROL (INPUT):** oyuncunun hamle yaptığı desen
- Bir hücreye basınca:
  - kendisi
  - üst / alt / sağ / sol komşuları (sınır içindeyse) toggle olur

### 2. Sonsuz Seviye İlerlemesi (Prosedürel)
- Seviye **1**’den başlar, her başarıdan sonra otomatik artar
- Her seviyede yeni ve çözülebilir bir hedef desen üretilir
- Zorluk, seviye ile birlikte artar (`difficulty = currentLevel + 2`)

### 3. Basit Arayüz ve Geri Bildirim
- Seviye tamamlanınca üstte bildirim banner’ı
- 1.5 saniye sonra otomatik olarak sonraki seviyeye geçiş
- Kontroller:
  - **Sıfırla:** sadece oyuncu ızgarasını temizler (hedef aynı kalır)
  - **Pas Geç:** seviyeyi artırır ve yeni hedef üretir

### 4. Neon Retro Stil
- Orbitron font + neon vurgu renkleri
- Tek sayfalık sade yapı

---

## Proje Yapısı

- `index.html` — oyunun tamamı (arayüz + stiller + oyun mantığı)

---

## Başlangıç

Yerelde çalıştırmak için:

1. Repoyu klonlayın:
   ```bash
   git clone https://github.com/miyigun/neonlogicv2.git
   ```
2. Klasöre girin:
   ```bash
   cd neonlogicv2
   ```
3. `index.html` dosyasını tarayıcıda açın

> Öneri: Daha stabil çalışması için local server kullanın.
Örnek (Python):
```bash
python -m http.server 8000
```
Sonra şurayı açın:
- `http://localhost:8000`

---

## 🛠️ Kullanılan Teknolojiler
- HTML / CSS / JavaScript (tek sayfa)
- Google Fonts (Orbitron)

---

## 📌 Notlar
- **Kazanma koşulu:** KONTROL/INPUT ızgarası, HEDEF ile hücre hücre aynı olmalıdır.
- **Sıfırla**, hedefi değiştirmez; sadece oyuncu desenini temizler.
- Hedef desen, geçerli hamleler uygulanarak üretildiği için seviyeler çözülebilirdir.

---

## 📜 Lisans
MIT lisansı (LICENSE dosyasına bakınız).