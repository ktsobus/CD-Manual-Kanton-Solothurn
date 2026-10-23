# CD-Manual Kanton Solothurn

Extrakt des Corporate Design Manuals «CD-Manual Kanton Solothurn – Gesamtübersicht,
Arbeitsinstrument für die Verwaltung und die Druckindustrie» vom Miro-Board
<https://miro.com/app/board/uXjVKj6w4cc=/> (Stand der Extraktion: 23.10.2026).

- **[CD-Manual-Kanton-Solothurn.md](CD-Manual-Kanton-Solothurn.md)** – vollständige Abschrift aller 38 Seiten
- **[frames/](frames/)** – Bild jeder Seite (Dateiname = Reihenfolge im Manual)
- **[board-overview.png](board-overview.png)** – Gesamtansicht des Boards

Massgebend bleibt das Original auf Miro; bei Abweichungen gilt das Board.

![Übersicht des Boards](board-overview.png)

| Kapitel | Seiten |
| ------- | ------ |
| Titel, Inhalt | [00](frames/00-titel.png), [01](frames/01-inhalt.png) |
| 1 Logo | [Intro](frames/10-logo.png) · [Varianten](frames/11-logo-varianten.png) · [Sprach-Varianten](frames/12-sprach-varianten.png) · [Grössen](frames/13-logo-groessen.png) · [Anwendung](frames/14-logo-anwendung.png) · [Don'ts](frames/15-logo-donts.png) |
| 2 Typografie | [Intro](frames/20-typografie.png) · [Schriften](frames/21-schriften.png) · [Hauptschrift](frames/22-schriftschnitte-hauptschrift.png) · [Zusatzschrift](frames/23-schriftschnitte-zusatzschrift.png) · [Satzzeichen](frames/24-satzzeichen.png) · [Wortabstand](frames/25-wortabstand.png) |
| 3 Farben | [Intro](frames/30-farben-intro.png) · [Farben](frames/31-farben.png) · [Farben für Grafiken](frames/32-farben-fuer-grafiken.png) · [Don'ts](frames/33-farben-donts.png) |
| 4 Grundsätze | [Intro](frames/40-grundsaetze.png) · [Absender](frames/41-absender.png) · [Textanwendung](frames/42-textanwendung.png) · [Bildsprache](frames/43-bildsprache.png) · [Don'ts](frames/44-grundsaetze-donts.png) |
| 5 Anwendung | [Intro](frames/50-anwendung.png) · [Briefpapier](frames/51-briefpapier.png) · [Visitenkarten](frames/52-visitenkarten.png) · [Adressen](frames/53-adressen.png) · [Kuverts](frames/54-kuverts.png) · [Umschläge](frames/55-umschlaege.png) ([A4](frames/56-umschlag-a4.png), [A5](frames/57-umschlag-a5.png), [A6/5](frames/58-umschlag-a6-5.png)) · [Stelleninserate](frames/59-stelleninserate.png) ([Full](frames/60-stelleninserat-full.png), [Short](frames/61-stelleninserat-short.png), [Teaser](frames/62-stelleninserat-teaser.png)) · [PowerPoint](frames/63-powerpoint.png) · [Don'ts](frames/64-anwendung-donts.png) |

---

## Umsetzung im Dashboard

Das Manual ist für Verwaltung und Druck geschrieben; für Bildschirme gibt es keine
eigenen Vorgaben. Das Dashboard überträgt die Regeln deshalb sinngemäss – und zwar
so, dass nichts verwendet wird, was das Manual nicht vorsieht.

| Vorgabe im Manual | Umsetzung | Datei |
| ----------------- | --------- | ----- |
| Logo nur aus Originaldateien, keine Veränderung ([Logo](frames/10-logo.png), [Don'ts](frames/15-logo-donts.png)) | Logo wird **nicht nachgebaut**; Platzhalter für `logo.svg` / `logo-negativ.svg`. Fehlt die Datei, bleibt der Platz leer – kein Ersatzschriftzug, kein Logo ohne Wappen | `public/assets/README.md`, `public/index.html` |
| Farbiges Logo bis 40 % Hintergrund, darüber negativ weiss heraldisch; Wappen in Rot nicht auf mehr als 5 % Hintergrund ([Anwendung](frames/14-logo-anwendung.png)) | Kopfzeile immer reinweiss mit farbigem Logo; im dunklen Modus die negative Variante | `public/css/app.css` (`.logo__img`) |
| Schutzraum X um das Logo ([Grössen](frames/13-logo-groessen.png)) | Freiraum rund um das Logo, keine anderen Elemente im Schutzraum | `.logo` |
| Hausschrift Frutiger LT Std; Hauptschnitte 55 Roman, 56 Italic, 75 Black, 76 Black Italic; Condensed nur in platzarmen Situationen wie Grafiken ([Schnitte](frames/22-schriftschnitte-hauptschrift.png), [Zusatz](frames/23-schriftschnitte-zusatzschrift.png)) | Nur diese vier Schnitte (400/700 normal/kursiv); Condensed nur für Achsen-/Spaltenbeschriftungen in Grafiken. Lokal installierte Frutiger wird verwendet, sonst Arial | `public/css/fonts.css` |
| Solothurner Rot RGB 204/0/0, Schwarz, Weiss; Grafikfarben Grau 100/107/118, Schwarz 51/51/51, Zusatzfarben ([Farben](frames/31-farben.png), [Grafiken](frames/32-farben-fuer-grafiken.png)) | Alle Farben stammen aus dieser Palette bzw. sind Tonwerte davon (wie in der PowerPoint-Vorlage, z. B. DodgerBlue4 8 % = `#ECF1F6`). Datenfarben sind auf Kontrast (≥ 3:1 bzw. Heatmap ≥ 2:1) und gleichmässige Helligkeitsstufen geprüft; Zellbeschriftungen ≥ 4.5:1 | `public/css/tokens.css` |
| Keine willkürlichen Farben, keine Farbverläufe oder Schattierungen ([Farben Don'ts](frames/33-farben-donts.png)) | Flache Flächen, Haarlinien statt Schatten, keine Verläufe | `public/css/app.css` |
| Rotes Quadrat links neben dem Seitentitel, Kapitel-Kennzeichnung «3 FARBEN →» (alle Seiten) | Rotes Quadrat beim Titel; Abschnitte «1 ÜBERSICHT ⟶», «2 ANALYSE ⟶», «3 APPLIKATIONEN ⟶» mit feinem roten Pfeil | `public/index.html`, `.section__title` |
| Kein zentrierter Satz; Flattersatz; Satzbreite max. ~70 Zeichen ([Textanwendung](frames/42-textanwendung.png)) | Fliess- und Tabellentexte linksbündig (auch Zahlen in Matrixzellen), Fliesstext auf 70 Zeichen begrenzt; einzig Achsen- und Säulenbeschriftungen richten sich an ihrer Marke aus | `public/css/app.css` |
| «Guillemets», Halbgeviertstrich für Aufzählungen, %-Zeichen, echte Auslassungspunkte ([Satzzeichen](frames/24-satzzeichen.png)) | UI-Texte mit « », – und …; Listen mit Halbgeviertstrich | `public/js/*`, `.dash-list` |
| Absender: Amtsbezeichnung in Frutiger Black Italic, einheitliche Schreibweise ([Absender](frames/41-absender.png)) | Optionale Amtsbezeichnung (`DASHBOARD_UNIT`) in der Fusszeile, Black Italic | `.absender` |
| Status mit Farbe | Status (Handlungsbedarf, End of Life, ohne Verantwortliche) immer **Symbol + Text**, nie nur Farbe; Rot = kritisch, DarkOrange = ernst, Gold = Warnung | `public/js/icons.js` |

### Farbpalette im Dashboard

| Rolle | Hell | Dunkel | Herkunft |
| ----- | ---- | ------ | -------- |
| Marke (Quadrat, Pfeile, Primärbutton) | `#CC0000` | `#CC0000` | Solothurner Rot |
| Text | `#000000` / `#333333` | `#FFFFFF` | Schwarz / Grafik-Schwarz |
| Text sekundär | `#646B76` | `#AAAEB4` | Grau / Grau 55 % |
| Flächen | `#FFFFFF`, `#ECF1F6` | `#161616`, `#222222` | Weiss, DodgerBlue4 8 % / Schwarz-Tonwerte |
| Datenreihe | `#235C94` | `#059CCF` | DodgerBlue4 92 % / DeepSkyBlue2 85 % |
| Heatmap (5 Stufen) | `#9BB5CE` → `#104E8B` | `#145E78` → `#00B2EE` | Tonwerte DodgerBlue4 / DeepSkyBlue2 |
| Status | `#228B22`, `#E1D700`, `#E18C00`, `#CC0000` | gleich | ForestGreen, Gold, DarkOrange1, Rot |

**Offener Punkt:** Auf der Seite [Farben für Grafiken](frames/32-farben-fuer-grafiken.png) sind
«DarkOrange 1» und «Gold» mit **R 225** beschriftet, die Farbflächen sind aber mit **R 255**
dargestellt (`#FF8C00` / `#FFD700` – das entspricht auch den Farbnamen). Das Dashboard verwendet
vorerst die beschrifteten Werte (`#E18C00` / `#E1D700`, nur in Status-Symbolen). Nach Klärung mit
dem Kompetenzzentrum für Publikationsmedien ggf. in `public/css/tokens.css` anpassen.
