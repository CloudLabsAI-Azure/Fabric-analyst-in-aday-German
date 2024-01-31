![](./Media/7.1.png)

# Inhalt

- Einführung

- Power BI

    - Aufgabe 1: Bericht automatisch erstellen

    - Aufgabe 2: Standardtabellen (Metriken) ausblenden
    
    - Aufgabe 3: Hintergrund für einen neuen Bericht konfigurieren
    
    - Aufgabe 4: Dem Bericht eine Kopfzeile hinzufügen
    
    - Aufgabe 5: Dem Bericht KPIs hinzufügen
    
    - Aufgabe 6: Dem Bericht ein Liniendiagramm hinzufügen
    
    - Aufgabe 7: Spalte „Year“ in der Tabelle „Date“ konfigurieren
    
    - Aufgabe 8: Die Spalte „Short_Month_Name“ in der Tabelle „Date“ konfigurieren
    
    - Aufgabe 9: Liniendiagramm formatieren
    
    - Aufgabe 10: Neue Daten hinzufügen, um den Direct Lake-Modus zu simulieren

- Übungsumgebung bereinigen

- Referenzen

## Einführung 

Wir haben Daten aus verschiedenen Datenquellen in Lakehouse erfasst, eine Einführung in Lakehouse erhalten, ein Datenmodell erstellt und einen Aktualisierungsplan für die Datenquellen festgelegt. Jetzt erstellen wir einen Bericht.

Inhalt dieser Übung: 
- So erstellen Sie einen Bericht automatisch
- So erstellen Sie einen Bericht von einem leeren Canvas ausgehend
- So erkunden Sie den Direct Lake-Modus, in dem Daten automatisch aktualisiert werden

## Power BI

### Aufgabe 1: Bericht automatisch erstellen

Verwenden wir zunächst die Option „Bericht automatisch erstellen“. Und später in der Übung werden wir den Bericht, den wir in Power BI haben, neu erstellen.

1. Wir navigieren zurück zum **Fabric-Arbeitsbereich**, den Sie in der vorherigen Übung erstellt haben.
2. Sie befinden sich wahrscheinlich auf der Data Factory-Startseite. Wählen Sie unten links das **Data Factory-Symbol** aus.
3. Das Dialogfeld „Fabric-Funktionsbereich“ wird geöffnet. Wählen Sie **Power BI** aus. Sie werden zur **Power BI-Startseite** weitergeleitet.

    ![](./Media/7.2.png)
 
4. Wählen Sie **Neuer Bericht** aus dem oberen Menü aus.

    ![](./Media/7.3.png)
 
5. Sie werden zu **Erstellen Sie Ihren ersten Bericht** weitergeleitet. Dort sind Optionen verfügbar, um Daten manuell einzugeben und einen Bericht zu erstellen oder um ein veröffentlichtes semantisches Modell auszuwählen. In den vorherigen Übungen haben wir ein semantisches Modell erstellt. Lassen Sie uns das verwenden. Wählen Sie die Option **Veröffentlichtes Semantikmodell auswählen** aus.

    ![](./Media/7.4.png)
 
6. Die Seite „Ein in Ihrem Bericht zu verwendendes DataSet auswählen“ wird geöffnet. Beachten Sie, dass wir über vier Optionen verfügen. **Wählen Sie lh_FAIAD aus:**

    a. **lh_FAIAD:** Dies ist das Lakehouse mit dem DataSet, den wir erstellt haben und für den Bericht verwenden möchten.

    b. **Units by Supplier:** Dies ist das DataSet, das wir mit T-SQL erstellt haben.

    c. **DataflowsStagingWarehouse:** Dies ist das Staging Warehouse, das standardmäßig erstellt wird, das wir es nicht verwendet und keine Daten bereitgestellt haben.
    
    d. **DataflowsStagingLakehouse:** Dies ist das Staging Lakehouse, das standardmäßig erstellt wird, das wir es nicht verwendet und keine Daten bereitgestellt haben.

7. Klicken Sie auf den **Pfeil neben der Schaltfläche „Bericht automatisch erstellen“**. Beachten Sie, dass es zwei Optionen gibt: „Bericht automatisch erstellen“ und „Leeren Bericht erstellen“. Versuchen wir es mit der automatischen Erstellung. Wählen Sie daher **Bericht automatisch erstellen** aus.

    ![](./Media/7.5.png)

