# Testdurchführung

## Szenario 1: Sternebewertung

Als Kunde von MarketMate kann ich ein Produkt nicht bewerten, ohne Sterne zu vergeben.

| Schritt | Aktion                                                                       | Erwartetes Ergebnis                                                                 | OK/NOK | URL                                            | Link zum Issue |
| ------- | ---------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ------ | ---------------------------------------------- | -------------- |
| 1       | Gehe zur Homepage von MarketMate                                                          | Homepage erscheint                                                                  | OK     | https://grocerymate.masterschool.com/          |                |
| 2       | Gib "Birchwood Quarter Pounders" in Suchleiste ein                          | Du wirst auf Produktseite weitergeleitet                                            | OK     | /product/66b3a57b3fd5048eacb479c8              |                |
| 3       | Klicke im Bewertungsfenster auf "Send" ohne Sterne zu vergeben              | Fehlermeldung erscheint: "Invalid input for the field 'Rating'. Please check your input." | OK     |                                                |                |


<img width="1323" height="800" alt="587948835-f2987fd1-de45-41be-b779-0773e5ebbca0" src="https://github.com/user-attachments/assets/577a785f-430f-4584-89c5-b91e68b4400f" />
<img width="1324" height="795" alt="587949631-e6ccb091-91ae-4e9e-b3ff-d22047970997" src="https://github.com/user-attachments/assets/9a7ff65f-4798-40c3-8899-018b2afe40f1" />
<img width="876" height="801" alt="587951316-381e0bfa-0fbe-4d5e-8647-e023b9130cd9" src="https://github.com/user-attachments/assets/15ca6226-f58f-455d-80a1-632b253ea560" />
<img width="800" height="429" alt="587951379-f25739fe-5a15-4ff0-b468-d1ebfd9834cb" src="https://github.com/user-attachments/assets/2f511c7d-df42-4137-8fbe-bdae39859e78" />






## Szenario 2: Max. 500‑Zeichen Bewertung

Als Kunde von MarketMate kann ich ein Produkt mit einem Text bis zu 500 Zeichen bewerten.

| Schritt | Aktion                                                                 | Erwartetes Ergebnis                                                               | OK/NOK | URL                                           | Link zum Issue |
| ------- | ---------------------------------------------------------------------- | --------------------------------------------------------------------------------- | ------ | --------------------------------------------- | -------------- |
| 1       | Gehe zur Homepage von MarketMate                                                      | Homepage erscheint                                                                | OK     | https://grocerymate.masterschool.com/         |                |
| 2       | Gib "Birchwood Quarter Pounders" in Suchleiste ein                     | Du wirst auf Produktseite weitergeleitet                                          | OK     | /product/66b3a57b3fd5048eacb479c8             |                |
| 3a      | Vergebe im Bewertungsfenster bis zu 5 Sterne                           |                                                                                   |        |                                               |                |
| 3b      | Gib 500 Zeichen in das Textfeld ein                                    | Nachricht erscheint: "500/500" und "You cannot tell us more about this product." | OK     |                                               |                |


<img width="1323" height="800" alt="screenshot" src="https://github.com/user-attachments/assets/f2987fd1-de45-41be-b779-0773e5ebbca0" />
<img width="1324" height="795" alt="screenshot" src="https://github.com/user-attachments/assets/e6ccb091-91ae-4e9e-b3ff-d22047970997" />
<img width="876" height="801" alt="screenshot" src="https://github.com/user-attachments/assets/381e0bfa-0fbe-4d5e-8647-e023b9130cd9" />
<img width="593" height="430" alt="screenshot" src="https://github.com/user-attachments/assets/40024678-eeae-4ac6-89ab-b7a52f9e2c55" />


## Szenario 3: Bewertung ändern

Als Kunde von MarketMate kann ich meine Bewertung ändern.

