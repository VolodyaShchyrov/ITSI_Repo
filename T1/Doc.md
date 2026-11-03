# ***Task - Grundlagen*** 

`Name`: Volodymyr Shchyrov 

`Klasse`: 3CHIT

`Datum`: 09/10/26 


### **Teil 1 - Bedrohungsmodellierung mit dem Microsoft Threat Modeling Tool**

**Schritt 1: Tool kennenlernen**

Installieren wir zuerst das Programm ```Microsoft Threat Modeling tool```. Dannach erstellen wir eine neue Model mit einem bestimten Tamplate **SDL TM Knowledge Base**.

![Screenshot](./img/Screenshot%202026-10-09%20140346.png)

**Schritt 2: System modellieren**

Erstellen wir eine **Datenflussdiagramm (DFD)** Mit solche Objekte:

    - Externe Eintität
    - Prozesse
    - Datenspeicher
    - Datenflüsse

![DFD](./img/DFD2.png)


**Schritt 3: Bedrohungen analysieren**

Dieses Tool kann alle Bedrohungen automatish generieren und vorgeschlagene Risiken analyieren.

![Analyse](./img/Analyse.png)

Wenn man bei **View => Analyses View** klickt, öffnet man eine Bedrohungsliste mit allen möglichen Bedrohungen.

Bei mir kommt auf einmal 31 Bedrohungen. Solche Bedrohungen wie: Spoofing, Elevation, SQL injection, Tampering, Denial Of Service.

Alle diese Bedrohungstypen steheN auf höherem Priorität, weil sie alle kritisch sein können.


**Schritt 4: Gegenmaßnahmen entwickeln**

|**Bedrohung**|**Risiko**|**Gegenmaßnahme**|
|-------------|----------|-----------------|
|Elevation Of Privilege|Eine SQL-Datenbank könnte unter Umständen die Remote-Ausführung von Code für eine Webanwendung ermöglichen.|Einschränkung der Datenbankrechte, Deaktivierung gefährlicher Funktionalitäten|
|Denial Of Service|Die Webanwendung stürzt ab, bleibt stehen, hält an oder läuft langsam – in all diesen Fällen wird ein Verfügbarkeitswert verletzt.|Lastverteilung, Time-out's, Überwachung und Alarmierung|
|Repudiation|Die Webanwendung gibt an, keine Daten von einer Quelle außerhalb der Vertrauensgrenze erhalten zu haben. Ziehen Sie den Einsatz von Protokollierung oder Auditierung in Betracht, um die Quelle, den Zeitpunkt sowie eine Zusammenfassung der empfangenen Daten zu erfassen.|Protokollierung, Auditing|


**Schritt 5: Reflexion**

1. Ich habe das Programm ```Microsoft Threat Modeling tool``` kennengelernt und wofür verwendet man dieses Programm.
2. Automatische Bedrohungskennung ist sehr hilfreich, weil dise System sehr viel zeit beim Bedrohungsuche speichert und dises Programm allgemein sehr angenehm zur Benutzung ist.
3. Es gab keine wesentliche Probleme, außer dass, das es genug Zeit verbraucht.



### **Teil 2 - Vulnerability Analyse**

**Setup:** 
- Webserver läuft als root
- /admin nur durch URL erreichbar (keine Auth)
- Debug-Modus aktiv
- .git-Ordner öffentlich zugänglich
- keine Input-Validierung bei Formularen
- keine TLS-Verschlüsselung

**Aufgabe 1:**



