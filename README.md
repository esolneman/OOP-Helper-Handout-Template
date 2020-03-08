# OOP-Helper-Handout-Template

## Anleitung

Kopiere den Masterbranch und passe den Inhalt an. Hierbei ist zu beachten, dass die Struktur nich verändert werden darf, sondern nur der Inhalt.
Lege eine *.task* Datei an mit folgendem Inhalt: 

    HANDOUT_URL = *URL des Repositories* 

    HANDOUT_BRANCH_PATH = *Pfad zum Branch zum Beispiel: refs/heads/branch_name* 

    HANDOUT_BRANCH_NAME = *Branchname* 
    
    TASK = *Name der Studienleistung* 

Speichere die Datei im Starterpaket der Studienleistung / Übungsaufgabe im Wurzelverzeichnis.

## Anpassen der Inhalte

### Handout
Das Handout befindet sich im Wurzelverzeichnis mit den Namen *index.html*. Folgende zusätzliche Änderungen können vorgenommen werden:

**Links vom Handout zum Code** Für die Erstellung eines Links vom Handout zum Code wird ein Hyperlink erstellt mit einer *id* und einem *href*-Attribut, welches die Url spezifiziert. Die Url besteht aus einem Bezeichner für die Art des Links *LinkToCode* und Parameter für den Klassennamen *class*, den Pfad im Projektverzeichnis *path* und des Funktionsnamens *function*. Im Fall eines Linkes auf eine Klasse ist der Funktionsname wieder der Klassenname. Im Fall eines Linkes auf eine Funktion werden zusätzliche Inforamtionen der ersten Zeile der Funktion mit eingefügt um sicherzustellen, dass der Link zu der Funktion führt und nicht zu einem Aufruf dieser Funktion.
```
Link auf eine Methode
<a id="LunarLanderLauncher.java/LunarLanderLauncher" href="LinkToCode?class=LunarLanderLauncher.java&amp;path=/src/&amp;function=public%20class%20LunarLanderLauncher">
<code>LunarLanderLauncher</code>
</a> 

Link auf eine Klasse
<a id="LunarLander.java/LunarLander" href="LinkToCode?class=LunarLander.java&amp;path=/src/&amp;function=public%20class%20LunarLander%20"><code>LunarLander</code></a>
```

**Links vom Code zum Handout** Für die Erstellung des Linkes in die entgegengesetzte Richtung wird ein Hyperlink gesetzt mit einem *name*-Attribut, welches aus dem Klassennamen und dem Namen der Methode oder Funktion zusammengesetzt ist.
```
<a name="LunarLander.java/LunarLander" style="padding-top: 50px; margin-top: -50px;"></a>
```

**Links zu einer speziellen Folie im Foliensatz**

Zur Erstellung eines Links für eine bestimmte Seite im foliensatz, um zum Beispiel auf ein Konzept zu verweisen, wird die entsprechende als Parameter *startAtSlide* mitgegeben.
```
<a href="https://regensburger-forscher.de/oop-slides/index.html?slides=08-Interfaces-und-Event-basierte-Programmierung&amp;startAtSlide=28">hier</a>
```

**Einbinden des Videos**

Zum Einbinden des Videos muss dieses in den dafür vorhergesehenen Ordner im Repository speichern */videos* und den Pfad für das Video entsprechend anpassen. Das Foramt des Videos sollte zur Sicherstellung der Funktionalität *mp4* sein.


### Vordefinierte Anforderungen (checkliste)

Die vordefinierte Checkliste kann in der Datei */checklist/checklist.json* angepasst werden. 
Ein einzelner Task besteht aus einer Aufgabenbeschreibung *taskDescription*, einer Kennzeichnung für den Status Aufgabe *checked* und einem eindeutigen Bezeichner *id*.
Der Status der Aufgabe wird im Allgemeinen beim Erstellen der Checkliste auf *false* gesetzt. 
Die *id* dient dazu Änderungen an der Aufgabenbeschreibung beim Updaten der Daten beim Nutzer zurodnen zu können. 

    {"checklist":
          [{"taskDescription":"Die erste Aufgabe",
            "checked":"false", 
            "id": 1}
     ]}
     
### Bewertungskriterien
Die Bewertungskriterien werden in der Datei *specific-assessment-criteria.html* angepasst. 
Dazu werden die Bewertungkriterien in die HTML-Tabelle eingefügt. Hierbei ist zu beachten, dass die Breite *width* der Spalten angepasst werden muss, je nachdem wie viele Abstufungen für ein Kriterium vorhanden sind.


    Die restlichen Dateien und Inhalte müssen nicht extra für eine Studienleistung angepasst werden.
    Bei Bedarf können weitere Shortcuts */common_information/shortcuts.html* hinzugefügt werden.
    
