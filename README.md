# Aufgabenstellung BinaryCounter2
Versionen in C++ und Python

## Vorbereitung github
- logge dich auf deinem Github-Account ein
- navigiere zu https://github.com/bulme-wt/BinaryCounter-2
- erstelle einen Fork dieses Projekts in deinem Github-Account
- Im Terminal deines Raspberrys: ```git clone git@github.com:hierDeinGithubUsername/BinaryCounter-2.git```

## Programmierung
Auf Basis des existierenden Code-Gerüstes soll ein Modulo-16-Zähler programmiert werden, der den Zählerstand im grafischen
Widget und über die LEDs am Zusatzboard anzeigt.

Spezifikationen:
- Der Startwert soll 1 sein
- Druck auf Taster GPIO17: wenn der aktelle Wert gerade ist, erhöhe den Zählerstand um 1, ansonstenen soll er verdoppelt werden
- Druck auf Taster GPIO22: halbiere den Zählerstand und ziehe 1 davon ab
- Druck auf Taster GPIO27: Zählerstand auf 0 zurücksetzen
- Der Zählvorgang wird durch die fallende Flanke beim Drücken des Tasters ausgelöst. Längeres Drücken löst keinen weiteren Zählvorgang aus.
- Der Zähler soll von 0 bis 15 zählen. Auf den Höchstwert 15 folgt wieder 0. Beim Abwärtszählen folgt auf 0 der Wert 15.
- Anzeige des Zählerstandes im Widget durch QLCDNumber dezimal.
- Anzeige des Zählerstandes am Zusatzboard: dual über die 4 LEDs (GPIO18 = MSB, GPIO25 = LSB). Umrechnung dezimal-dual bitte *nicht* mit 
mehrfach-if-Bedingungen, sondern mittels geeignetem Algorithmus.

## Abgabe
Hochladen auf github:
```
git add .
git commit -m "Abgabe"
git push origin main
```