8. Power BI beginnt mit der automatischen Erstellung des Berichts. Beachten Sie, dass bei entsprechender Auswahl eine Option für die Vorauswahl verschiedener Daten vorhanden ist. Sobald der Bericht fertig ist, wird oben rechts auf dem Bildschirm ein Dialogfeld angezeigt. Wählen Sie **Bericht jetzt anzeigen** aus.

    ![](./Media/7.6.png)
 
**Prüfpunkt:** Sie erhalten einen Bericht, der wie im folgenden Screenshot aussieht. Es gibt einige KPIs und einige Trendvisualisierungen. Dies ist ein guter Ausgangspunkt, wenn Sie ein neues Modell analysieren und sofort starten müssen.

**Hinweis:** Im oberen Menü haben Sie die Möglichkeit, den Bericht zu bearbeiten oder einige der Daten als Tabellen anzuzeigen. Sehen Sie sich diese Optionen doch einmal genauer an.

9. Sobald Sie fertig sind, **reduzieren** Sie alle Tabellen im Abschnitt **Daten** rechts. Beachten Sie, dass wir fünf neue Tabellen haben, die nicht Teil des von uns erstellten Modells sind. Hierbei handelt es sich um Standardtabellen, die zur Analyse der Leistung hinzugefügt wurden. Wir werden diese in Kürze aus der Berichtsansicht entfernen.

10. Speichern wir diesen Bericht. Wählen Sie im oberen Menü **Speichern** aus.

11. Das Dialogfeld „Bericht speichern“ wird geöffnet. Geben Sie dem Bericht den Namen **rpt_Sales_Auto_Report**.

**Hinweis:** Wir stellen dem Berichtsnamen das Präfix „rpt“ voran, was für „Bericht“ steht.

12. Stellen Sie sicher, dass der Bericht unter **<Name Ihres Arbeitsbereichs>** gespeichert wird.

13. Wählen Sie **Speichern** aus.

    ![](./Media/7.7.png)

### Aufgabe 2: Standardtabellen (Metriken) ausblenden

Erstellen wir einen Bericht wie den in Power BI Desktop. Dazu beginnen wir mit einem leeren Canvas. Bevor wir mit der Erstellung eines Berichts beginnen, entfernen wir die Standardtabellen (siehe Screenshot oben) aus der Berichtsansicht. Dies erfolgt im Modellierungsabschnitt von Lakehouse.

1. Wählen Sie unten im linken Bereich das **Power BI-Symbol** aus. Das Dialogfeld „Fabric“ wird geöffnet.

2. Klicken Sie auf **Data Engineering**. Sie werden zur Startseite von Data Engineering weitergeleitet.

    ![](./Media/7.8.png)
 
3. Scrollen Sie nach unten zum Abschnitt **Schnellzugriff**.

4. Wählen Sie **lh_FAIAD -> SQL-Analyseendpunkt** aus. Wir befinden uns in der Datenansicht von Lakehouse.

5. Wählen Sie unten **im linken Bereich Modell** aus, um zur Modellansicht zu navigieren.

Beachten Sie, dass sich die Standardtabellen im Designcanvas befinden. (Sie müssen möglicherweise nach rechts oder unten scrollen, um sie anzuzeigen.)

![](./Media/7.9.png)

6. Klicken Sie mit der rechten Maustaste auf die Tabelle **long_running_queries**, und wählen Sie **In Berichtsansicht ausblenden** aus.

    ![](./Media/7.10.png)
 
7. Wählen Sie entsprechend die Option **In Berichtsansicht ausblenden** für die folgenden Tabellen aus:

    a. fabric_query_starting
    
    b. fabric_query_completed
    
    c. exec_requests_history
    
    d. frequently_run_queries

### Aufgabe 3: Hintergrund für einen neuen Bericht konfigurieren

1. Jetzt können wir einen neuen Bericht übe die Modellansicht erstellen. Wählen Sie im oberen Menü **Start -> Neuer Bericht** aus. Sie werden zum Power BI-Berichtscanvas in einem neuen Fenster/einer neuen Registerkarte in Ihrem Browser weitergeleitet.

    ![](./Media/7.11.png)
 
2. Öffnen Sie, sofern noch nicht geschehen, auf dem **Desktop** Ihrer Übungsumgebung im Ordner **Report** die Datei **FAIAD.pbix**.

Wir werden diesen Bericht als Referenz verwenden. Wir fügen zunächst den Canvashintergrund hinzu. Wir erstellen die Berichtskopfzeile, fügen einige KPIs hinzu und erstellen das Liniendiagramm „Verkäufe im Laufe der Zeit“. Aus Zeitgründen und davon ausgehend, dass Sie bereits Erfahrung mit der Erstellung von Visuals Power BI Desktop haben, werden wir nicht alle Visuals erstellen.

