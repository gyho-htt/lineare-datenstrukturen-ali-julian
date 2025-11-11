# Arbeitsauftrag
Beobachte das Objektspiel zum *second hand shop* und beantworte folgende Fragen:
1. Wie entwickelt sich die Länge der Datenstruktur? Spielt die Länge der Datenstruktur eine Rolle zur Verwaltung der Elemente?
je mehr Käufer kommen, desto länger wird die Schlange 
- Dynammische Länge
- Spielt keine Rolle (Vermutung: alle Verwaltungsoperationen funktionieren auf jeder beliebigen Länge. Auf die meisten Elemente wird nicht zugegriffen)

2. Wie werden neue Elemente hinzugefügt?
In eine Schlange angestellt
- Das Verwaltungsobjekt fügt das neue Element hinter das letzte Element ein.
- Interessanter Fall: Das aller erste Element, wenn die Schlange leer ist.

3. Auf welche Elemente wird Zugegriffen?
Auf das erste in der Schlange
- Es wird nur auf das erste Element zugegriffen.

4. Welche Beziehungen der Elemente gibt es untereinander?
Elemente kennen sich nicht unbtereinander. Kennen nur Verwaltungs Operator und Verkäufer (Henry)
- Ein Element kennt das Element das vor ihm steht (Vorgänger)
- Jedes Element kennt seinen Inhalt (Hier: Bestellbestätigung)
- Frage: Muss jedes Element auch seinen Nachfolger kennen??? damit die Schlange aufrücken kann.
	-> Elemente müssen ihre Nachfolger nicht kennen (oder doch? ansonsten geht Information verloren)

5. Welche Elemente müsste ein Verwaltungselement kennen?
Alle die sich in der Schlange anstellen
- Alle Elemente? Erstes und letztes auf jeden Fall.
- Das Verwaltungobjekt kennt den INhalt der Elemente nicht.
- Frage: Wird jemals die Position aller Elemente benutzt???
	-> Nein! Nur das erste und das letzte Element

6. Nach welchem Prinzip arbeitet die Datenstruktur? Wie nennt man eine solche Datenstruktur?
- (Warte-) Schlange englisch: Queue
- FIFO: First in First out

7. Welche (Verwaltungs)Operationen sind für diese Datenstruktur sinnvoll?
anstellen, vorrücken, Schlange verlassen, bestellung bearbeiten
- Elemente hinzufügen (einreihen)
- das erste Element entfernen (entlassen)
	-> aufrücken
- Wissen, ob die Schlange leer ist.
- gib das erste Element

Fragen:
- Vorgänger/ Nachfolger was wird hier wirklich benötigt?
- Was müssen Elemente eigentlich tun können? (vllt. Inhalt geben) 

- Vorgänger: Schleife und If um durchzulaufen wer alles einen Vorgänger hat bis ein Element keinen mehr hat
- Nachfolger: Zwischenspeicher des ersten Elements um danach den ersten Zeiger auf das neue erste Element zu setzen