| Schritt | Aktion                                                  | Erwartetes Ergebnis                                                                 | OK/NOK | URL                                           | Link zum Issue |
| ------- | ------------------------------------------------------- | ----------------------------------------------------------------------------------- | ------ | --------------------------------------------- | -------------- |
| 1       | Gehe zur Homepage von MarketMate                                       | Homepage erscheint                                                                  | OK     | https://grocerymate.masterschool.com/         |                |
| 2       | Gib "Birchwood Quarter Pounders" in Suchleiste ein      | Du wirst auf Produktseite weitergeleitet                                            | OK     | /product/66b3a57b3fd5048eacb479c8             |                |
| 3       | Klicke auf die 3 Punkte bei deiner Bewertung            | Auswahl "Edit" und "Delete" werden angezeigt                                        | OK     |                                               |                |
| 4       | Klicke auf "Edit"                                       | Fenster "Edit Review" erscheint                                                     | OK     |                                               |                |
| 5       | Ändere Anzahl an Sternen                                |                                                                                     |        |                                               |                |
| 6       | Klicke auf "Save changes"                               | Anzahl der Sterne in der Bewertung wurde geändert und der Durchschnitt angepasst   | OK     |                                               |                |


<img width="1323" height="800" alt="screenshot" src="https://github.com/user-attachments/assets/f2987fd1-de45-41be-b779-0773e5ebbca0" />
<img width="1324" height="795" alt="screenshot" src="https://github.com/user-attachments/assets/e6ccb091-91ae-4e9e-b3ff-d22047970997" />
<img width="1229" height="480" alt="screenshot" src="https://github.com/user-attachments/assets/c4778a9d-2c03-4d1c-a992-daa3ce20bd90" />
<img width="977" height="138" alt="screenshot" src="https://github.com/user-attachments/assets/45ba8a0d-c5a8-41cd-8247-66943a5ea503" />
<img width="412" height="381" alt="screenshot" src="https://github.com/user-attachments/assets/5450a0ad-33d7-40c6-b7f9-6e7513b0e613" />
<img width="413" height="382" alt="screenshot" src="https://github.com/user-attachments/assets/9ddbc3d8-5b11-4532-917f-b40e65a32e64" />
<img width="1226" height="472" alt="screenshot" src="https://github.com/user-attachments/assets/afcb46c9-2a9e-497d-b3df-3906ac3efe02" />


## Szenario 4: Altersverifikation beim Zugriff auf 18+ Kategorie

Auf MarketMate erscheint ein Pop-up zur Altersverifikation beim Zugriff auf die 18+ Kategorie.

| Schritt | Aktion                         | Erwartetes Ergebnis                          | OK/NOK | URL                                | Link zum Issue |
| ------- | ------------------------------ | -------------------------------------------- | ------ | ---------------------------------- | -------------- |
| 1       | Gehe zur Homepage von MarketMate              | Homepage erscheint                            | OK     | https://grocerymate.masterschool.com/ |                |
| 2       | Klicke auf "Shop"              | Altersverifikations-Pop-up erscheint         | OK     | /store                              |                |


<img width="1323" height="800" alt="image" src="https://github.com/user-attachments/assets/f2987fd1-de45-41be-b779-0773e5ebbca0" />
<img width="1321" height="790" alt="Bildschirmfoto 2026-05-06 um 01 53 29" src="https://github.com/user-attachments/assets/7f510f16-0a8b-46bd-a8e8-059355a7a739" />


## Szenario 5: Altersverifikation beim Zugriff auf 18+ Kategorie

Auf MarketMate erscheint ein Pop-up zur Altersverifikation beim Zugriff auf die 18+ Kategorie.

| Schritt | Aktion                                                                                              | Erwartetes Ergebnis                                                                                          | OK/NOK | URL                                | Link zum Issue |
| ------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | ------ | ---------------------------------- | -------------- |
| 1       | Gehe zur Homepage                                                                                   | Homepage erscheint                                                                                           | OK     | https://grocerymate.masterschool.com/ |                |
| 2       | Klicke auf "Shop"                                                                                   | Altersverifikations-Pop-up erscheint                                                                         | OK     | /store                              |                |
| 3       | Gib Geburtsdatum ein (heute: 18)                                                                    |                                                                                                              |        |                                      |                |
| 4       | Klicke auf "Confirm"                                                                                | Meldung erscheint: "You are of age. You can now view all products, even alcohol products." Zugriff auf 18+ Produkte gewährt. | OK     |                                      |                |