![](./Media/7.12.png)
 
3. Navigieren Sie zurück zum **Power BI-Canvas** in Ihrem Browser.

4. Wählen Sie im Visualisierungsbereich das 
**Symbol** für die **Formatseite** aus.

5. Erweitern Sie den **Abschnitt „Canvas-Hintergrund“** aus.

6. Wählen Sie **Durchsuchen** über die Option **Bild** aus. Das Dialogfeld „Datei-Explorer“ wird geöffnet.

7. Navigieren Sie auf dem **Desktop** Ihrer Übungsumgebung zum Ordner **Report**. 

8. Wählen Sie **Summary Background.png** aus.

9. Wählen Sie im Dropdownmenü **Bild anpassen** den Eintrag **Anpassen** aus.

10. Legen Sie die Transparenz auf **0 %** fest.

    ![](./Media/7.13.png)
 

### Aufgabe 4: Dem Bericht eine Kopfzeile hinzufügen

1. Wir fügen nun die Kopfzeile am oberen Rand hinzu. Wählen Sie im **Menü** die Option **Textfeld** aus.

2. Geben Sie **Fabrikam Company** als erste Zeile in das Textfeld ein.

3. Geben Sie als zweite Zeile **Sales Report** in das Textfeld ein.

4. Markieren Sie **Fabrikam Company**, und legen Sie **Schriftart** auf **Segoe UI** und **Schriftgröße** auf **18, Fett** fest.

5. Markieren Sie Sales Report, und legen Sie **Schriftart** auf **Segoe UI** und **Schriftgröße** auf **14** fest.

6. Erweitern Sie bei **ausgewähltem Textfeld** im Bereich „Format“ rechts die Option **Effekte**.

7. Verwenden Sie den Schieberegler **Hintergrund**, um ihn auf **Aus** festzulegen.

8. Passen Sie die Größe des **Textfelds so an, dass es in den oberen Rand passt**.

    ![](./Media/7.14.png)
 

### Aufgabe 5: Dem Bericht KPIs hinzufügen

1. Fügen wir nun Verkauf-KPI hinzu. Wählen Sie den **Leerraum** im Canvas aus, um den Fokus vom Textfeld zu entfernen.

2. Wählen Sie im **Abschnitt Visualisierungen** die Option **Mehrzeiliges Kartenvisual** aus.

3. Erweitern Sie im **Abschnitt „Daten“** die **Tabelle Sales**.

4. Wählen Sie **Kennzahl „Sales“** aus.

    ![](./Media/7.15.png)
 
5. Wenn das **mehrzeilige Kartenvisual ausgewählt ist**, wählen Sie das **Symbol „Visual formatieren“** im Abschnitt „Visualisierungen“ aus.

6. Erweitern Sie den Abschnitt **Kategoriebeschriftungen** aus.

7. Erhöhen Sie die **Schriftgröße** auf **14**.

8. Wählen Sie das **Dropdownmenü „Farbe“** aus. Das Dialogfeld „Farbpalette“ wird geöffnet.

9. Legen Sie den HEX-Wert auf **#004753** fest.

    ![](./Media/7.16.png)
 
10. Erweitern Sie den Abschnitt **Karten**.

11. Verwenden Sie den Schieberegler **Akzentleiste**, um ihn auf Aus festzulegen.

    ![](./Media/7.17.png)
 
12. Wählen Sie im Visualisierungsbereich **Allgemein** aus.

13. Erweitern Sie den **Abschnitt „Effekte“**.

14. Verwenden Sie den Schieberegler **Hintergrund**, um ihn auf **Aus** festzulegen.

15. Ändern Sie die Größe des **Visuals**, und verschieben Sie es in das **linke Feld, wie im Screenshot dargestellt**.

    ![](./Media/7.18.png)
 
16. Fügen wir nun einen weiteren KPI hinzu. Wählen Sie die soeben erstellte **mehrzeilige Sales-Karte** aus. **Kopieren Sie** das Visual, indem Sie **STRG+C** auf Ihrer Tastatur auswählen.

17. **Fügen Sie** das Visual ein, indem Sie **STRG+V** auf Ihrer Tastatur auswählen. Beachten Sie, dass das Visual in das Canvas eingefügt wird.

18. Wenn das **neue Visual hervorgehoben ist**, entfernen Sie im Abschnitt **Visualisierungsbereich -> Visual erstellen -> Felder** die Kennzahl **Sales**.

