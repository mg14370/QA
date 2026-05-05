Testplan & Testfallentwurf

GroceryMate - Market Mate  

1. Produktanalyse

Zielsetzung
GroceryMate (Market Mate) ist ein Online‑Lebensmittelshop. Ziel dieses Releases: Einführung von drei neuen Funktionen - Bewertungsmodul, Altersverifikation für 18+ Produkte (Anzeige‑Pop‑up) sowie dynamische Versandkostenberechnung -und Sicherstellung, dass bestehende Kernfunktionen nicht beeinträchtigt werden.

Zielgruppe

- Privatpersonen ab 18
- Jahren (für vollen Zugriff auf 18+ Inhalte)  
- Registrierte Nutzer (Hauptzielgruppe für Bewertungen)  
- Gastnutzer (eingeschränkter Zugriff)  
- Stakeholder: Product Owner, Entwicklerteam, QA, Endnutzer (UAT)

Hardware‑ & Software‑Spezifikationen

- Geräte: PCs, Laptops, Smartphones, Tablets (empfohlen mind. 4 GB RAM, 2 GHz CPU)  
- Betriebssysteme: Windows, macOS, Android, iOS  
- Browser: Chrome, Firefox, Safari, Edge  
- Abhängigkeiten: Backend‑Dienste, interner Profanity‑Filter‑Service, externe Zahlungsanbieter

Produktfunktionen (relevant für Release)

- Registrierung & Login  
- Produktkatalog & Suche  
- Warenkorb & Checkout  
- Bewertungsmodul:
  - 5‑Sterne (Pflichtfeld)
  - Optionales Textfeld, max. 500 Zeichen
  - Bewertungen nur für eingeloggte Nutzer
  - Pro Produkt genau 1 Bewertung pro Nutzer; Editfunktion ersetzt bestehende Bewertung
  - Durchschnittsbewertung = arithmetisches Mittel aller Sterne, Anzeige mit 1 Dezimalstelle
  - Profanity‑Filter und Melden/Moderation
- Altersverifikation:
  - Anzeige‑Pop‑up bei 18+ Produkten (z. B. alkoholische Produkte) - Hinweis/TO‑DO: Klären, ob weitere Produktkategorien ab 18 existieren (z. B. Tabak, verschreibungspflichtige Produkte).
  - Hinweis zur technischen Erwartung: Der Server darf 18+ Produkte nicht lediglich unterdrücken im UI; Tests müssen Anzeige/Access‑Kontrolle und API‑Antworten prüfen (Anzeige + API‑Response‑Checks).
- Dynamische Versandkosten:
  - Kostenlos ab 20 €, sonst 5 €

---

2. Teststrategie

Scope of Testing

- In Scope  
  - Bewertungsmodul: UI‑Validierung, Speichern/Editieren/Löschen, Mittelwertberechnung, Profanity‑Filter‑Integration (UI + Service‑Response prüfen)  
  - Altersverifikations‑Pop‑up: Anzeige/Validierung/Session‑Verhalten; Zugriffskontrolle für 18+ Produkte (UI‑Anzeige + API‑Antworten prüfen)  
  - Versandkostenberechnung: Echtzeit‑Update im Warenkorb, Schwellenwertverhalten, Wechsel bei Mengen-/Preisänderung  
  - Regressionstest: Login, Warenkorb, Checkout‑Grundfunktionen nach Änderungen

- Out of Scope  
  - Direkte Backend‑Datenbank‑Operationen ohne UI‑Einfluss (DB‑Migrationsdetails)  
  - Interne Implementierungsdetails von Drittanbieter‑Systemen (z. B. interne Architektur des Profanity‑Filters, Zahlungsanbieter‑Interna)  
  - Performance‑Extremtests (>10.000 gleichzeitige Nutzer)

Testarten

- Funktionstests  
- Regressionstests  
- Grenzwerttests (Zeichenlimit, Versand‑Schwellenwert, Altersgrenze)  
- Sicherheitstests (Bypass‑Versuche als Prüfaktivität; Fokus: Nachweis, dass Anzeige/API‑Responses korrekt sind)  
- Usability‑Tests  
- Negative/Fehlerfalltests

 Testlogistik / Rollen

- Testmanager: Jane Smith  
- QA (Funktion & Regression): John Doe  
- QA (Sicherheit & Grenzwerte): Alice Johnson  
- QA (Usability): Robert Brown  
- UAT Endanwender: Maria Garcia

