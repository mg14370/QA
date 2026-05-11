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


<img width="1323" height="800" alt="587948835-f2987fd1-de45-41be-b779-0773e5ebbca0" src="https://github.com/user-attachments/assets/3e293c1c-7ef1-4b78-b5ad-f49e17c971ee" />
<img width="1324" height="795" alt="587949631-e6ccb091-91ae-4e9e-b3ff-d22047970997" src="https://github.com/user-attachments/assets/285f731b-5d8c-4dc3-a56c-88a758283696" />
<img width="876" height="801" alt="587951316-381e0bfa-0fbe-4d5e-8647-e023b9130cd9" src="https://github.com/user-attachments/assets/e184838e-bc04-4727-a78e-e8fc6b93b7b1" />
<img width="593" height="430" alt="587964534-40024678-eeae-4ac6-89ab-b7a52f9e2c55" src="https://github.com/user-attachments/assets/6882332a-c7b2-480c-89a4-d7f2c24815ca" />


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


<img width="1323" height="800" alt="587948835-f2987fd1-de45-41be-b779-0773e5ebbca0" src="https://github.com/user-attachments/assets/57540d61-bb13-42c1-a387-1f89dd0ac71f" />
<img width="1324" height="795" alt="587949631-e6ccb091-91ae-4e9e-b3ff-d22047970997" src="https://github.com/user-attachments/assets/66e5acb9-5aa9-4563-b39a-438e16ae1eba" />
<img width="1229" height="480" alt="587976681-c4778a9d-2c03-4d1c-a992-daa3ce20bd90" src="https://github.com/user-attachments/assets/4b26998c-69fe-4058-bdb3-cc08df64283e" />
<img width="977" height="138" alt="587977059-45ba8a0d-c5a8-41cd-8247-66943a5ea503" src="https://github.com/user-attachments/assets/9c6a80b4-e2e0-437f-92aa-427f4b00fc36" />
<img width="412" height="381" alt="587977117-5450a0ad-33d7-40c6-b7f9-6e7513b0e613" src="https://github.com/user-attachments/assets/d81d7f74-2119-401b-8b80-3a6bff512739" />
<img width="413" height="382" alt="587978158-9ddbc3d8-5b11-4532-917f-b40e65a32e64" src="https://github.com/user-attachments/assets/cc6ff413-69fb-43bf-8992-b9b94b116905" />
<img width="1226" height="472" alt="587977351-afcb46c9-2a9e-497d-b3df-3906ac3efe02" src="https://github.com/user-attachments/assets/c5197916-4493-44f4-a27f-fbfe3281ee0e" />


## Szenario 4: Altersverifikation beim Zugriff auf 18+ Kategorie

Auf MarketMate erscheint ein Pop-up zur Altersverifikation beim Zugriff auf die 18+ Kategorie.

| Schritt | Aktion                                                                 | Erwartetes Ergebnis                                                                                                        | OK/NOK | URL                                           | Link zum Issue |
| ------- | ---------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | ------ | --------------------------------------------- | -------------- |
| 1       | Gehe zur Homepage                                                      | Homepage erscheint                                                                                                         | OK     | https://grocerymate.masterschool.com/         |                |
| 2       | Klicke auf "Shop"                                                      | Altersverifikations-Pop-up erscheint                                                                                        | OK     | /store                                        |                |
| 3       | Klicke auf "Confirm" ohne Eingaben                                     | Meldung erscheint: "You are underage. You can still browse the site, but you will not be able to view alcohol products." Zugriffsblock auf Alkoholprodukte (nur Browsen möglich) | OK     |                                               |                |


<img width="1323" height="800" alt="587948835-f2987fd1-de45-41be-b779-0773e5ebbca0" src="https://github.com/user-attachments/assets/443698f0-e812-4da5-a7b3-45e934c8b980" />
<img width="1321" height="790" alt="587995399-7f510f16-0a8b-46bd-a8e8-059355a7a739" src="https://github.com/user-attachments/assets/9f938b75-a3bf-435c-a4f5-5ec8d9ca59d0" />
<img width="345" height="108" alt="588001912-8f80a79c-d44d-4f57-aaf7-eb527bd512db" src="https://github.com/user-attachments/assets/6f72fb2a-f715-496c-b631-0806ce0a7571" />


## Szenario 5: Altersverifikation beim Zugriff auf 18+ Kategorie

Auf MarketMate erscheint ein Pop-up zur Altersverifikation beim Zugriff auf die 18+ Kategorie.

