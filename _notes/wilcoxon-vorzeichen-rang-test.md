---
title: Wilcoxon-Vorzeichen-Rang Test
---

Der Wilcoxon-Vorzeichen Rang-Test ist das non-parametrische Gegenstück zu dem t-Test für abhängige Stichproben.
Hierbei müssen die Daten nicht normalverteilt sein.

Kann ein- oder zweiseitig getestet werden.

---

### <u>Beispiel:</u>

Gibt es einen Unterschied im Stresslevel vor und nach einer Aufmerksamkeitsübung?

* **Abhängige Variable:** Stresslevel (ordinal oder nicht normalverteilt metrisch)

* **Unabhängige Variable:** Messzeitpunkt (vorher vs. nachher)

---

### <u>Voraussetzungen:</u>

* Ordinalskalierte Merkmale

---

### <u>Hypothesen:</u>

* H<sub>0</sub>: Median der Differenzen $\neq$ 0
  * Die Summe der Ranplatzverschlechterungen (T<sub>p</sub>) und Rangplatzverbesserungen(T<sub>m</sub>) sind gleich
* H<sub>1</sub>: Median der Differenzen >/\< 0
  * Die Summe der Ranplatzverschlechterungen (T<sub>p</sub>) und Rangplatzverbesserungen(T<sub>m</sub>) sind unterschiedlich
    * Es gibt einen Unterschiede aufgrund der Messzeitpunkte

---

### <u>Entscheidung:</u>

* T<sub>emp</sub> \< T<sub>krit</sub>
  * Signifikant und Nullhypothese wird abgelehnt
  * Anders als normalerweise
* z<sub>emp</sub> $\ge$ z<sub>krit</sub>
  * Signifikant

---

### <u>Vorgehen:</u>

1. Absolutbetrag der Differenz zwischen den Werten der Gruppe 1 und der Gruppe 2 bilden:
   * x<sub>1,n</sub> -x<sub>2,n</sub>
1. Richtung der Änderung notieren:
   * Wenn der Messwert steigt z.B. ein + wenn der Messwert sinkt z.B. ein -
1. Absolutbeträge in Rangreihe bringen und Rangplätze zuweisen:
   * Rangbindung berücksichtigen
   * Bei keiner Differenz (0) wird der Wert nicht weiter beachtet
   * Wenn den gleichen Werten; Mittelwert bestimmen und allen mit dem gleichen Wert den gleichen Rangplatzmittelwert zuweisen
1. Rangsummen bilden
   * T<sub>p</sub>: Alle positiven Rangplätze aufsummieren
   * T<sub>m</sub>: Alle negativen Rangplätze aufsummieren
1. Prüfgröße T<sub>emp</sub>
   * Kleinerer T-Wert wird wird zu T<sub>emp</sub>
1. Ab n $\ge$ 20: z standardisieren:
   * $z = \dfrac{W- \mu_{w}}{\sigma_{w}}$

---

### Navigation:

* Robuste-non-parametrische Verfahren
  * [Zurück zur Übersicht](/robuste-non-parametrische-verfahren)
* Voraussetzungen:
  * 1 Stichprobe:
    * [Voraussetzungen 1](/stichprobenanzahl-robuste)
  * 2 Stichproben:
    * [Voraussetzungen 2](/abhaengigkeit)

\#Test
