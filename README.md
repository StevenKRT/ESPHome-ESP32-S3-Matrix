# ESP32-S3 8×8 LED-Matrix mit ESPHome und Home Assistant

Dieses Repository enthält eine vollständige ESPHome-Konfiguration für eine 8×8 RGB-LED-Matrix auf Basis eines ESP32-S3.  
Die Matrix ist vollständig in Home Assistant integriert und eignet sich als visuelles Signal- und Statusanzeigegerät.

---

## Einsatzbereiche

- Signallicht (Status, Warnung, Hinweis)
- „Besetzt / Frei“-Anzeige für Toilette oder Bad
- Visuelle Rückmeldung für Automationen
- Tür-, Klingel- oder Benachrichtigungsanzeige
- Farbanzeige oder Symbolanzeige pro Zustand

---

## Funktionen

- 8×8 RGB-LED-Matrix (64 LEDs, WS2811/WS2812-kompatibel)
- Steuerung über Home Assistant
- Mehrere Anzeigemodi (Symbole, Farbe, Flächen)
- Einstellbare Helligkeit
- Farbsteuerung über RGB-Entity
- Entprellte Modusumschaltung
- Statusspeicherung über Neustarts
- OTA-Updates
- Verschlüsselte ESPHome-API
- WLAN-Fallback-Access-Point

---

## Hardware

- ESP32-S3 (DevKitC-1 oder kompatibel)
- 8×8 NeoPixel / RGB-LED-Matrix
- Externe 5-V-Versorgung empfohlen

AliExpress:  
[ESP32-S3-Matrix wifi bluetooth entwicklung board 8x8 RGB-LED mit qst haltung gyro sensor qmi8658c für arduino python](https://s.click.aliexpress.com/e/_EQnYzJ2)

---

## Technische Parameter

| Parameter | Wert |
|---------|------|
| Matrixgröße | 8×8 (64 LEDs) |
| LED-Typ | WS2811 |
| Farbe | RGB |
| Steuerung | ESPHome / Home Assistant |
| Helligkeit | 1–100 % |
| GPIO Daten | GPIO14 |
| Versorgung | 5 V |

---

## Anzeigemodi

Über Home Assistant auswählbar:

- Aus
- Bullseye
- Heart
- Check
- Cross
- Bell
- Pflanzenlicht
- Stop
- L
- Farbe (vollflächig, frei wählbar)

---

## Home-Assistant-Entitäten

- Select: Display Mode
- Number: Matrix Brightness
- Light: Matrix Farbe
- Device Status (über ESPHome)
- OTA-Update-Funktion

---

## Netzwerkverhalten

- WLAN-Anbindung
- Fallback-Hotspot bei Verbindungsverlust
- OTA-Updates über WLAN
- Verschlüsselte ESPHome-API

---

## Dateien

- `led8x8-qmi8658.yaml` – vollständige ESPHome-Konfiguration

---

## Hinweise zum Einsatz als „Besetzt / Frei“-Anzeige

Die Anzeige kann direkt über Home-Assistant-Automationen gesteuert werden, z. B.:

- Rot / Stop → Besetzt
- Grün / Check → Frei
- Symbolwechsel bei Türkontakt
- Automatische Abschaltung nach Zeit

---

## Lizenz

Freie Nutzung. Keine Gewährleistung.
