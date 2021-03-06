# U04 | ToDo-Liste

## Aufgabe

Erstellen Sie eine **ToDo-Liste**, die es dem Benutzer erlaubt Aufgaben über ein Eingabefeld (`EditText`) zu erstellen. Die eingegebenen Aufgaben werden in einem `ListView` angezeigt und können gelöscht werden, in dem der Benutzer länger auf den entsprechenden Eintrag in der Liste klickt (`OnItemLongClick()`). Speichern Sie die Aufgaben als String in einer entsprechenden `ArrayList` und  nutzen Sie zur Anbindung an das *User Interface* einen `ArrayAdapter`. Sie sollten bereits damit vertraut sein, wie man `Views` aus dem Layout in einer Activity intialisiert. Speziell geübt werden sollen dadurch der Umgang mit `ListView` und `ArrayAdapter`.


## Hinweise

* Benutzen sie für diese Übung das `Constraint Layout`. In einem Constraint Layout werden Views mittels Constraints “magnetisch” an andere gebunden, um sie so relativ im Layout zu platzieren.

* Für die Implementierung eines "Hinzufügen"-`ImageButtons` können sie das vorgefertigte Icon (unter `res/drawable/ic_add.xml`) als `src` verwenden und das Shape (unter `res/drawable/shape_round_primary_color.xml`) als `background`.

* Lagern Sie Texte, die dem Nutzer später angezeigt werden, in die `strings.xml` (unter `res/values/strings.xm`) aus.

* Nach dem Hinzufügen eines neuen Eintrages soll das Eingabefeld (`EditText`) wieder leer sein.

* Beim `OnItemLongClickListener()` wird die Position des *angeklickten* Elements über den Parameter `position` übergeben. Mithilfe dieser Information kann man auf das korrespondierende Element der ArrayList zugreifen..

* Damit der Adapter Änderung aus der Liste and das `ListView` weitergibt, müssen Sie nach allen Manipulationen Ihrer Liste die Methode `notifyDatSetChanged()` des Adapters aufrufen.

## Vorgehen

Versuchen Sie „ordentlichen“ Code zu erstellen. Lagern Sie Teilaufgaben in Methoden aus. Zur Zuweisung eines *Listener* zu einer `View` reicht eine lokale Referenz innerhalb der entsprechenden Methode. Versuchen Sie Fehler abzufangen. Ihre App sollte keine Probleme damit haben, eine leere Eingabe des Benutzers zu verarbeiten.

1. Laden Sie das Starterpacket herunter und erstellen Sie zunächst das nötige Layout durch bearbeiten der XML-Datei. Beachten Sie dabei die obigen Hinweise und orientieren Sie sich an den Screenshots unten.

2. Bearbeiten Sie die `MainActivity`: Erstellen Sie Instanzvariablen für alle Views die Sie aus dem Layout benötigen und initialisieren Sie diese richtig. Es wird außerdem eine Liste benötigt, in der später die Einträge (Strings) gespeichert werden.

3. Stellen Sie über *Listener* sicher, Klicks des "Hinzufügen"-`ImageButtons` und längere Klicks auf ein `ListView`-Item entsprechend abzufangen und zu verarbeiten.

5. Erstellen Sie anschließend  einen `ArrayAdapter` für den entsprechenden Datentyp. Dieser erwartet für die Listeneinträge das Layout `android.R.layout.simple_list_item_1` und greift als Datenbasis auf Ihre Liste zu. Verbinden Sie den Adapter mit der `ListView`.

## Anmerkungen

In dieser Aufgabe werden die Einträge der ListView im Code durch einfache Strings repräsentiert. Der Ansatz ist für diese Übungsaufgabe zwar akzeptabel (nachdem ein ListView Eintrag aus nur einem einzigen Text besteht), allerdings wäre **das Erstellen einer eigenen Task-Klasse**, welche dann einen einzelnen ListView-Eintrag repräsentiert, der **besserer Ansatz**.

## Screenshots der Anwendung
![Screenshots der ToDo-App](./docs/screenshots.png )
