---
title: Berechnung der Regressiongerade für die einfache lineare Regression
---

**Die Regressionsgerade** ist eine mathematische Gerade, die den Zusammenhang zwischen einer oder mehreren unabhängigen Variablen (Prädiktoren) und einer abhängigen Variablen (Kriterium) beschreibt und zur Vorhersage des Kriteriumswerts dient.

---

### <u>Vorgehen:</u>

* Regressionsgerade  aufstellen
  * $\hat{y} = b_{yx} \cdot x \;+\; a_{yx}$
  * $a_{yx} \text{ und } \; b_{yx}$ sind Regressionsgewichte
    * $b_{yx}\text{ oder } \; b_1$ gibt an wie sehr sich die AV verändert wenn sich UV um eine Einheit verändert
    * $a_{yx} \text{ oder } \; b_0$ ist der Y-Achsenabschnitt
  * Reale Form der Regressionsgerade mit Fehler $\epsilon$
    * $Y_i = b_0 + b_1 \cdot x_i + \epsilon_i$
    * $Y_i$ : Entsprechender Wert des Kriteriums Y für i-Personen
    * $x_i$ : i-te Beobachtung des Prädiktors
    * $b_0/b_1$ : Regressionskoeffizienten
    * $\epsilon_i = Y_i - \hat{Y}_i$ : Residuen
      * Abweichungen von der geschätzten Regressionsgerade
  * Die Variante mit $\hat{y}$ nutzt man für Vorhersagen (brauchen wir)
  * Die Variante mit $\epsilon$ nutzt man zur Modellierung der Realität und zur Analyse der Fehler (Residuen)
* Regressionskoeffizienten berechnen
  * $b_1 = \dfrac{cov(x,y)}{s^2_{x}}$ (b<sub>yx</sub> in Regressionsgerade)
    \* $cov(x,y) = \frac{1}{n \text{ ; } n - 1} \cdot \sum(x_i - \bar{x})\cdot (y_i - \bar{y})$
    \* n für Stichprobe
    \* n-1 für Population
    * $b_{yx} = r_{yx} \cdot \dfrac{s_y}{s_x}$
  * $b_0 = \bar{y} - b_{yx} \cdot \bar{x}$
    * $a_{yx}$ in der Regressionsgerade}
    * wird auch Intercept genannt

---

### <u>Vorhersage:</u>

* Aufgrund der Regressionsgerade kann man eine Vorhersage treffen
  * Z.B.: 5 Stunden Lernzeit
    * x = 5
    * $\hat{y} = b_{yx} \cdot 5 \;+\; a_{yx}$
    * $\hat{y}$: Sagt nun hervor wie viel Prüfungsangst jemand hat wenn diese Person 5 Stunden gelernt hat

---

### <u>Besondere Formen der Regressionsgerade:</u>

* Regressionsgerade bei Nullkorrelation
  * Regressionsgewicht: $b=0$
  * Y-Achsenabschnitt: $a= \bar{y}$
  * Die Regressionsgerade liegt parallel zur x-Achse, bei $\bar{y}$
* Regressionsgerade bei z-standardisierten Variablen
  * $$\hat{z}_{yi}=r_{xy}\cdot z_{xi}$$
  * $b = \beta =r$
    * Gibt an um wie viele Standardabweichungen sich die Variable Y verändert wenn x sich um eins erhöht
  * $a = b_0 = 0$
  * Standardabweichung bei z-standardisierten Werte:
    * immer SD=1
    * $\bar{x} =0$

---

### <u>Navigation:</u>

* [Einfache-lineare Regression](/einfache-lineare-regression)