19. Erweitern Sie im Abschnitt **Daten** die Tabelle **Sales**, und wählen Sie die Kennzahl **Units** aus.

20. Ändern Sie die Größe des **Visuals** und **platzieren Sie es im Feld unter dem Sales-Visual**.

    ![](./Media/7.19.png)


### Aufgabe 6: Dem Bericht ein Liniendiagramm hinzufügen

Lassen Sie uns ein Liniendiagramm erstellen, um Sales im Zeitverlauf nach Reseller Company zu visualisieren.
1. Wählen Sie den **Leerraum** im Canvas aus, um den Fokus vom mehrzeiligen Kartenvisual zu entfernen.
2. Wählen Sie im **Abschnitt Visualisierungen** die Option **Liniendiagramm** aus.
3. Erweitern Sie im **Abschnitt „Daten“** die Tabelle **Date**.
4. Wählen Sie das Feld **Year** aus. Beachten Sie, dass „Year“ standardmäßig summiert und der Y-Achse hinzugefügt wird. Lassen Sie uns dies korrigieren.
  
    ![](./Media/7.20.png)

### Aufgabe 7: Spalte „Year“ in der Tabelle „Date“ konfigurieren

1. Navigieren Sie über die **Modellansicht von Lakehouse** zur Registerkarte des Browsers.
2. Erweitern Sie im linken Explorer-Bereich **lhFAIAD -> Schemas -> dbo -> Tables -> Date**.
3. Wählen Sie die Spalte **Year** aus.
4. Erweitern Sie im Bereich **Eigenschaften** rechts den Abschnitt **Erweitert**.
5. Wählen Sie aus der Dropdownliste **Zusammenfassen nach** den Eintrag **Keine** aus.

    ![](./Media/7.21.png)
 
6. Navigieren Sie mit dem **Power BI-Canvas** zurück zur Registerkarte des Browsers.
7. Wählen Sie im oberen Menü **Aktualisieren** aus. Beachten Sie, dass „Year“ kein Summierungsfeld ist. 
8. Wenn das **Visual „Liniendiagramm“ ausgewählt ist, entfernen Sie „Sum of Year“** von der Y-Achse.
9. Wählen Sie das Feld **Year** aus, sodass es der **X-Achse** hinzugefügt wird.
10. Erweitern Sie die Tabelle **Sales**, und wählen Sie die **Kennzahl „Sales“** aus.
 
    ![](./Media/7.22.png)

### Aufgabe 8: Die Spalte „Short_Month_Name“ in der Tabelle „Date“ konfigurieren

1. Fügen wir diesem Diagramm „Monat“ hinzu. Ziehen Sie das Feld **Short_Month_Name** unter **Year** aus der Tabelle „Date“ in die **X-Achse**. Beachten Sie dass das Visual nach „Sales“ sortiert ist. Nun sortieren wir es nach Short_Month_Name.
2. Wählen Sie die **Auslassungspunkte (…)** oben rechts im Visual aus.
3. Wählen Sie **Sortierachse -> Year Short_Month_Name** aus.
4. Wählen Sie die **Auslassungspunkte (…)** oben rechts im Visual aus.
5. Wählen Sie **Sortierachse -> Aufsteigend sortieren** aus.

    ![](./Media/7.23.png)
 
**Hinweis:** Die Monate sind alphabetisch sortiert. Lassen Sie uns dieses Problem beheben.

![](./Media/7.24.png)
 
6. Navigieren Sie über die **Modellansicht von Lakehouse** zur Registerkarte des Browsers.
7. Erweitern Sie im linken Explorer-Bereich **lhFAIAD -> Schemas -> dbo -> Tables -> Date**.
8. Wählen Sie die Spalte **Short_Month_Name** aus.
9. Erweitern Sie im Bereich **Eigenschaften** rechts den Abschnitt **Erweitert**.
10. Wählen Sie im Dropdownmenü **Nach Spalte sortieren** den Eintrag **Monat** aus.

    ![](./Media/7.25.png)
 
11. Navigieren Sie mit dem **Power BI-Canvas** zurück zur Registerkarte des Browsers.

12. Wählen Sie im oberen Menü **Aktualisieren** aus. Beachten Sie, dass die Monate jetzt richtig sortiert sind.

    ![](./Media/7.26.png)
  

### Aufgabe 9: Liniendiagramm formatieren
Beachten Sie, wie einfach es ist, das semantische Modell beim Erstellen der Berichte zu aktualisieren. Daraus ergibt sich eine nahtlose Interaktion wie Power BI Desktop.

