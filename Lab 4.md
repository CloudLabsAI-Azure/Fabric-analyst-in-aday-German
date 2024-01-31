# Inhalt

- Einführung

- Dataflow Gen2

   - Aufgabe 1: Snowflake-Abfragen in Dataflow kopieren

   - Aufgabe 2: Verbindung zu Snowflake erstellen

    - Aufgabe 3: Datenziel für die Abfragen „Supplier“ und „PO“ konfigurieren

    - Aufgabe 4: Snowflake-Dataflow umbenennen und veröffentlichen

    - Aufgabe 5: Dataverse-Abfragen in Dataflow kopieren

    - Aufgabe 6: Verbindung zu Dataverse erstellen

    - Aufgabe 7: Datenziel für die Abfrage „Customer“ erstellen

    - Aufgabe 8: Dataverse-Dataflow veröffentlichen und umbenennen

    - Aufgabe 9: SharePoint-Abfragen in Dataflow kopieren

    - Aufgabe 10: Verbindung zu SharePoint erstellen

    - Aufgabe 11: Datenziel für die Abfrage „People“ konfigurieren

    - Aufgabe 12: SharePoint-Dataflow veröffentlichen und umbenennen

## Referenzen

Bei unserem Anwendungsfall befinden sich die Lieferantendaten in Snowflake, die Kundendaten in Dataverse und die Mitarbeiterdaten in SharePoint. Alle diese Datenquellen werden zu verschiedenen Zeiten aktualisiert. Um die Anzahl der Datenaktualisierungen von Dataflows zu verringern, erstellen wir für jede dieser Datenquellen individuelle Dataflows.
Hinweis: Ein einziger Dataflow berücksichtigt dabei mehrere Datenquellen.

**Inhalt dieser Übung:**
- Mit Dataflow Gen2 eine Verbindung zu Snowflake herstellen und Daten im Lakehouse erfassen
- Mit Dataflow Gen2 eine Verbindung zu SharePoint herstellen und Daten im Lakehouse erfassen
- Mit Dataflow Gen2 eine Verbindung zu Dataverse herstellen und Daten im Lakehouse erfassen

## Dataflow Gen2

### Aufgabe 1: Snowflake-Abfragen in Dataflow kopieren
1. Wechseln wir zurück zum Fabric-Arbeitsbereich FAIAD_<Benutzername>, den Sie in Aufgabe 8 von Übung 2 erstellt haben.
2. Wählen Sie im Menü oben die Option Neu -> Dataflow Gen2 aus.


 Sie werden zur Dataflow-Seite weitergeleitet. Nachdem Sie Dataflow nun kennen, kopieren Sie die Abfragen aus Power BI Desktop in Dataflow.
3. Öffnen Sie, sofern noch nicht geschehen, auf dem Desktop Ihrer Übungsumgebung im Ordner Report die Datei FAIAD.pbix.
4. Wählen Sie im Menüband Start > Daten transformieren aus. Das Power Query-Fenster wird geöffnet.
5. Das Power Query-Fenster wird geöffnet. Wählen Sie links unter dem Ordner „SnowflakeData“ mit Strg+Auswahl oder „Umschalt+Auswahl“ die folgenden Abfragen aus:

   a. SupplierCategories
   
   b. Suppliers
   
   c. Supplier
   
   d. PO
   
   e. PO Line Items

6. Klicken Sie mit der rechten Maustaste, und wählen Sie Kopieren aus.
7. Navigieren Sie zurück zum Browser.
8. Wählen Sie im Bereich Dataflow den mittleren Bereich aus, und drücken Sie Strg+V (das Einfügen mittels Rechtklick ist derzeit nicht möglich).

