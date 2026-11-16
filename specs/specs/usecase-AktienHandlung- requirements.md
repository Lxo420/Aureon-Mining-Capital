# Use Case: AktienHandlung

<!-- Beschreiben Sie, WAS passiert, nicht WIE es technisch umgesetzt wird.
     Akzeptanzkriterien (Given/When/Then) ergänzen Sie erst in der Vorbereitung auf L4. -->

- Name: Aktien handeln
- Zusammenfassung: Kund:innen können über die Plattform Aktien von Gold- und Silberminenunternhemen virtuell kaufen und verkaufen. Dabei kömnen sie aktuelle Kursdaten einsehen, die gewünschte Stückzahl festlegen und Ihre Aktien anschließend in Ihrem Portfolio verwalten.
  - Standardablauf:
    1. Kund:in meldet sich an und klickt auf „Aktien handeln“.
    2. System zeigt eine Übersicht der verfügbaren Minenaktien mit aktuellen Kursdaten.
    3. Kund:in wählt eine Aktie aus und sieht deren Kursverlauf sowie Unternehmensinformationen.
    4. Kund:in entscheidet sich zwischen „Kaufen“ und „Verkaufen“.
    5. Kund:in gibt die gewünschte Stückzahl ein.
    6. System berechnet den Gesamtwert der Transaktion und zeigt die verfügbaren finanziellen Mittel beziehungsweise Aktienbestände an.
    7. Kund:in überprüft die Angaben und bestätigt die Transaktion.
    8. System führt die virtuelle Transaktion aus und aktualisiert das Portfolio sowie das verfügbare Guthaben.
    9. Kund:in erhält eine Bestätigung und kann die Transaktion im persönlichen Portfolio einsehen.
  - Erweiterungen:
    - 1a. Kund:in ist nicht angemeldet: System leitet zur Loginseite weiter.
    - 2a. Es sind keine Aktien verfügbar: System zeigt „Aktuell sind keine Aktien zum Handel verfügbar.“
    - 5a. Kund:in gibt eine ungültige Stückzahl ein: System zeigt eine Fehlermeldung und fordert zur Korrektur auf.
    - 6a. Das verfügbare Guthaben reicht für den Kauf nicht aus: System zeigt „Nicht genügend Guthaben vorhanden.“
    - 6b. Kund:in möchte mehr Aktien verkaufen, als im Portfolio vorhanden sind: System verhindert die Transaktion.
    - 7a. Kund:in bricht die Transaktion ab: System kehrt zur Aktienübersicht zurück, ohne Änderungen zu speichern.
    - 8a. Die Transaktion kann nicht gespeichert werden: System zeigt eine Fehlermeldung und verändert weder Guthaben noch Aktienbestand.

- Akteur: Registrierte/r Kund:in
- Auslösendes Ereignis: Kund:in möchte in eine bestimmte Gold- oder Silberminenaktie investieren oder bereits vorhandene Aktien verkaufen.

## Daten

- **Aktie:** Pflicht, Auswahl einer verfügbaren Gold- oder Silberminenaktie aus der Aktienübersicht.
- **Aktienkurs:** Wird vom System angezeigt: positiver Geldbetrag in Euro mit zwei Nachkommastellen.
- **Kursverlauf:** Wird vom System angezeigt: historische Kursentwicklung der ausgewählten Aktie.
- **Transaktionsart:** Pflicht, Auswahl zwischen „Kaufen“ und „Verkaufen“.
- **Anzahl Aktien:** Pflicht, ganze Zahl von 1 bis 10.000.
- **Gesamtbetrag:** Wird vom System automatisch berechnet (Aktienkurs × Anzahl Aktien) und in Euro angezeigt.
- **Verfügbares Guthaben:** Wird vom System angezeigt: beim Kauf darf der Gesamtbetrag das verfügbare Guthaben nicht überschreiten.
- **Aktienbestand:** Wird vom System angezeigt: beim Verkauf darf die angegebene Stückzahl den vorhandenen Aktienbestand nicht überschreiten.
- **Transaktionsbestätigung:** Pflicht, Kund:in muss die Transaktion über den Button „Kauf bestätigen“ oder „Verkauf bestätigen“ ausdrücklich bestätigen.
- **Transaktionshistorie:** Das System speichert die ausgewählte Aktie, Transaktionsart, Stückzahl, Ausführungskurs, Gesamtbetrag sowie Datum und Uhrzeit der Transaktion.

## Screens

<!-- Zwei bis vier Wireframes (Mobile) aus Figma, als PNG nach specs/figma/ exportiert.
     Darunter als Text: Welcher Screen gehört zu welchen Schritten? Keine Anmerkungen ins Bild. -->

![Termin wählen](figma/pickup-1-termin.png)

![Leergut angeben](figma/pickup-2-leergut.png)

- Termin wählen: Schritte 1–2 und 2a
- Leergut angeben: TODO
- TODO

## Out of scope

- Die Bezahlung des Pfands an die Kund:in. Sie wird bei der Abholung bar erledigt.
- TODO