1. Wenn das **Visual „Liniendiagramm“ ausgewählt ist**, erweitern Sie im Abschnitt **Daten** die Tabelle **Reseller**.

2. Ziehen Sie das Feld **Reseller -> Reseller Company** in den Abschnitt **Legende**.
 
    ![](./Media/7.27.png)

3. Wenn das **Visual „Liniendiagramm“ ausgewählt ist**, wählen Sie im Abschnitt **Visualisierung** das **Symbol „Visual formatieren“ -> Allgemein** aus.
4. Erweitern Sie den Abschnitt **Titel**.
5. Legen Sie den **Titeltext** auf **Verkäufe im Zeitverlauf** fest.
6. Erweitern Sie den Abschnitt **Effekte**.
7. Verwenden Sie den Schieberegler **Hintergrund**, um ihn auf **Aus** festzulegen.

    ![](./Media/7.28.png)
 
8. Wählen Sie im Abschnitt **Visualisierung Symbol „Visual formatieren“ -> Visual** aus.
9. Erweitern Sie den Abschnitt **X-Achse**.
10. Verwenden Sie den Schieberegler **Titel**, um ihn auf **Aus** festzulegen.
11. Erweitern Sie den Abschnitt **Linien**.
12. Erweitern Sie den Abschnitt **Farben**.
13. Legen Sie die Farbe von **Wingtip Toys** auf **#004753** fest.
14. Legen Sie die Farbe von **Tailspin Toys** auf **#F17925** fest.
15. Ändern Sie die Größe des Visuals, und verschieben Sie es in das **obere rechte Feld, wie im Screenshot dargestellt**.
16. Scrollen Sie im Visual nach rechts und **beachten Sie, dass Daten bis April 2023 verfügbar sind**.

    ![](./Media/7.29.png)

17. Lassen Sie uns den Bericht speichern, indem wird im Menü **Datei -> Speichern** auswählen.
18. Das Dialogfeld „Bericht speichern“ wird geöffnet. Geben Sie dem Bericht den Namen **rpt_Sales_Report**.

**Hinweis:** Wir stellen dem Berichtsnamen das Präfix „rpt“ voran, was für „Bericht“ steht.

19. Stellen Sie sicher, dass der Bericht unter **<Name Ihres Arbeitsbereichs>** gespeichert wird.
20. Wählen Sie **Speichern** aus.

    ![](./Media/7.30.png)
 
Wie bereits erwähnt, werden wir nicht alle Visuals in dieser Übung erstellen. Sie können nach Belieben weitere Visuals erstellen. 

### Aufgabe 10: Neue Daten hinzufügen, um den Direct Lake-Modus zu simulieren
Normalerweise müssen wir im Import-Modus, sobald die Daten in der Quelle aktualisiert wurden, das Power BI-Modell aktualisieren, woraufhin die Daten im Bericht aktualisiert werden. Im Direct Query-Modus sind die Daten im Power BI-Bericht verfügbar, nachdem sie in der Quelle aktualisiert wurden. Der Direct Query-Modus ist in der Regel jedoch langsam. Um dieses Problem zu beheben, hat Microsoft Fabric den Direct Lake-Modus eingeführt. Direct Lake ermöglicht das schnelle Laden der Daten aus dem Lake direkt in das Power BI-Modul, wo sie für die Analyse bereit sind. Untersuchen wir dies genauer.

In einem realen Szenario werden die Daten an der Quelle aktualisiert. Da wir uns in einer Trainingsumgebung befinden, simulieren wir dies, indem wir eine Verbindung mit einer Parquet-Datei mit Daten für Mai 2023 herstellen.

1. Navigieren Sie über die **Modellansicht von Lakehouse** zur Registerkarte des Browsers.
2. Wählen Sie im linken Bereich **<Arbeitsbereiche>** aus.
3. Wählen Sie **df_Sales_ADFS** aus, damit wir den Dataflow bearbeiten können, indem wir die neue Parquet-Datei hinzufügen.

    ![](./Media/7.31.png)
 
4. Öffnen Sie, sofern noch nicht geschehen, auf dem **Desktop** Ihrer Übungsumgebung im Ordner **Report** die Datei **FAIAD.pbix**. 
5. Wählen Sie im Menüband **Start > Daten transformieren** aus. Das Power Query-Fenster wird geöffnet.
6. Wählen Sie links unter dem Ordner **DirectLake** die Abfrage **MayInvoice** aus.
7. **Klicken Sie mit der rechten Maustaste**, und wählen Sie **Kopieren** aus.

    ![](./Media/7.32.png)
 
