---
title: Berechnung der Regressionsgerade für die Multiple lineare Regression
---

**Die Regressionsgerade** ist eine mathematische Gerade, die den Zusammenhang zwischen einer oder mehreren unabhängigen Variablen (Prädiktoren) und einer abhängigen Variablen (Kriterium) beschreibt und zur Vorhersage des Kriteriumswerts dient.

---

##### <u>Vorgehen:</u>

* Regressionsgerade aufstellen
  * $\hat{y}_i = b_{1} + x_{1i} \;+\; b_{2} \cdot x_{2i} \; + ... + \; b_{k} \cdot x_{ki} + b_0$
    * ($\hat{y}_i = b_0 + \sum_{1}^{k} b_k\cdot x_{ki}$ )
    * k =Anzahl der Prädiktoren
* Regressionskoeffizienten berechnen
  * $b_{yx_k} = \dfrac{cov(x,y)}{s^2_{x}}$
    * $cov(x,y) = \frac{1}{n \text{ ; } n - 1} \cdot \sum(x_i - \bar{x})\cdot (y_i - \bar{y})$
      * n für Stichprobe
      * n-1 für Population
  * $b_0 = \bar{Y} - b_1 \cdot \bar{X}_1 - b_2 \cdot \bar{X}_2 - \; ... \; - b_k \cdot \bar{X}_k$
    * $a_{yx}$ in der Regressionsgerade}
    * wird auch Intercept genannt

---

##### <u>Vorhersage:</u>

* Aufgrund der Regressionsgerade kann man eine Vorhersage treffen
  * Z.B.: 5 Stunden Lernzeit und 3 Stunden gespielt
    * x = 5
    * $\hat{y} = b_{yx_1} \cdot 5 \;+\; b_{yx_2} \cdot 3 + b_{0}$
    * $\hat{y}$: Sagt nun hervor wie viel Prüfungsangst jemand hat wenn diese Person 5 Stunden gelernt hat

---

##### <u>Z-Standardisierung:</u>

* Z-Standardisierung der Werte
  * $z_i  = \dfrac {x_i - \bar{x}} {SD}$
  * Dies sind die $x_{ki}$ - Werte (nicht Regressionsgewichte)
* Standardisierung der Regressionsgewichte b
  $$\beta_1 = \dfrac { r_{yx_1} - r_{yx_2} \cdot r_{x_1 x_2} } {1- r^2_{x_1 x_2}} \; \text{ ; } \; \beta_2 = \dfrac { r_{yx_2} - r_{yx_1} \cdot r_{x_1 x_2} } {1- r^2_{x_1 x_2}}$$
  * Intercept $b_0$ fällt weg (=0)
  * Bei mehr Regressionsgewichten mit Matrizenrechnung (müssen wir nicht können)
  * Wenn Prädiktoren nicht untereinander korrelieren
    * $r_{x_1 x_2}  = 0 \text{ ; } r^2_{x_1 x_2}  = 0$
    * --> $\beta_i =  r_{yi}$ alle Regressionsgewichte entsprechen dem zugehörigem Korrelationswert
    * Sehr unwahrscheinlich
* Grund:
  * Vergleichbarkeit:
    * $\beta$-Werte zeigen, welcher Prädiktor den stärkeren Einfluss hat
  * Effektstärke:
    * $\beta$ interpretierbar ähnlich wie $r$
  * Mathematische Vorteile:
    * hilfreich bei Interaktionstermen & Multikollinearität
  * Nicht geeignet für echte Vorhersagen → dafür $b$-Werte verwenden

---

##### <u>Navigation:</u>

* [Multiple Lineare Regression](/multiple-lineare-regression)
