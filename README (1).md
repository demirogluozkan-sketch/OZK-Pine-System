# OZK Lean Modular System — 3 Motor (v2.7)

TradingView **Pine Script v6** strateji dosyası. Modüler `type`/`method` mimarisi
(4 type, 15+ method, 9 section) ile backtest odaklı bir alım-satım sistemi.

Güncel sürüm: **r37**

## Dosyalar

| Dosya | Açıklama |
|-------|----------|
| `OZK_3Motor_v2_7_Mod_r37.pine` | Strateji kodu (TradingView'a yapıştırılır) |
| `OZK_3Motor_v2_7_Mod_DEVIR_PROMPT_r37.txt` | Tam bağlam / devir notları (mimari, revizyon geçmişi, açık konular) |

## Mimari özet

Tek bir **AKTIF MOTOR** seçicisi ile sadece biri çalışır:

- **Motor 1 (Hibrit):** Gösterge (AT/GC/ST) + EMA Rejim + fiyat üçlü koşulu.
- **Motor 2 (Basit):** Sadece çizgi crossover (AT/GC/ST), EMA Rejim filtresi yok.

Göstergeler: **AT** (AlphaTrend), **GC** (G-Channel), **ST** (SuperTrend).

**EMA Backtest** toggle'ı: "EMA Periyot" değeriyle saf EMA crossover çalıştırıp
(Panel 2'den) en kârlı periyodu bulmak içindir; bulunan değer Motor 1 hibritinde rejim
çizgisi olur.

İki panelli dashboard: **Panel 1** canlı durum, **Panel 2** backtest istatistikleri
(net kar, win rate, profit factor, max DD).

## Strateji ayarları

- Komisyon: %0.01
- Sermaye: 100.000 TL
- Backtest penceresi: son 4000 bar

## Kullanım (TradingView)

1. TradingView → Pine Editor.
2. `OZK_3Motor_v2_7_Mod_r37.pine` içeriğini yapıştır.
3. Kaydet (Ctrl+S) → "Add to chart".
4. Ayarlardan motoru, göstergeyi ve (gerekirse) EMA Backtest'i seç.

## Sürümleme

Her değişiklikte revizyon numarası artar (`rXX`). Detaylı geçmiş devir promptundaki
"REVİZYON GEÇMİŞİ" bölümündedir.