8. Rufen Sie im Browser wieder das Fenster **Dataflow** auf.

9. Drücken Sie im Bereich „Dataflow“ auf **STRG+V** (das Einfügen mittels Rechtsklick ist derzeit nicht möglich).

Entfernen wir nun den Verweis auf den „ADLS Base Folder (2)“ und verwenden wir den „ADLS Base Folder“.

10. Wählen Sie die Abfrage **MayInvoice** aus.

11. Wählen Sie im rechten Bereich unter **Angewendete Schritte** die Option **Quelle** aus.

12. Ändern Sie in der Formelleiste **#"ADLS Base Folder (2)"** in **#"ADLS Base Folder"**.

13. Klicken Sie auf das **Häkchen** neben der Formelleiste, oder drücken Sie die Eingabetaste.

    ![](./Media/7.33.png)
 
14. Klicken Sie im linken Bereich unter dem Abschnitt „Abfragen“ mit der rechten Maustaste auf die **ADLS Base Folder (2)**-Abfrage, und wählen Sie **Löschen** aus.

15. Das Dialogfeld „Abfrage löschen“ wird angezeigt. Wählen Sie zur Bestätigung **Löschen** aus.

    ![](./Media/7.34.png)
 
16. Fügen wir nun die Rechnungsdaten vom Mai an die Invoice-Tabelle an. Wählen Sie im Abschnitt „Abfragen“ die Abfrage **„Invoice“** aus.

17. Wählen Sie im Menüband **Start -> Anfragen** anfügen aus.

18. Das Dialogfeld „Abfrage anfügen“ wird angezeigt. Wählen Sie aus der Dropdown-Liste **Anzufügende Tabelle** den Eintrag **MayInvoice** aus.

19. Wählen Sie **OK** aus.

    ![](./Media/7.35.png)
 
20. Wählen Sie in der unteren rechten Ecke **Veröffentlichen** aus, um die Änderungen zu speichern und zu veröffentlichen.

    ![](./Media/7.36.png)
 
**Hinweis:** Nach der Veröffentlichung wird der Dataflow aktualisiert. Dies kann einige Minuten dauern.

21. Navigieren Sie mit dem **Power BI-Canvas** zurück zur Registerkarte des Browsers.

22. Wählen Sie im oberen Menü **Aktualisieren** aus. Beachten Sie, dass im Liniendiagramm jetzt Daten für Mai 2023 vorhanden sind. Beachten Sie auch, dass der Verkaufswert gestiegen ist.

    ![](./Media/7.37.png)
 
Da jeder Dataflow, den wir in früheren Übungen erstellt haben, termingerecht aktualisiert wird, werden die Daten in Lakehouse erfasst. Das Datenmodell in Lakehouse wird aktualisiert und die Berichte werden aktualisiert. Wir müssen das Datenmodell und den Bericht nicht aktualisieren, wenn jeder Dataflow aktualisiert wird. Dies ist der Vorteil von Direct Lake.

Sehen wir uns noch einmal die Herausforderungen an, die in der Problemstellung aufgeführt sind:

- **Das Dataset muss mindestens dreimal täglich aktualisiert werden, um den verschiedenen Aktualisierungszeiten der Datenquellen Rechnung zu tragen**.

Wir haben dieses Problem mithilfe von Direct Lake gelöst. Jeder einzelne Dataflow wird nach seinem Zeitplan aktualisiert. Das DataSet und der Bericht müssen nicht aktualisiert werden.

- **Die Aktualisierungen dauern lange, weil die Daten jedes Mal komplett aktualisiert werden müssen, um alle Änderungen an den Daten in den Quellsystemen zu erfassen**.

Auch hier haben wir dieses Problem mithilfe von Direct Lake gelöst. Jeder einzelne Dataflow wird nach seinem Zeitplan aktualisiert. Das DataSet und der Bericht müssen nicht aktualisiert werden, sodass wir uns keine Sorgen über eine vollständige Aktualisierung machen müssen. 

- **Tritt in den Datenquellen, aus denen die Daten abgerufen werden, ein Fehler auf, wird die DataSet-Aktualisierung abgebrochen. Oftmals wird die Mitarbeiterdatei nicht pünktlich hochgeladen, was ebenso zum Abbruch der DataSet-Aktualisierung führt**. 

Die Datenpipeline hilft, dieses Problem zu lösen, indem es die Möglichkeit bietet, die Aktualisierung bei Fehlern und in verschiedenen Intervallen zu wiederholen.