| Schritt | Aktion                                                                                              | Erwartetes Ergebnis                                                                                          | OK/NOK | URL                                | Link zum Issue |
| ------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | ------ | ---------------------------------- | -------------- |
| 1       | Gehe zur Homepage                                                                                   | Homepage erscheint                                                                                           | OK     | https://grocerymate.masterschool.com/ |                |
| 2       | Klicke auf "Shop"                                                                                   | Altersverifikations-Pop-up erscheint                                                                         | OK     | /store                              |                |
| 3       | Gib Geburtsdatum 06.05.2008 ein (heute: 18)                                                                    |                                                                                                              |        |                                      |                |
| 4       | Klicke auf "Confirm"                                                                                | Meldung erscheint: "You are of age. You can now view all products, even alcohol products." Zugriff auf 18+ Produkte gewährt. | OK     |                                      |                |


<img width="1323" height="800" alt="587948835-f2987fd1-de45-41be-b779-0773e5ebbca0" src="https://github.com/user-attachments/assets/65ef82dd-b119-4839-b152-30325f4c22b0" />
<img width="1321" height="790" alt="587995399-7f510f16-0a8b-46bd-a8e8-059355a7a739" src="https://github.com/user-attachments/assets/0689bc72-142b-4d96-b1f5-a3f6c764e1e1" />
<img width="549" height="154" alt="588045717-e1e6e5d4-5d9f-4d6e-a4ad-2eba7516c0d7" src="https://github.com/user-attachments/assets/9baeeeed-088b-418a-b9d8-a31a42893dc3" />
<img width="408" height="134" alt="588046324-5eb3c528-8cba-4a7c-9f3e-144e659f8ea1" src="https://github.com/user-attachments/assets/cf5735be-9c1b-416a-8e8b-6b6fb7b9220d" />


## Szenario 6: Altersverifikation für 18+ Produkte

Auf MarketMate erscheint ein Pop-up zur Altersverifikation um Zugriff auf 18+ Produkte zu erhalten.

| Schritt | Aktion                                                                                              | Erwartetes Ergebnis                                                                                          | OK/NOK | URL                                | Link zum Issue |
| ------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | ------ | ---------------------------------- | -------------- |
| 1       | Gehe zur Homepage von MarketMate                                                                                   | Homepage erscheint                                                                                           | OK     | https://grocerymate.masterschool.com/ |                |
| 2       | Klicke auf "Shop"                                                                                   | Altersverifikations-Pop-up erscheint                                                                         | OK     | /store                              |                |
| 3       | Gib Geburtsdatum 07.05.2008 ein (heute: 17)                                                                     |                                                                                                              |        |                                      |                |
| 4       | Klicke auf "Confirm"                                                                                | Meldung erscheint: "You are underage. You can still browse the site, but you will not be able to view alcohol products." | OK     |                                      |                |


<img width="1323" height="800" alt="587948835-f2987fd1-de45-41be-b779-0773e5ebbca0" src="https://github.com/user-attachments/assets/833d6f4a-8e7b-4b0a-87b6-d3ab79f68737" />
<img width="1321" height="790" alt="587995399-7f510f16-0a8b-46bd-a8e8-059355a7a739" src="https://github.com/user-attachments/assets/155a75e3-0e1d-4500-9f91-e75af5f64a53" />
<img width="548" height="152" alt="588047627-f6dea80e-c432-40ba-bfde-fe06b52ce85f" src="https://github.com/user-attachments/assets/1d80f291-35d3-463c-8762-2fa4ea278f69" />
<img width="345" height="108" alt="588001912-8f80a79c-d44d-4f57-aaf7-eb527bd512db" src="https://github.com/user-attachments/assets/6f72fb2a-f715-496c-b631-0806ce0a7571" />


## Szenario 7: Versandkosten unter Schwellenwert (Versand 5 €)

Wenn der Warenkorb unter dem Versandfreigrenzwert liegt, werden 5,00 € Versand berechnet.

| Schritt | Aktion                                             | Erwartetes Ergebnis                                                      | OK/NOK | URL                   | Link zum Issue |
| ------- | -------------------------------------------------- | ------------------------------------------------------------------------ | ------ | --------------------- | -------------- |
| 1       | Gehe zur Homepage von MarketMate                                  | Homepage erscheint                                                         | OK     | https://grocerymate.masterschool.com/ |                |
| 2       | Klicke auf "Shop"                                  | Du wirst zur Produktübersicht weitergeleitet                              | OK     | /store                |                |
| 3       | Fülle Warenkorb im Wert von 19,99 €                |                                                                          |        |                       |                |
| 4       | Klicke auf Warenkorb                               | Du wirst zum Checkout weitergeleitet; Warenwert 19,99 €, Versand 5,00 €, Total = 24,99 € | OK     | /checkout             |                |


<img width="1323" height="800" alt="587948835-f2987fd1-de45-41be-b779-0773e5ebbca0" src="https://github.com/user-attachments/assets/da0d6dae-9d6a-4824-bfb6-4cadbc98d3b8" />
<img width="1325" height="797" alt="588038098-f269eeb9-8f8d-4b04-b448-9f8870990c79" src="https://github.com/user-attachments/assets/4ec393e6-0bea-4c47-ad1e-47a7fd3389c9" />
<img width="176" height="168" alt="588048444-5d4beaec-d0bb-4c84-bdc1-482495dddb6b" src="https://github.com/user-attachments/assets/db9399dd-c850-4be6-a8d6-ae214e5738e7" />
<img width="551" height="613" alt="588038513-baaf4966-ca13-4338-81b8-79a6548d527e" src="https://github.com/user-attachments/assets/508cf820-540b-4df2-a758-0dc689e28ef8" />


