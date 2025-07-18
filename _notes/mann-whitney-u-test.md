---
title: Mann-Whitney-U-Test
---


Der Mann-Whitney-U-Test ist das Äquivalent für den Zweistichproben t-test für unabhängige Stichproben.
Hierbei werden **Maße der zentrale Tendenz** der beiden Gruppen verglichen.
Der Vergleich wird nicht mit dem Mittelwert $\bar{x}$ sondern mit <u>Rangsummenunterschieden</u> durchgeführt.

Es wird getestet, ob bei der Betrachtung von 2 Populationen es gleich wahrscheinlich ist, dass ein **zufällig ausgewählter Wert** in der Population **größer oder kleiner** ist als ein zufällig ausgewählter Wert aus der anderen Population.

Falls die Nullhypothese verworfen wird geht man davon aus, dass Werte aus einer der Populationen dazu tendieren größer/kleiner zu sein als von der anderen Population.

Kann ein- oder zweiseitig getestet werden.

---

##### <u>Beispiel:</u>

Gibt es einen Unterschied im Stressempfinden zwischen Personen, die regelmäßig meditieren, und solchen, die nicht meditieren?

* **Abhängige Variable:** Stressempfinden (ordinal oder nicht normalverteilt metrisch)
* **Unabhängige Variable:** Meditation (ja / nein)

---

##### <u>Voraussetzung:</u>

* Mindestens Ordinalskalierte Daten

---

##### <u>Hypothesen:</u>

* H<sub>0</sub>: U<sub>u</sub>=U<sub>ü</sub>
* H<sub>1</sub>: U<sub>u</sub> $\neq$ U<sub>ü</sub>
* Die H<sub>0</sub> besagt dass in den beiden Gruppen gleich viele Rangplatzüberschreitungen (U<sub>ü</sub>) bzw Rangplatzunterschreitungen (U<sub>u</sub>) auftreten.

---

##### <u>Entscheidung:</u>

* U<sub>emp</sub> $\le$ U<sub>krit</sub> (hier anders als normalerweise)
* Ab n $\ge$ 20:
  * z<sub>emp</sub> $\ge$ z<sub>krit</sub>
* --> Signifikant und wir lehnen die Nullhypothese ab

---

##### <u>Vorgehen:</u>

* Für n \< 50
  
  1. Allen Werten wird ein Rangplatz zugeordnet:
     ![166x101](/Mann-Whitney-U.png)
  1. Rangsummen für beide Gruppen berechnen:
     * T<sub>1</sub> = $\sum_{i=1}^{n} t_{1i}$
       * T<sub>1</sub> = 4+6+5+2 = 17
     * T<sub>2</sub> = $\sum_{i=1}^{n} t_{2i}$
       * T<sub>2</sub> = 8+3+7+1 = 19
  1. Rangplatzüberschreitungen berechnen:
     * Auch ablesbar: Wie viele Rangplätze von Gruppe 1 sind kleiner als von Gruppe 2
     * $U_{1} = n_{1} \cdot n_{2} + \dfrac{n_{1} \cdot (n_{1}+1)}{2} - T_{1}$
       * U<sub>1</u>=9
     * $U_{2} = n_{1} \cdot n_{2} + \dfrac{n_{2} \cdot (n_{2}+1)}{2} - T_{2}$
       * U<sub>2</sub>=7
  1. Prüfgröße U
     * Der kleiner U-Wert wird zum empirischen U-Wert (U<sub>emp</sub>)
       * U<sub>emp</sub> = U<sub>2</sub> = 7
* Für N $\ge$ 20 (bzw n<sub>1</sub> + n<sub>2</sub> $\ge$ 20):
  
  * Z-standardisieren:
    * $z_{emp} = \dfrac{U_{ü} \; - \; \mu_{u}} {\sigma_{u}}$
    * $\mu_{u}$ = Erwartungswert des U-Werts
      * $\mu_{u} = \dfrac{n_{1} \cdot n_{2}} 2$
    * Standardabweichung des U-Werts ($\sigma_{u}$)
      * $\sigma_{u}=\sqrt{ \dfrac{ n_{1} \cdot n_{2} \cdot (n_{1} + n_{2} + 1)} {12}}$

---

##### Navigation:

* Zurück zu Robuste-non-parametrische Verfahren:
  
  * [Zurück zur Übersicht](/robuste-non-parametrische-verfahren)
* Zurück zu Voraussetzungen:
  
  * [Voraussetzungen](/Voraussetzungen\Abhaengigkeit\abhaengigkeit)

\#Test