- **Änderungen am Datenmodell nehmen sehr viel Zeit in Anspruch, weil Power Query aufgrund der großen Datenmenge und des aufwändigen Transformationsvorgangs sehr lange braucht, um die Vorschauversionen zu aktualisieren**.

Wir haben festgestellt, dass Dataflows effizient und einfach zu ändern sind. Das Laden der Vorschauversion in Dataflows dauert in der Regel nicht lange.

- **Für Power BI Desktop brauchen Sie einen PC mit Windows, auch wenn im Unternehmen Mac-Geräte genutzt werden**.

Microsoft Fabric ist ein SaaS-Angebot. Wir benötigen lediglich einen Browser, um auf den Dienst zuzugreifen. Wir müssen keine Software auf unseren Desktops installieren.

### Übungsumgebung bereinigen

Wenn Sie bereit sind, die Übungsumgebung zu bereinigen, führen Sie die folgenden Schritte aus.

1. Navigieren Sie mit dem **Power BI-Canvas** zurück zur Registerkarte des Browsers. **Schließen Sie diese Registerkarte**.

2. Navigieren Sie über die **Modellansicht von Lakehouse** zur Registerkarte.

3. Wählen Sie im linken Bereich **<Name Ihres Arbeitsbereichs>** aus, um zur Startseite zu navigieren.

    ![](./Media/7.38.png)
 
4. Klicken im oberen Menü auf die **Auslassungspunkte (…)** neben „Zugriff verwalten“, und wählen Sie **Arbeitsbereichseinstellungen** aus.

    ![](./Media/7.39.png)
 
5. Das Dialogfeld „Arbeitsbereichseinstellungen“ wird geöffnet. Wählen Sie im linken Menü **Weitere** aus.
6. Wählen Sie **Diesen Arbeitsbereich entfernen** aus.
7. Das Dialogfeld „Arbeitsbereich löschen“ wird angezeigt. Wählen Sie **Löschen** aus.

Dadurch werden der Arbeitsbereich und alle darin enthaltenen Elemente gelöscht.

![](./Media/7.40.png)
 

## Referenzen
Bei Fabric Analyst in a Day (FAIAD) lernen Sie einige der wichtigsten Funktionen von Microsoft Fabric kennen. Im Menü des Dienstes finden Sie in der Hilfe (?) Links zu praktischen Informationen.

![](./Media/7.41.png)

Nachfolgend finden Sie weitere Angebote zur weiteren Arbeit mit Microsoft Fabric.

- Die vollständige https://aka.ms/Fabric-Hero-Blog-Ignite23 finden Sie im Blogbeitrag.
- Fabric bei einer https://aka.ms/Fabric-GuidedTour kennenlernen
- Zur https://aka.ms/try-fabric anmelden
- https://aka.ms/microsoft-fabric besuchen
- Mit Modulen von https://aka.ms/learn-fabric neue Qualifikationen erwerben
- https://aka.ms/fabric-docs lesen
- https://aka.ms/fabric-get-started-ebook lesen
- Mitglied der https://aka.ms/fabric-community werden, um Fragen zu stellen, Feedback zu geben und sich mit anderen auszutauschen

Lesen Sie die detaillierteren Blogs zur Ankündigung der Fabric-Umgebung:

- https://aka.ms/Fabric-Data-Factory-Blog
- https://aka.ms/Fabric-DE-Blog
- https://aka.ms/Fabric-DS-Blog
- https://aka.ms/Fabric-DW-Blog
- https://aka.ms/Fabric-RTA-Blog
- https://aka.ms/Fabric-PBI-Blog
- https://aka.ms/Fabric-DA-Blog
- https://aka.ms/Fabric-Admin-Gov-Blog
- https://aka.ms/Fabric-OneLake-Blog
- https://aka.ms/Dataverse-Fabric-Blog

© 2023 Microsoft Corporation. Alle Rechte vorbehalten.

Durch die Verwendung der vorliegenden Demo/Übung stimmen Sie den folgenden Bedingungen zu:

Die in dieser Demo/Übung beschriebene Technologie/Funktionalität wird von der Microsoft Corporation bereitgestellt, um Feedback von Ihnen zu erhalten und Ihnen Wissen zu vermitteln. Sie dürfen die Demo/Übung nur verwenden, um derartige Technologiefeatures und Funktionen zu bewerten und Microsoft Feedback zu geben. Es ist Ihnen nicht erlaubt, sie für andere Zwecke zu verwenden. Es ist Ihnen nicht gestattet, diese Demo/Übung oder einen Teil derselben zu ändern, zu kopieren, zu verbreiten, zu übertragen, anzuzeigen, auszuführen, zu vervielfältigen, zu veröffentlichen, zu lizenzieren, zu transferieren oder zu verkaufen oder aus ihr abgeleitete Werke zu erstellen.

