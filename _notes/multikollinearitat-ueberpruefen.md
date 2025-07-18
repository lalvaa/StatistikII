---
title: Multikollinearität überprüfen
---

Eine Voraussetzung der multiplen Regression ist das keine stark Multikollinearität vorliegt.
Diese liegt bot wenn Prädiktoren stark miteinander korrelieren, oder ein Prädiktor als (Linear) Kombination anderer Prädiktoren darstellbar ist.

---

##### <u>Problem:</u>

* Die Regressionskoeffizienten werden verzerrt geschätzt
  * Schwierig oder unmöglich den Einfluss einzelner Prädiktoren sinnvoll zu interpretieren
* Es kann passieren dass;
  * Eigentlich wichtige Prädiktoren nicht signifikant erscheinen
  * Vorzeichen der Effekte vertauscht werden

---

##### <u>Lösung:</u>

* VIF (Variations-Inflations-Faktor)
  * Misst wie stark die Varianz eines Regressionsgewichts durch Multikollinearität verzerrt wird
  * VIF $\ge$ 10
    * Starke Multikollinearität
  * VIF $\ge$ 3
    * Mögliche Multikollinearität
  * VIF \< 3
    * Unbedenklich

---

##### <u>Navigation:</u>

[Multiple Lineare Regression](/Multiple-lineare-regression)
