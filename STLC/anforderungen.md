## Anforderungen

### 1. Bewertungssystem für Produkte

**Unklare Anforderung**  
Nutzer sollen Produkte mit einem 5‑Sterne‑System bewerten und zusätzlich schriftliches Feedback hinterlassen können.

**Fragen**
1. Wie viele Zeichen darf das schriftliche Feedback maximal umfassen?  
2. Ist die Vergabe von Sternen eine Pflichtangabe für das Absenden eines Kommentars?  
3. Dürfen anonyme Reviews abgegeben werden oder muss eine Bewertung mit einem Nutzerkonto verknüpft sein?  
4. Werden Duplicate‑Reviews (mehrere Bewertungen desselben Nutzers für ein Produkt) erlaubt oder verhindert?

**Detaillierte Anforderung**  
Auf der Produktdetailseite wird ein Bewertungsmodul implementiert, das aus einer 5‑Sterne‑Skala (Pflichtfeld) und einem optionalen Textfeld besteht. Das Textfeld erlaubt maximal 500 Zeichen. Bewertungen sind nur für angemeldete Benutzer möglich; anonyme Bewertungen sind nicht zulässig. Pro Produkt darf ein Nutzer genau eine Bewertung abgeben; ein Nutzer kann seine bestehende Bewertung über ein Bearbeitungsformular direkt editieren und nach Anpassung absenden - die gespeicherte Bewertung wird durch die bearbeitete Version ersetzt. Das System berechnet die durchschnittliche Produktbewertung, indem alle Sterne addiert und durch die Anzahl der Bewertungen geteilt werden, und zeigt das Ergebnis mit einer Nachkommastelle an (z. B. 4.2).

---

### 2. Altersverifikation für alkoholische Produkte

**Unklare Anforderung**  
Alkoholische Produkte erfordern eine Altersverifikation. Beim Aufrufen der Kategorie soll ein Fenster erscheinen, in dem Nutzer ihr Alter angeben müssen (18+), bevor sie Zugriff erhalten.

**Fragen**
1. In welchem Format soll das Geburtsdatum angegeben werden (z. B. DD‑MM‑YYYY)?  
2. Wann wird die Altersabfrage ausgelöst - beim Aufrufen der Kategorie, beim direkten Produktlink oder bei Suchergebnissen?  
3. Wird die Verifikation nur für die Dauer der Sitzung gespeichert oder dauerhaft an das Nutzerkonto gebunden?  
4. Dürfen minderjährige Nutzer alkoholische Produkte über direkte Links oder Suche sehen (Bypass‑Szenarien)?  
5. Gibt es noch andere Produktkategorien oder Artikel, die eine 18+ Verifikation erfordern?

**Detaillierte Anforderung**  
Zugriff auf alkoholische Produkte ist durch ein Alters‑Verifikations‑Pop‑up geschützt. Das Pop‑up erscheint, wenn ein Nutzer die Kategorie „Alcohol“, ein alkoholisches Produkt oder Suchergebnisse mit alkoholischen Artikeln öffnet. Im Pop‑up wird der Nutzer gebeten, sein Geburtsdatum im Format DD‑MM‑YYYY einzugeben; das System prüft, ob er mindestens 18 Jahre alt ist. Die erfolgreiche Verifikation wird für die aktuelle Sitzung gespeichert; bei angemeldeten Nutzern wird außerdem ein Verifikations‑Hinweis im Konto gesetzt. Nutzer unter 18 bekommen eine Meldung und können keine alkoholischen Produkte sehen; der übrige Shop bleibt nutzbar. Technisch darf der Server keine alkoholischen Produkte an nicht‑verifizierte oder minderjährige Nutzer anzeigen (auch nicht über direkte Links oder Suchergebnisse).

---

### 3. Änderungen bei den Versandkosten

**Unklare Anforderung**  
Versandkosten entfallen ab einem bestimmten Bestellwert. Darunter fallen Versandkosten an.

**Fragen**
1. Ab welchem Bestellwert entfallen die Versandkosten (Schwellenwert)?  
2. Wie hoch sind die Versandkosten, wenn der Bestellwert unter dem Schwellenwert liegt?  
3. Welche Beträge und Bezeichnungen sollen im Warenkorb angezeigt werden (z. B. Product Total, Shipment, Total)?  
4. Werden Versandkosten bei Änderung des Warenkorbs (Mengenänderung / Entfernen) automatisch neu berechnet?

**Detaillierte Anforderung**  
Im Warenkorb werden die Felder „Product Total“, „Shipment“ und „Total“ angezeigt. Es erscheint der Hinweis „Free shipment if your purchase is 20€ or more“. Ist Product Total < 20€, werden Versandkosten in Höhe von 5€ unter „Shipment“ ausgewiesen; bei Product Total ≥ 20€ ist „Shipment“ 0€. „Total“ ergibt sich automatisch als Product Total + Shipment. Änderungen im Warenkorb (Mengenänderung, Entfernen/Hinzufügen von Artikeln) lösen sofort eine Neuberechnung aus und aktualisieren „Shipment“ und „Total“ in Echtzeit. Rabatte werden vor Prüfung auf Versandfreiheit vom Product Total abgezogen.