DAS KOPIEREN ODER VERVIELFÄLTIGEN DER DEMO/ÜBUNG (ODER EINES TEILS DERSELBEN) AUF EINEN/EINEM ANDEREN SERVER ODER SPEICHERORT FÜR DIE WEITERE VERVIELFÄLTIGUNG ODER VERBREITUNG IST AUSDRÜCKLICH UNTERSAGT.

DIESE DEMO/ÜBUNG STELLT BESTIMMTE SOFTWARE-TECHNOLOGIE-/PRODUKTFEATURES UND FUNKTIONEN, EINSCHLIESSLICH POTENZIELLER NEUER FEATURES UND KONZEPTE, IN EINER SIMULIERTEN UMGEBUNG OHNE KOMPLEXE EINRICHTUNG ODER INSTALLATION FÜR DEN OBEN BESCHRIEBENEN ZWECK BEREIT. DIE TECHNOLOGIE/KONZEPTE IN DIESER DEMO/ÜBUNG ZEIGEN MÖGLICHERWEISE NICHT DAS VOLLSTÄNDIGE FUNKTIONSSPEKTRUM UND FUNKTIONIEREN MÖGLICHERWEISE NICHT WIE DIE ENDGÜLTIGE VERSION. UNTER UMSTÄNDEN VERÖFFENTLICHEN WIR AUCH KEINE ENDGÜLTIGE VERSION DERARTIGER FEATURES ODER KONZEPTE. IHRE ERFAHRUNG BEI DER VERWENDUNG DERARTIGER FEATURES UND FUNKTIONEN IN EINER PHYSISCHEN UMGEBUNG KANN FERNER ABWEICHEND SEIN.

**FEEDBACK.** Wenn Sie Feedback zu den Technologiefeatures, Funktionen und/oder Konzepten geben, die in dieser Demo/Übung beschrieben werden, gewähren Sie Microsoft das Recht, Ihr Feedback in jeglicher Weise und für jeglichen Zweck kostenlos zu verwenden, zu veröffentlichen und gewerblich zu nutzen. Außerdem treten Sie Dritten kostenlos sämtliche Patentrechte ab, die erforderlich sind, damit deren Produkte, Technologien und Dienste bestimmte Teile einer Software oder eines Dienstes von Microsoft, welche/welcher das Feedback enthält, verwenden oder eine Verbindung zu dieser/diesem herstellen können. Sie geben kein Feedback, das einem Lizenzvertrag unterliegt, aufgrund dessen Microsoft Drittparteien eine Lizenz für seine Software oder Dokumentation gewähren muss, weil wir Ihr Feedback in diese aufnehmen. Diese Rechte bestehen nach Ablauf dieser Vereinbarung fort.
DIE MICROSOFT CORPORATION LEHNT HIERMIT JEGLICHE GEWÄHRLEISTUNGEN UND GARANTIEN IN BEZUG AUF DIE DEMO/ÜBUNG AB, EINSCHLIESSLICH ALLER AUSDRÜCKLICHEN, KONKLUDENTEN ODER GESETZLICHEN GEWÄHRLEISTUNGEN UND GARANTIEN DER HANDELSÜBLICHKEIT, DER EIGNUNG FÜR EINEN BESTIMMTEN ZWECK, DES RECHTSANSPRUCHS UND DER NICHTVERLETZUNG VON RECHTEN DRITTER. MICROSOFT MACHT KEINERLEI ZUSICHERUNGEN BZW. ERHEBT KEINERLEI ANSPRÜCHE IM HINBLICK AUF DIE RICHTIGKEIT DER ERGEBNISSE UND DES AUS DER VERWENDUNG DER DEMO/ÜBUNG RESULTIERENDEN ARBEITSERGEBNISSES BZW. BEZÜGLICH DER EIGNUNG DER IN DER DEMO/ÜBUNG ENTHALTENEN INFORMATIONEN FÜR EINEN BESTIMMTEN ZWECK.

**HAFTUNGSAUSSCHLUSS**

Diese Demo/Übung enthält nur einen Teil der neuen Features und Verbesserungen in Microsoft Power BI. Einige Features können sich unter Umständen in zukünftigen Versionen des Produkts ändern. In dieser Demo/Übung erhalten Sie Informationen über einige, aber nicht über alle neuen Features.