<img width="1323" height="800" alt="screenshot" src="https://github.com/user-attachments/assets/f2987fd1-de45-41be-b779-0773e5ebbca0" />
<img width="1321" height="790" alt="screenshot" src="https://github.com/user-attachments/assets/1402786b-8f31-4809-b8d0-c4dc22040dcd" />
<img width="549" height="154" alt="screenshot" src="https://github.com/user-attachments/assets/e1e6e5d4-5d9f-4d6e-a4ad-2eba7516c0d7" />
<img width="408" height="134" alt="screenshot" src="https://github.com/user-attachments/assets/5eb3c528-8cba-4a7c-9f3e-144e659f8ea1" />


## Szenario 6: Altersverifikation für 18+ Produkte

Auf MarketMate erscheint ein Pop-up zur Altersverifikation um Zugriff auf 18+ Produkte zu erhalten.

| Schritt | Aktion                                                                                              | Erwartetes Ergebnis                                                                                          | OK/NOK | URL                                | Link zum Issue |
| ------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | ------ | ---------------------------------- | -------------- |
| 1       | Gehe zur Homepage von MarketMate                                                                                   | Homepage erscheint                                                                                           | OK     | https://grocerymate.masterschool.com/ |                |
| 2       | Klicke auf "Shop"                                                                                   | Altersverifikations-Pop-up erscheint                                                                         | OK     | /store                              |                |
| 3       | Gib Geburtsdatum ein (heute: 17)                                                                    |                                                                                                              |        |                                      |                |
| 4       | Klicke auf "Confirm"                                                                                | Meldung erscheint: "You are underage. You can still browse the site, but you will not be able to view alcohol products." | OK     |                                      |                |


<img width="1323" height="800" alt="screenshot" src="https://github.com/user-attachments/assets/f2987fd1-de45-41be-b779-0773e5ebbca0" />
<img width="1321" height="790" alt="screenshot" src="https://github.com/user-attachments/assets/1402786b-8f31-4809-b8d0-c4dc22040dcd" />
<img width="548" height="152" alt="screenshot" src="https://github.com/user-attachments/assets/f6dea80e-c432-40ba-bfde-fe06b52ce85f" />
<img width="345" height="108" alt="screenshot" src="https://github.com/user-attachments/assets/8f80a79c-d44d-4f57-aaf7-eb527bd512db" />


## Szenario 7: Versandkosten unter Schwellenwert (Versand 5 €)

Wenn der Warenkorb unter dem Versandfreigrenzwert liegt, werden 5,00 € Versand berechnet.

| Schritt | Aktion                                             | Erwartetes Ergebnis                                                      | OK/NOK | URL                   | Link zum Issue |
| ------- | -------------------------------------------------- | ------------------------------------------------------------------------ | ------ | --------------------- | -------------- |
| 1       | Gehe zur Homepage von MarketMate                                  | Homepage erscheint                                                         | OK     | https://grocerymate.masterschool.com/ |                |
| 2       | Klicke auf "Shop"                                  | Du wirst zur Produktübersicht weitergeleitet                              | OK     | /store                |                |
| 3       | Fülle Warenkorb im Wert von 19,99 €                |                                                                          |        |                       |                |
| 4       | Klicke auf Warenkorb                               | Du wirst zum Checkout weitergeleitet; Warenwert 19,99 €, Versand 5,00 €, Total = 24,99 € | OK     | /checkout             |                |


<img width="1323" height="800" alt="screenshot" src="https://github.com/user-attachments/assets/f2987fd1-de45-41be-b779-0773e5ebbca0" />
<img width="1325" height="797" alt="screenshot" src="https://github.com/user-attachments/assets/f269eeb9-8f8d-4b04-b448-9f8870990c79" />
<img width="176" height="168" alt="screenshot" src="https://github.com/user-attachments/assets/5d4beaec-d0bb-4c84-bdc1-482495dddb6b" />
<img width="551" height="613" alt="screenshot" src="https://github.com/user-attachments/assets/baaf4966-ca13-4338-81b8-79a6548d527e" />


