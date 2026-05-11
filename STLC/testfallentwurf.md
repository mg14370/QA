# Testfallentwurf (9 Testfälle - 3 pro Feature)

### **1. Bewertungsmodul**

**Test-Design-Techniken**: Use Case Testing, Boundary Value Analysis (BVA), Error Guessing

### Testfälle:

1. **Error Guessing**:
   - **Testfall**: Pflichtfeld Sterne prüfen
     - **Input**: keine Sterne auswählen
     - **Erwartetes Ergebnis**: Fehlermeldung "Bitte wähle eine Sternebewertung aus." → Review nicht gespeichert.

2. **Boundary Value Analysis (BVA)**:
   - **Testfall**: Zeichenlimit prüfen (500 Zeichen)
     - **Input**: Text mit genau 500 Zeichen eingeben
     - **Erwartetes Ergebnis**: Review gespeichert → Text vollständig mit 500 Zeichen angezeigt.

3. **Use Case Testing**:
   - **Testfall**: Ein Nutzer = eine Bewertung / Editieren
     - **Input**: vorhandene Bewertung bearbeiten
     - **Erwartetes Ergebnis**: Alte Bewertung wird durch die neue ersetzt → Durchschnitt neu berechnet und angezeigt.

---

### **2. Altersverifikation (18+)**

**Test-Design-Techniken**: Use Case Testing, Boundary Value Analysis (BVA)

### Testfälle:

1. **Use Case Testing**:
   - **Testfall**: Zugriff auf 18+ Kategorie ohne Altersnachweis
     - **Input**: Altersverifikations-Pop-up wegklicken und 18+ Produkt aufrufen
     - **Erwartetes Ergebnis**: Anstatt der 18+ Produkte wird eine Fehlermeldung angezeigt.

2. **Boundary Value Analysis (BVA)**:
   - **Testfall**: Grenzwert 18 Jahre (exakt)
     - **Input**: Geburtsdatum = (Heute: 18 Jahre)
     - **Erwartetes Ergebnis**: Zugriff auf 18+ Produkte gewährt.

3. **Boundary Value Analysis (BVA)**:
   - **Testfall**: Unter 18 Jahre (Minderjähriger)
     - **Input**: Geburtsdatum = (Heute: 17 Jahre)
     - **Erwartetes Ergebnis**: Hinweis „Du musst mindestens 18 Jahre alt sein.“ → Zugriff verweigert.

---

### **3. Versandkostenberechnung**

**Test-Design-Techniken**: Use Case Testing, Boundary Value Analysis (BVA)

### Testfälle:

1. **Boundary Value Analysis (BVA)**:
   - **Testfall**: Unter Schwellenwert (Versand 5 €)
     - **Input**: Warenkorb Product Total = 19,99 €
     - **Erwartetes Ergebnis**: Versandkosten 5,00 € → Total korrekt (24,99 €).

2. **Boundary Value Analysis (BVA)**:
   - **Testfall**: Genau Schwellenwert 20,00 € (versandfrei)
     - **Input**: Warenkorb Product Total = 20,00 €
     - **Erwartetes Ergebnis**: Versandkosten 0,00 € → Total korrekt (20,00 €).

3. **Use Case Testing**:
   - **Testfall**: Echtzeit‑Änderung beim Mengenupdate
     - **Input**: Warenkorb Product Total von 20,00 € auf 15,00 € verringern.
     - **Erwartetes Ergebnis**: Versandkosten wechseln von 0,00 € auf 5,00 € → Total korrekt (20,00 €).
