# Aufgabe 5: Probleme und Ausnahmen in BPMN 2.0 modellieren

## Zeitrahmen: 2 Lektionen

## Ziele:

Die Lernenden sollen für einen Geschäftsprozess im Happy Path Probleme und Ausnahmen korrekt in BPMN 2.0 modellieren können.

## Aufgabenstellung:

Nachfolgender BPMN Prozess im Happy Path dient als Basis:

Modelliert zuerst diesen Prozess im Happy Path in Camunda oder Adonis NP. Fügt als nächstes das Handling für die nachfolgenden Probleme im selben Diagramm hinzu:
Die Bestelldaten sind unvollständig.
Die Bestelldaten sind unleserlich.
Die Kundennummer ist falsch.
Der Kunde besitzt keine ausreichende Bonität.
Der bestellte Artikel ist nicht lieferbar.
Das Versenden der Auftragsbestätigung schlägt fehl.

### Hinweise

Verwendet für jedes Problem entweder ein angeheftetes Fehlerereignis an der Aufgabe, oder ein XOR-Gateway nach der Aufgabe wie in der nachfolgenden Abbildung dargestellt:
Außer bei Problem Nr. 6 sollten alle Probleme zur Ablehnung des Auftrags führen.
Nutzt nur ein Modell für die gesamte Aufgabe.
Ihr müsst die ausgelösten Fehlerereignisse nicht modellieren. Geht davon aus, dass die Fehler innerhalb der Aufgabe entstehen und kümmert euch nur um die Fehlerbehandlung.

Abgabe: Screenshot von euer Lösung (als Bild oder als PDF, keine .bmpn Datei!).
