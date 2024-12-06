+++
date = '2024-12-06'
draft = true
title = 'Datenbank Normalisierung'
+++
Normalisierung ist der Prozess einen Datensatz in eine Normalform zu bringen.

## 1. Normalform

Ein Modell ist in der 1NF, wenn:

- Alle **Attribute atomar** sind – Es gibt keine Mehrfachwerte in einer Zelle

{{% expand title="**Beispiel Ausgangslage, nicht in 1NF**:" %}}| Kundennummer (PK) | Kunde                                          | Artikelnummer (PK) | Vermerk                                                       |
| ----------------- | ---------------------------------------------- | ------------------ | ------------------------------------------------------------- |
| 101               | Megabit GmbH, Zusestr., Nr. 1, 86161, Augsburg | 801                | Blu Ray DVD Laufwerk, 8 Stück, 1.600 €, 20.11.2023, 8:02 Uhr  |
| 101               | Megabit GmbH, Zusestr., Nr. 1, 86161, Augsburg | 802                | 2 TB SSD, 2 Stück, 300 €, 20.11.2023, 8:34 Uhr                |
| 102               | Phase AG, Roboweg, Nr. 3, 86166, Augsburg      | 802                | 2 TB SSD, 4 Stück, 600 €, 21.11.2023, 9:45 Uhr                |
| 102               | Phase AG, Roboweg, Nr. 3, 86166, Augsburg      | 801                | Blue Ray DVD Laufwerk, 6 Stück, 1.200 €, 21.11.2023, 9:56 Uhr |
| 103               | Krause UG, Chipallee, Nr. 7, 86356, Neusäß     | 802                | 2 TB SSD, 10 Stück, 1.500 €, 21.11.2023, 11:33 Uhr            |{{% /expand %}}

**Probleme**:

- Die Spalten „Name“ und „Vermerk“ enthalten mehrere Werte in einer Zeile, was gegen die 1NF verstößt.

{{% expand title="**Lösung 1NF**:" %}}| KundenNr (PK) | Kundennamen  | Strasse   | HausNR | PLZ   | Ort      | Artikel-Nr (PK) | Artikel               | Anzahl | Preis   | Zeit             |
| ------------- | ------------ | --------- | ------ | ----- | -------- | --------------- | --------------------- | ------ | ------- | ---------------- |
| 101           | Megabit GmbH | Zusestr.  | 1      | 86161 | Augsburg | 801             | Blue Ray DVD Laufwerk | 8      | 1.600 € | 2023.11.20 08:02 |
| 101           | Megabit GmbH | Zusestr.  | 1      | 86161 | Augsburg | 802             | 2 TB SSD              | 2      | 300 €   | 2023.11.20 09:45 |
| 102           | Phase AG     | Roboweg   | 3      | 86161 | Augsburg | 802             | 2 TB SSD              | 4      | 600 €   | 2023.11.21 09:45 |
| 102           | Phase AG     | Roboweg   | 3      | 86161 | Augsburg | 801             | Blue Ray DVD Laufwerk | 6      | 1.200 € | 2023.11.21 09:56 |
| 103           | Krause UG    | Chipallee | 7      | 86356 | Neusäß   | 802             | 2 TB SSD              | 10     | 1.500 € | 2023.11.21 11:33 |{{% /expand %}}

Anmerkung:

Was als atomar gilt hängt davon ab, wie die Daten genutzt werden. Da der Name „Megabit“ i.d.R. zusammen mit der Rechtsform „GmbH“ genutzt wird gibt es keinen Grund diese Daten gesondert zu speichern.

Datum und Zeit werden in der Praxis oft Zusammen benötigt und in Datenbanken auch mit der Zeitzone zusammen gespeichert. Wären die Daten einzeln gespeichert wäre es sehr aufwendig mit Sommer- und Winterzeit und Zeitzonen zu arbeiten.

## 2. Normalform

Ein Modell ist in der 2NF, wenn:

- Das Modell in der ersten Normalform ist
- Keine partielle Abhängigkeit zwischen einem Nicht-Schlüsselattribut und einem Teil eines zusammengesetzten Schlüssels besteht.

