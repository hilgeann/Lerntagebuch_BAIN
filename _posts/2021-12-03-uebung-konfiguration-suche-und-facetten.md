---
title: "Übung - VuFind:Konfiguration Suche und Facetten"
date: 2021-12-03
---

Zur Vorbereitung auf die LE 8 mussten wir die Installation von VuFind vornehmen. Dank der Unterstützung durch die Dozierenden hat die Installation dann beim dritten Anlauf geklappt. Über die für uns relevanten Hinweise zur Installation und den kurzen Erklärungen dazu, fühlte ich mich besser aufgehoben, als wenn ich alles gemäss der Anleitung auf der VuFind-Website hätte machen müssen. Auch der Testimport von Beispieldaten hat funktioniert. Als ich das Programm dann wieder öffne, um mögliche Inhalte parallel zum Einführungsvideo auszuprobieren, musste ich feststellen, dass Solr separat im Terminal gestartet werden muss, damit beim Aufrufen der Website keine Fehlermeldung angezeigt wird. 
Begonnen wird mit der Suchfunktion, so wird z.B. gezeigt, dass man über die «…searches.ini» Datei festlegen kann, in welcher Reihenfolge die Facetten im Dropdown der Basissuche erscheinen. Und tatsächlich, ein Verschieben der ISBN/ISBN im Dokument «searches» hat eine direkt sichtbare Auswirkung. Beim Advanced Searches, sieht man links die Search Handlers und rechts die sogenannten Translation Strings. Diese können beliebig vergeben werden, man muss aber wissen, dass diese in jeder verfügbaren Sprache vorhanden sein müssen, damit sie korrekt übersetzt werden können. Die Elemente mit Semikolon sind auskommentiert, da nur in wenigen Fällen nützlich.

<img width="454" alt="grafik" src="https://user-images.githubusercontent.com/90834619/146323224-acf48922-7f4a-4bda-bb5f-ab7ad8eb1e35.png">

Bei Anpassungen von Default-Werten in der Konfig-Datei, muss beachtet werden, dass der Browser neu gestartet wird, da die Default-Einstellungen in Cookies gespeichert werden. So kann z.B. die Anzahl Suchergebnisse pro Seite angepasst werden.
Weiter kann auch das Layout angepasst werden, z.B. in dem die Facetten oberhalb der Suchleiste entfernt werden.

<img width="454" alt="grafik" src="https://user-images.githubusercontent.com/90834619/146323267-73297da3-0c05-4a06-a9de-be6317ed6457.png">

Links in grün stehen Werte, die Felder im Solr Index sind, die Werte rechts sind wieder Translation Strings. Hier können nur Felder verwendet werden, die einen Wert enthalten, weil Solr nicht sortieren kann bei Feldern, die mehrere Werte enthalten können.

<img width="454" alt="grafik" src="https://user-images.githubusercontent.com/90834619/146323302-2880e5ef-7658-4747-87da-43d79d85bf17.png">

Dann wechseln wir in das «facets.ini» Dokument, wo die Solr Felder links, die entsprechenden Facetten und z.B. deren Reihenfolge festlegen.

<img width="454" alt="grafik" src="https://user-images.githubusercontent.com/90834619/146323332-56bdb1db-4d9c-468c-aa33-6a2e28c940e0.png">

Durch dateRange wird z.B. ermöglicht, dass es einen Schieberegler gibt, mit dem man das Datum anpassen kann.

<img width="454" alt="grafik" src="https://user-images.githubusercontent.com/90834619/146323367-083d3b56-2989-4357-a52a-95648ee7714f.png">

Das Einfügen dieser Checkbox, ermöglicht dann ein Feld, bei dem alle Ergebnisse ohne Autor\*innen angewählt werden können.

<img width="454" alt="grafik" src="https://user-images.githubusercontent.com/90834619/146323767-d19612d9-4ce3-437c-b4c0-97aa218ac050.png">
<img width="226" alt="grafik" src="https://user-images.githubusercontent.com/90834619/146323784-2e8316ff-cf5d-4791-a178-57023f0dc757.png">

Es kann festgelegt werden, wie viele Facetten angezeigt werden und um wie viele die Ansicht erweitert werden kann. Oder auch eine Option, die es ermöglicht manuell gewisse Facetten auszuschliessen bzw. Facetten auszuwählen und mit einem Booleschen ODER zu verknüpfen. Hierbei bleiben nach der Auswahl die anderen Facetten weiterhin sichtbar.
Es kann auch bestimmt werden, welche Facetten auf der Homepage angezeigt werden sollen.
Im Video wird dann noch gezeigt, welchen Einfluss auf die Präsentation der Suchergebnisse genommen werden kann. So kann die Wichtigkeit einzelner Felder im Verhältnis zueinander eingerichtet werden. Sind z.B. Treffer im Autor\*innenfeld wichtiger als im Titelfeld, werden diese weiter oben angezeigt. Ausserdem gibt es die Möglichkeit die Exaktesuche zu konfigurieren bzw. ein Relevanceranking einzurichten.
