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

---

Testfallentwurf - Priorisierte Auswahl (9 Testfälle; 3 pro Feature) 

Begründung Top‑3
- TC‑01 (Pflichtfeld Sterne): verhindert ungültige Reviews - kritische Validierung.  
- TC‑03 (Ein Nutzer = eine Bewertung / Editieren): Kerngeschäftsregel, Datenintegrität.  
- TC‑04 (Pop‑up bei 18+ Zugriff): Zugriffskontrolle für altersbeschränkte Produkte - rechtlich/geschäftlich wichtig.

---

Feature 1 — Bewertungsmodul (TC‑01 … TC‑03)

- TC‑01 -Pflichtfeld Sterne prüfen (Top‑3)
  - Vorbedingung: Eingeloggter Nutzer ohne bestehende Bewertung  
  - Schritte: Produktseite öffnen → optional Text eingeben → keine Sterne auswählen → Absenden  
  - Erwartetes Ergebnis: Validierungsfehler "Bitte wähle eine Sternebewertung aus."; Review nicht gespeichert.  
  - Automatisierbarkeit: Hoch -deterministische UI‑Validierung.

- TC‑02 - Zeichenlimit prüfen (500 Zeichen)  
  - Vorbedingung: Eingeloggter Nutzer  
  - Schritte: Text mit genau 500 Zeichen eingeben → Sterne wählen → Absenden; zusätzlich Test mit 501 Zeichen  
  - Erwartetes Ergebnis: 500 Zeichen: Review gespeichert, Text vollständig angezeigt; 501 Zeichen: Eingabe begrenzt ODER Fehlermeldung "Maximale Zeichenanzahl überschritten."  
  - Automatisierbarkeit: Hoch - Grenzwerttest.

- TC‑03 - Ein Nutzer, eine Bewertung / Editieren (Top‑3)
  - Vorbedingung: Eingeloggter Nutzer hat bestehende Bewertung  
  - Schritte: Produktseite → Bewertung bearbeiten → Sterne/Text ändern → Absenden  
  - Erwartetes Ergebnis: Alte Bewertung wird durch neue ersetzt; Durchschnitt neu berechnet und angezeigt.  
  - Automatisierbarkeit: Hoch -prüfbar via API/DB + UI.

---

Feature 2 - Altersverifikation (18+) (TC‑04 … TC‑06)

- TC‑04 - Pop‑up bei Zugriff auf Alkohol‑Kategorie (Top‑3)
  - Vorbedingung: Nicht verifizierter Nutzer (eingeloggt oder Gast)  
  - Schritte: Kategorie "Alcohol" öffnen oder direkten Produktlink eines 18+ Produkts aufrufen  
  - Erwartetes Ergebnis: Altersverifikations‑Pop‑up erscheint (Anzeige); Nutzer kann Geburtsdatum eingeben oder abbrechen.  
  - Hinweis/TO‑DO: Klären, ob weitere Produktkategorien ab 18 bestehen (z. B. Tabak) und dieselbe Verifikation anwenden.  
  - Automatisierbarkeit: Teilweise - UI‑Anzeige manuell/automatisiert prüfen; API‑Response‑Checks automatisierbar.

- TC‑05 - Grenzwert 18 Jahre (exakt)  
  - Vorbedingung: Eingeloggter Nutzer; Geburtsdatum = heute 18 Jahre  
  - Schritte: Pop‑up ausfüllen mit DD‑MM‑YYYY → Bestätigen  
  - Erwartetes Ergebnis: Zugriff auf 18+ Produkte gewährt; Produktdetails sichtbar.  
  - Automatisierbarkeit: Hoch - deterministischer Input/Output.

- TC‑06 - Session‑Verifikation bleibt gültig  
  - Vorbedingung: Nutzer verifiziert sich erfolgreich  
  - Schritte: Verifizieren → zu anderer Kategorie navigieren → zurück zur Alkohol‑Kategorie in gleicher Session  
  - Erwartetes Ergebnis: Pop‑up erscheint nicht erneut; Zugriff direkt möglich.  
  - Automatisierbarkeit: Teilweise - Session‑State prüfen via automatisierte Tests.

---

Feature 3 - Versandkostenberechnung (TC‑07 … TC‑09)

- TC‑07 - Unter Schwellenwert (Versand 5 €)  
  - Vorbedingung: Warenkorb Product Total = 10,00 €  
  - Schritte: Warenkorb öffnen  
  - Erwartetes Ergebnis: Versandkosten 5,00 €; Total korrekt (15,00 €).  
  - Automatisierbarkeit: Hoch

- TC‑08 - Genau Schwellenwert 20,00 €  
  - Vorbedingung: Warenkorb Product Total = 20,00 €  
  - Schritte: Warenkorb öffnen  
  - Erwartetes Ergebnis: Versandkosten 0,00 €; Hinweistext "Versandfrei ab 20 €" sichtbar; Total korrekt.  
  - Automatisierbarkeit: Hoch

- TC‑09 - Echtzeit‑Änderung beim Mengenupdate  
  - Vorbedingung: Warenkorb Product Total = 15,00 €  
  - Schritte: Menge eines Artikels erhöhen bis Product Total ≥ 20,00 €  
  - Erwartetes Ergebnis: Versandkosten wechseln sofort von 5,00 € auf 0,00 €; Total aktualisiert in Echtzeit.  
  - Automatisierbarkeit: Hoch (UI+API)

---

Automatisierungsempfehlung (kurz)
- Empfohlen automatisieren: TC‑01, TC‑02, TC‑03, TC‑05, TC‑07, TC‑08, TC‑09 - rationale: deterministische Eingabe/Ausgabe, regressionsrelevant.  
- Teilweise/Manuell: TC‑04 (UI/Usability), TC‑06 (Session‑Edge). Moderations‑Workflows (Review melden) initial manuell prüfen; Profanity‑Filter‑API‑Responses automatisierbar.