## Szenario 8: Versandkosten - Genau Schwellenwert 20,00 € (versandfrei)

Wenn der Warenkorb genau den Versandfreigrenzwert erreicht, ist der Versand kostenlos.

| Schritt | Aktion                                     | Erwartetes Ergebnis                                         | OK/NOK | URL                                         | Link zum Issue |
| ------- | ------------------------------------------ | ----------------------------------------------------------- | ------ | ------------------------------------------- | -------------- |
| 1       | Gehe zur Homepage von MarketMate           | Homepage erscheint                                            | OK     | https://grocerymate.masterschool.com/      |                |
| 2       | Klicke auf "Shop"                          | Du wirst zur Produktübersicht weitergeleitet                 | OK     | /store                                      |                |
| 3       | Fülle Warenkorb im Wert von 20,00 €        |                                                             |        |                                             |                |
| 4       | Klicke auf Warenkorb                        | Du wirst zum Checkout weitergeleitet; Warenwert 20,00 €, Versand 0,00 €, Total = 20,00 € | OK     | /checkout                                   |                |


<img width="1323" height="800" alt="screenshot" src="https://github.com/user-attachments/assets/f2987fd1-de45-41be-b779-0773e5ebbca0" />
<img width="1325" height="797" alt="screenshot" src="https://github.com/user-attachments/assets/f269eeb9-8f8d-4b04-b448-9f8870990c79" />
<img width="176" height="168" alt="screenshot" src="https://github.com/user-attachments/assets/5d4beaec-d0bb-4c84-bdc1-482495dddb6b" />
<img width="547" height="466" alt="screenshot" src="https://github.com/user-attachments/assets/ce56bfed-260c-49de-8c50-b3c83713d72f" />


## Szenario 9: Echtzeit‑Änderung beim Mengenupdate

Wenn der Warenwert in Echtzeit unter die Versandfreigrenze sinkt, ändern sich die Versandkosten entsprechend.

| Schritt | Aktion                                                     | Erwartetes Ergebnis                                                                 | OK/NOK | URL        | Link zum Issue |
| ------- | ---------------------------------------------------------- | ----------------------------------------------------------------------------------- | ------ | ---------- | -------------- |
| 1       | Gehe zur Homepage von MarketMate                           | Homepage erscheint                                                                  | OK     | https://grocerymate.masterschool.com/ |                |
| 2       | Klicke auf "Shop"                                          | Du wirst zur Produktübersicht weitergeleitet                                        | OK     | /store     |                |
| 3       | Fülle Warenkorb über Wert von 20,00 €                        |                                                                                     |        |            |                |
| 4       | Klicke auf Warenkorb                                        | Du wirst zum Checkout weitergeleitet; Warenwert 29,37 €, Versand 0,00 €, Total = 29,37 € | OK     | /checkout  |                |
| 5       | Verringere Warenwert auf unter 20,00 € | Versandkosten wechseln von 0,00 € auf 5,00 €; Total wird entsprechend angepasst; Warenwert + 5,00 € Versand) | NOK    | /checkout  |                |


<img width="1323" height="800" alt="screenshot" src="https://github.com/user-attachments/assets/f2987fd1-de45-41be-b779-0773e5ebbca0" />
<img width="1325" height="797" alt="screenshot" src="https://github.com/user-attachments/assets/f269eeb9-8f8d-4b04-b448-9f8870990c79" />
<img width="176" height="168" alt="screenshot" src="https://github.com/user-attachments/assets/5d4beaec-d0bb-4c84-bdc1-482495dddb6b" />
<img width="550" height="461" alt="screenshot" src="https://github.com/user-attachments/assets/86c8b82c-41bf-4ff4-92d0-9bcc11cd7b39" />
<img width="546" height="464" alt="screenshot" src="https://github.com/user-attachments/assets/26b746be-6f0e-4f35-9f77-b6b80ce0e91c" />
