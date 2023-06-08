# Aufgabe 4: Geschäftsprozess mit BPMN 2.0 vollständig dokumentieren

## Zeitrahmen: 2 Lektionen

## Ziele:

Die Lernenden sollen aus einem Text Geschäftsprozesse vollständig und syntaktisch korrekt in BPMN 2.0 modellieren können.
Die Lernenden sollen Pools und Lanes sowie den dazugehörigen Nachrichtenfluss zwischen den Pools korrekt modellieren können.

## Aufgabenstellung:

Wählt NUR EINE (GP1 oder GP2) der unten aufgeführten Aufgaben aus und modelliert basierend auf dem beschriebenen Text ein vollständiges und korrektes Kollaborationsdiagramm in BPMN 2.0. Für die Modellierung könnt ihr entweder Camunda oder Adonis NP verwenden.

Abgabe: Screenshot von eurem vollständigen Kollaborationsdiagramm (als Bild oder als PDF, keine .bmpn Datei!).

## GP 1: Selbstbedienungsrestaurant

### Hintergrund

In einem Selbstbedienungsrestaurant geht es chaotisch zu. Die Kunden geben ihre Bestellungen an der Kasse auf und erhalten ihre Mahlzeiten auf Zuruf von der Küche. Da sich das Restaurant grosser Beliebtheit erfreut, müssen die Prozesse an die steigenden Besucherzahlen angepasst werden. Die Gäste des Restaurants sollen für Ihre Bestellungen nur noch Kontakt mit einem Mitarbeiter haben. Der Koch soll sich ausschließlich auf die Zubereitung der Mahlzeiten konzentrieren. Es werden Pieper eingeführt, die den Gästen signalisieren, wenn Ihre Bestellungen fertig zubereitet sind.

### Aufgabe: Modellieren Sie folgenden optimierten Prozess

Ein Gast betritt das Restaurant, wenn er Hunger verspürt. Er wählt sich aus dem wechselnden Angebot ein Gericht aus und wartet, bis er an der Reihe ist. Daraufhin gibt er beim Angestellten seine Bestellung auf. Der Angestellte gibt anschließend die Bestellung in das Kassensystem ein und kassiert das Geld vom Gast. Wenn der Gast bezahlt hat, stellt der Angestellte einen Pieper ein und übergibt ihn an den Gast mit den Worten "wenn sich der Pieper meldet, ist ihr Essen fertig".

Danach informiert der Angestellte den Koch über die bestellte Mahlzeit. Der Koch bereitet die Mahlzeit zu und stellt sie danach in die Durchreiche zum Angestellten. Nachdem er die Mahlzeit in die Durchreiche gestellt hat, informiert der Koch den Angestellten darüber.

Sobald der Angestellte weiß, dass das Essen fertig ist löst er den Pieper des Gastes aus. So erfährt der Gast, dass sein Essen abholbereit ist. Er kann sein Essen abholen und anschließend die Mahlzeit verzehren. Sobald der Gast an der Ausgabe erscheint, übergibt ihm der Angestellte das Essen. Sollte ein Gast einmal nicht auf den Pieper reagieren, ruft der Angestellte den Gast nach 5 Minuten aus – notfalls auch mehrere Male hintereinander.

#### Hinweis

Verwenden Sie für die Modellierung 3 verschiedene Pools:
Gast (Nahrungsaufnahme)
Angestellter (Bestellungsbearbeitung)
Koch (Mahlzeitenzubereitung)

## GP 2: IT-Support Prozess

Stellen Sie sich vor, Sie sind für die Modellierung von Prozessen bei einem IT-Service-Dienstleister zuständig. Ihre Aufgabe ist die Erhebung und Modellierung des IST-Prozesses "IT Support 1st Level durchführen 0.01" in einem Workshop gemeinsam mit dem Prozessmanager und ausgewählten Prozessbeteiligten. Nach Angaben der Beteiligten stellt sich der Ablauf wie folgt dar:

Der Prozess startet mit dem Eingang eines Anrufs vom Kunden (Hinweis: den Kunden als Black-Box Pool modellieren, dessen Prozessdetails unbekannt sind). Der Service-Desk Mitarbeiter nimmt den Anruf entgegen. Anschliessend fragt er nach der Kundennummer und prüft die Kundendaten im CRM System. Tragen Sie bitte die ergänzende Information, dass es im CRM-System nach der Kundennummer gesucht wird und den Wartungsvertrag überprüft wird (entweder als Beschreibung oder als alleinstehende Textanmerkung). Falls der Kunde keinen Wartungsvertrag abgeschlossen hat, was eine Voraussetzung für die Anruf-Bearbeitung ist, wird der Anrufende diesbezüglich informiert und der Anruf beendet. Falls es sich um einen Wartungskunden handelt, fragt der Servicedesk-Mitarbeiter nach den Details.

Der Servicedesk-Mitarbeiter stellt ein Service-Ticket im Ticket-System mit den gemeldeten Details ein und kategorisiert die Anfrage. Abhängig von der Kategorie (neue Software-Anforderung oder Störung) verzweigt sich hier der Prozess. Wenn es um eine neue Anforderung geht, leitet er den Anruf an den Kundenbetreuer weiter (Hinweis: Kundenbetreuer ist ein Black-Box-Pool) und beendet damit den Prozess.

Wenn es sich um eine Störung handelt, führt der Servicedesk-Mitarbeiter eine erste Analyse durch. Falls keine Lösung bekannt ist, leitet er den Anruf an 2nd Level Support weiter und beendet damit den Prozess (Hinweis: 2nd Level Support ist ein Black-Box Pool). Falls eine Lösung bekannt ist, wird diese dem Kunden mitgeteilt. An der Stelle wartet der Servicedesk-Mitarbeiter auf Input des Kunden bezüglich der Ergebnisse der Fehlerbehebung. Falls der Kunde meldet, dass die Störung behoben werden kann, schliesst der Servicedesk-Mitarbeiter das Ticket und beendet damit den Prozess. Falls die Störung nicht behoben werden konnte, leitet der Servicedesk-Mitarbeiter den Anruf an 2nd Level Support und beendet damit den Prozess.