---

3. Testziele

1. Funktionalität: Bewertungsmodul, Altersverifikation und Versandberechnung arbeiten wie spezifiziert.  
2. Zugriffskontrolle: 18+ Produkte werden nur angezeigt/zugänglich, wenn Altersverifikation erfolgreich (UI‑Anzeige + API‑Antwort).  
3. Korrektheit: Mathematisch korrekte Durchschnitts‑ und Versandberechnungen (1 Dezimalstelle für Bewertungen).  
4. Datenintegrität: Reviews korrekt gespeichert; ein Nutzer = eine Bewertung; Audit‑Log‑Einträge vorhanden.  
5. Usability: Pop‑ups und Bewertungsprozesse sind verständlich und führen zu minimalen Abbrüchen.  
6. Regression: Änderungen brechen zentrale Flows (Login/Warenkorb/Checkout) nicht.

Priorität: Zugriffskontrolle & Funktionalität > Korrektheit & Datenintegrität > Usability > Regression‑Reporting.

---

4. Testkriterien

Aussetzungskriterien (Suspension)

- Kritische Blocker‑Bugs, die Tests verhindern (z. B. Auth‑Service down).  
- Testumgebung nicht verfügbar/instabil.  
- Fehlende essentielle Testdaten/Abhängigkeiten.

Abnahmekriterien (Exit)

- Alle geplanten Testfälle ausgeführt.  
- Ausführungsrate ≥ 95 %.  
- Bestehensrate ≥ 90 % der ausgeführten TCs.  
- Keine offenen Defekte mit Severity Critical/High.  
- UAT abgeschlossen und signiert.  
- Nachweis: Altersverifikations‑Bypassversuche wurden geprüft und nicht erfolgreich (API/UI‑Checks bestanden).

---

5. Ressourcenplanung

- Personal: QA‑Team (4), Entwickler, 1 UAT‑Endanwender  
- Hardware: reale Endgeräte (Desktop + Mobile)  
- Software/Tools: Browser (aktuell), GitHub Issues, Postman (API‑Checks), Testmanagement in Markdown/Sheets  
- Testdaten: Testaccounts (volljährig, minderjährig, Gast), Produkt‑IDs (inkl. 18+ Produkt)

---

6. Testumgebung

- Environments: DEV → TEST → ACC → PROD  
- Geräte: Reale Endgeräte + Browser (Desktop/Mobile)  
- Separate Testdatenbank / vorbereitete Testkonten  
- Vorbereitete Produktdatensätze (mind. 1 alkoholisches Produkt, mehrere bewertbare Produkte)

---

7. Zeitplan (Kurz)

| Aktivität | Start | Ende | Verantwortlich | Aufwand |
|---|---:|---:|---|---:|
| Testplanung & Finalisierung TCs | 01.04.2026 | 05.04.2026 | Testmanager/QA | 20 Std. |
| Testfalldesign abgeschlossen | 06.04.2026 | 14.04.2026 | QA‑Team | 40 Std. |
| Unittest (Dev) | 15.04.2026 | 23.04.2026 | Entwicklerteam | 60 Std. |
| Integrationstest | 24.04.2026 | 28.04.2026 | QA‑Team | 30 Std. |
| Systemtest | 29.04.2026 | 09.05.2026 | QA‑Team | 80 Std. |
| Regressionstest | 10.05.2026 | 14.05.2026 | QA‑Team | 40 Std. |
| Performanztest | 15.05.2026 | 17.05.2026 | QA‑Team | 20 Std. |
| Sicherheitstest | 18.05.2026 | 20.05.2026 | QA‑Team | 20 Std. |
| Abnahmetest (UAT) | 21.05.2026 | 30.05.2026 | Endanwender | 50 Std. |
| Produktionsfreigabe | 01.06.2026 | 01.06.2026 | DevOps | 10 Std. |

---

8. Test‑Deliverables

- Testplandokument (Markdown + exportiertes PDF)  
- Testfälle & Testskripte (Markdown)  
- Testdatenliste (CSV/Markdown)  
- Testdurchführungsberichte (Execution Reports)  
- Fehlerberichte (GitHub Issues)  
- UAT‑Abnahmeprotokoll (Sign‑off)