## Szenario 8: Versandkosten - Genau Schwellenwert 20,00 € (versandfrei)

Wenn der Warenkorb genau den Versandfreigrenzwert erreicht, ist der Versand kostenlos.

| Schritt | Aktion                                     | Erwartetes Ergebnis                                         | OK/NOK | URL                                         | Link zum Issue |
| ------- | ------------------------------------------ | ----------------------------------------------------------- | ------ | ------------------------------------------- | -------------- |
| 1       | Gehe zur Homepage von MarketMate           | Homepage erscheint                                            | OK     | https://grocerymate.masterschool.com/      |                |
| 2       | Klicke auf "Shop"                          | Du wirst zur Produktübersicht weitergeleitet                 | OK     | /store                                      |                |
| 3       | Fülle Warenkorb im Wert von 20,00 €        |                                                             |        |                                             |                |
| 4       | Klicke auf Warenkorb                        | Du wirst zum Checkout weitergeleitet; Warenwert 20,00 €, Versand 0,00 €, Total = 20,00 € | OK     | /checkout                                   |                |


<img width="1323" height="800" alt="587948835-f2987fd1-de45-41be-b779-0773e5ebbca0" src="https://github.com/user-attachments/assets/e0c283b8-141d-41b0-85cc-892063805041" />
<img width="1325" height="797" alt="588038098-f269eeb9-8f8d-4b04-b448-9f8870990c79" src="https://github.com/user-attachments/assets/df641076-0580-4d9a-ac8e-b33691cb8a09" />
<img width="176" height="168" alt="588048444-5d4beaec-d0bb-4c84-bdc1-482495dddb6b" src="https://github.com/user-attachments/assets/0257e4c2-fe00-41a2-88d7-25a893da0091" />
<img width="547" height="466" alt="588056473-ce56bfed-260c-49de-8c50-b3c83713d72f" src="https://github.com/user-attachments/assets/e43799f1-a209-4fc5-84cf-8b1e0d74accb" />


## Szenario 9: Echtzeit‑Änderung beim Mengenupdate

Wenn der Warenwert in Echtzeit unter die Versandfreigrenze sinkt, ändern sich die Versandkosten entsprechend.

| Schritt | Aktion                                                     | Erwartetes Ergebnis                                                                 | OK/NOK | URL        | Link zum Issue |
| ------- | ---------------------------------------------------------- | ----------------------------------------------------------------------------------- | ------ | ---------- | -------------- |
| 1       | Gehe zur Homepage von MarketMate                           | Homepage erscheint                                                                  | OK     | https://grocerymate.masterschool.com/ |                |
| 2       | Klicke auf "Shop"                                          | Du wirst zur Produktübersicht weitergeleitet                                        | OK     | /store     |                |
| 3       | Fülle Warenkorb über Wert von 20,00 €                        |                                                                                     |        |            |                |
| 4       | Klicke auf Warenkorb                                        | Du wirst zum Checkout weitergeleitet; Warenwert 29,37 €, Versand 0,00 €, Total = 29,37 € | OK     | /checkout  |                |
| 5       | Verringere Warenwert auf unter 20,00 € | Versandkosten wechseln von 0,00 € auf 5,00 €; Total wird entsprechend angepasst; Warenwert + 5,00 € Versand) | NOK    | /checkout  |                |


<img width="1323" height="800" alt="587948835-f2987fd1-de45-41be-b779-0773e5ebbca0" src="https://github.com/user-attachments/assets/ede25484-52c0-4853-a0d2-5cc264af3024" />
<img width="1325" height="797" alt="588038098-f269eeb9-8f8d-4b04-b448-9f8870990c79" src="https://github.com/user-attachments/assets/32418912-c3db-42a5-87ed-0be472bd4d38" />
<img width="176" height="168" alt="588048444-5d4beaec-d0bb-4c84-bdc1-482495dddb6b" src="https://github.com/user-attachments/assets/d2d0cd01-1112-43da-9e3f-6a7c100d3dc3" />
<img width="550" height="461" alt="588067313-86c8b82c-41bf-4ff4-92d0-9bcc11cd7b39" src="https://github.com/user-attachments/assets/2f98f4ef-43a3-492d-81d8-30c968b26ccc" />
<img width="546" height="464" alt="588067386-26b746be-6f0e-4f35-9f77-b6b80ce0e91c" src="https://github.com/user-attachments/assets/81d8acd4-867b-4f85-99b2-7b2d84ca77ef" />

