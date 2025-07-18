---
title: Güte der linearen Regression
---

Die Güte der Regression beschreibt, **wie gut das Regressionsmodell die Streuung der abhängigen Variable erklären kann**.

Sie wird über den **Determinationskoeffizient $R^2$** angegeben

Dieses gibt an wie viel Prozent der Veränderung des Kriteriums (Varianz) durch den/die Prädiktor/-en vorhergesagt werden können.

* Also **wie viel die Regressionsgerade zur Erklärung der abhängigen Variable beiträgt**

---

### <u>Wertebereich:</u>

* $0\le R^2 \le 1$
  * Große Werte = Gute Vorhersage
  * 0,01 sehr geringer Zusammenhang
  * 0,09 mäßiger Zusammenhang
  * 0,25 starker Zusammenhang

---

### <u>Formel für den (multiplen)Determinationskoeffizient R²:</u>

* Einfache Lineare Regression:
  * $R^2=\dfrac{s^2_{\hat{y}}} {s^2_{y}} =\; \; = \dfrac{\text{Regressionsvarianz}}{\text{Gesamtvarianz}}$
* Multiple Lineare Regression:
  * $R^2= 1- \dfrac{SS_{res}} {SS_{tot}}\; \; = \dfrac{\text{ aufgeklärte Varianz }}{\text{Gesamtvarianz}}$

---

### <u>Varianzzerlegung:</u>

* Einfache Lineare Regression
  
  * Gesamtvarianz
    * $s^2_y = \dfrac{\sum{(y_i -\bar{y})^2} }n$
    * $s^2_y = s^2_{\hat{y}} + s^2_e$
    * Gesamtvarianz = aufgeklärte Varianz + Fehlervarianz
    * Um die Unterschiede in der Y-Variable vorherzusagen wird die gesamte Varianz in zwei Anteile zerlegt
  * Aufgeklärte Varianz oder Regressionsvarianz
    * $s^2_{\hat{y}} = \dfrac{\sum(\hat{y}_i -\bar{y})^2}{n}$
  * Fehlervarianz der einfachen linearen Regression
    * $s^2_{e} = \dfrac{ \sum(y -\hat{y}_i)^2}{n}$
* Multiple lineare Regression
  
  * Gesamtvarianz
    * $SS_{tot} = \sum { (Y_i - \bar{Y}_i) }^2$
  * Aufgeklärte Varianz
    * $SS_{res} = \sum { (Y_i - \hat{Y}_i) }^2$

---

### <u>Standardschätzfehler (SE):</u>

* Gibt an wie stark die Werte um die Regressionsgerade streuen
* $SE = \sqrt {\dfrac{ \sum(y -\hat{y}_i)^2}{n - k - 1}} \;\;=\; \; \sqrt {s^2_{e}}$
* Wurzel der Fehlervarianz
* Je kleiner desto besser die Vorhersagequalität

---

### <u>Navigation:</u>

* Einfache Lineare Regression
  * [Einfache-lineare Regression](/einfache-lineare-regression)
* Multiple lineare Regression:
  * [Multiple Lineare Regression](/multiple-lineare-regression)
