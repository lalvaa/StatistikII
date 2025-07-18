---
title: Ausreißer überprüfen
---


Ausreißer sind Beobachtungswerte die am Rand der Verteilung liegen (bzgl. des Kriteriums)
Eine Voraussetzung der Multiplen Regression ist es keine starken Ausreißer zu haben. Dies können die Regressionsgerade stark verschieben und sind besonders kritisch wenn;

* Ausreißer sind nicht direkt als solche sichtbar
* Zeigen erst nach der Regressionsrechnung ihre Hebelwirkung

\_\_\_-

##### <u>Cook´s Distance:</u>

* Zeigt wie stark ein Datenpunkt das Regressionsmodell beeinflusst
* In Jamovi:
  * Für **jeden einzelnen Wert** wird berechnet, wie stark dieser das Modell verzerrt.
    * Sozusagen wie **stark würde sich das Modell ändern**, wenn man diesen Wert **entfernt**?
  * Min: die kleinste Verzerrung des Modells aufgrund eines Wertes
    * Unwichtig
  * Max: Die größte Verzerrung des Modells aufgrund eines Wertes
    * Auffällig bei ungefähr $max \ge1$
    * Bei großem Wert können wir davon ausgehen, dass ein Ausreißer im Datensatz ist

---

##### <u>Navigation:</u>

* [Multiple Lineare Regression](/Multiple-lineare-regression)
