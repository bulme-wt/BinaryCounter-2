# Aufgabenstellung BinaryCounter2
Versionen in C++ und Python

## Vorbereitung github
- logge dich auf deinem Github-Account ein
- navigiere zu https://github.com/bulme-wt/BinaryCounter-2
- erstelle einen Fork dieses Projekts in deinem Github-Account
- Im Terminal deines Raspberrys: ```git clone git@github.com:hierDeinGithubUsername/BinaryCounter-2.git```

## Programmierung
Auf Basis des existierenden Code-Gerüstes soll ein Modulo-100-Zähler programmiert werden, der den Zählerstand im grafischen
Widget und (die letzten vier Bits) über die LEDs am Zusatzboard anzeigt.

Spezifikationen:
- Der Startwert soll 1 sein
- Druck auf Taster GPIO17: erhöhe den Zählerstand um 1
- Druck auf Taster GPIO22: verdopple den Zählerstand
- Druck auf Taster GPIO27: verkleinere den Zählerstand um 1
- Der Zählvorgang wird durch die fallende Flanke beim Drücken des Tasters ausgelöst. Längeres Drücken löst keinen weiteren Zählvorgang aus.
- Der Zähler soll von 0 bis 15 zählen. Auf den Höchstwert 99 folgt wieder 0. Beim Abwärtszählen folgt auf 0 der Wert 99.
- Anzeige des Zählerstandes im Widget durch QLCDNumber dezimal.
- Anzeige des Zählerstandes am Zusatzboard: die letzten (niederwertigsten) vier Bits werden dual über die 4 LEDs (GPIO18 = MSB, GPIO25 = LSB) angezeigt. Umrechnung dezimal-dual bitte *nicht* mit mehrfach-if-Bedingungen, sondern mittels geeignetem Algorithmus.

## Abgabe
Hochladen auf github:
```
git add .
git commit -m "Abgabe"
git push origin main
```



