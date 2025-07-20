---
title: Einfaktorielle-ANOVA
---

Die Einfaktorielle-ANOVA untersucht, ob sich der Mittelwert **einer Abhängigen Variable** über 2 oder mehr Stufen **eines Faktors (UV)** signifikant unterscheiden. Sie wird auch Varianzanalyse genannt da sie sich auf das Verhältnis der Varianzschätzung die zwischen und innerhalb der Gruppen auftreten, stützt .

* 1 Faktor (UV) und 1 AV

ANOVA = "Analysis of variance"

Die zentrale Fragestellung lautet:  
*Unterscheiden sich die Gruppenmittelwerte signifikant stärker, als durch Zufall zu erwarten wäre?*

Die ANOVA ist ein erweiterter t-test. Auch hier wollen wir die Nullhypothese ablehnen.

[Varianzhomogenität bzw. Homoskedastizität](/varianzhomogenitaet-bzw-homoskedastizitaet)
[Normalverteilungsannahme testen](/normalverteilungsannahme-testen)

---

### <u>Beispiel:</u>

Unterscheiden sich das durchschnittliche Stresserleben von Studierenden aus den Studiengängen Psychologie, Jura und Maschinenbau.

* **AV**: Stresserleben
* **UV/Faktor**: Studiengang
  * **Faktorstufen:** Psychologie, Jura und Maschinenbau (Studiengang)

---

### <u>Hypothesen</u>

* $H_0: \mu_1 = \mu_2 = \; .; = \mu_p$
  * Es gibt keinen Unterschied zwischen den Populationsmittelwerten
* $H_1: \mu_p \overset{\text{mind 1}}{\neq}  \mu_k$
  * Mindestens ein Populationswert unterscheidet sich von den anderen

---

### <u>Voraussetzungen:</u>

* AV metrisch skaliert
* Normalverteilte AV
  * Die Werte in allen untersuchten Populationen sind normalverteilt
* Varianzhomogenität
  * Die untersuchten Populationen haben alle die gleiche Varianz
* Unabhängigkeit
  * Alle Daten müssen unabhängig voneinander sein

---

### <u>Interpretation der Ergebnisse:</u>

* $F-Wert$ :
  * Der F-Wert ist an sich wie der t-Wert
  * Vergleich des F-Werts mit dem kritischen F-Wert
  * $F_{emp}\ge F_{krit}$
    → Signifikant und Nullhypothese wird abgelehnt
  * $F\approx 1$
    * Gruppenzugehörigkeit hat genauso viel Einfluss wie zufällige Varianz innerhalb der Gruppen
    * p-Wert ist hoch
      * Annahme der $H_0$ sehr wahrscheinlich
  * $F>1$ (deutlich)
    * Gruppenzugehörigkeit hat größeren Einfluss auf Variabilität als zufällige Varianz innerhalb der Gruppen
    * p-Wert niedrig
      * Ablehnung der $H_0$ wahrscheinlicher
  * $F<1$ (selten)
    * Gruppenzugehörigkeit hat kleineren Einfluss auf Variabilität als zufällige Fehler
    * p-Wert sehr hoch
      * Annahme der $H_0$ sehr wahrscheinlich
* $p-Wert$:
  * Dieser Wert kann direkt mit dem $\alpha$-Wert verglichen werden
  * $p \le \alpha$
    → Signifikant und Nullhypothese wird abgelehnt
* Effektstärke $\eta^2$
  * Welcher Anteil der Gesamtvarianz der AV durch den Faktor erklärt wird
    * Die Schwankungen der AV kann durch den Faktor zu so viel Prozent erklärt werden ($\eta^2$)
  * Prozentangabe
  * $\eta^2 = \dfrac{QS_{\text{zw}}}{QS_{\text{ges}}} = \dfrac{QS_{\text{Faktor}}}{QS_{\text{Gesamt}}}$
    * $\eta^2=0,01$ Kleiner Effekt (1%)
    * $\eta^2=0,06$ Mittlerer Effekt (6%)
    * $\eta^2=0,14$ Großer Effekt (14%)
  * Wie $R^2$ bei Regression
* Was bedeutet ein Signifikanter Test?:
  * Mindestens eine Faktorstufe unterscheidet sich im Mittelwert der AV signifikant von mindestens einer anderen.
  * Ein signifikanter F-Test zeigt, dass **mindestens eine Gruppe** einen signifikant anderen Mittelwert aufweist.
  * Daraus lässt sich ableiten dass;
    * **Der Faktor hat einen Einfluss auf die AV**
      * Weil **nicht alle Gruppen gleich sind**, ist der Faktor **relevant** für Unterschiede in der AV.
    * **Nicht alle Faktorstufen wirken gleich stark auf die AV.**
      * Es gibt **signifikante Unterschiede** zwischen einzelnen Gruppen
      * Welche genau ist nur durch Post-Hoc heraus findbar
* Post-hoc
  * Aussage:
    * Welche Gruppen sich voneinander unterscheiden
      * nach einem signifikanten ANOVA test
  * ANOVA sagt nur ob es Unterschiede zwischen den Gruppen gibt
    * Post-hoc sagt welche Faktorstufen sich tatsächlich voneinander unterscheiden
  * P-Werte der einzelnen sind hier Aussagegebend
  * Keine Aussage darüber welche Faktorstufe am "besten/schlechtesten" ist
  * Beispiel:
    * ![296x196](/assets/posthoctest.png
  )
    * Anixfree unterscheidet sich signifikant von Joyzepam aber nicht signifikant von Placebo
    * Joyzepam unterscheidet sich signifikant von placebo

---

### <u>Jamovi, R Outputs und G\* Power:</u>

* Residuals
  * Fehlervarianz bzw. Varianz innerhalb der Gruppen
  * **Wie stark die Werte innerhalb einer Gruppe voneinander abweichen** also **nicht** durch den Faktor erklärt werden.
    * Viel Varianz:
      * Das Modell erklärt wenig
    * Wenig Varianz
      * Das Modell erklärt viel
* Quadratsumme (Sum Sq)
  * Faktor:
    * Erklärte Streuung
    * wie stark sich die Gruppenmittelwerte unterscheiden
    * Wird durch den Faktor verursacht
  * Residuals:
    * Unerklärte Streuung
    * Wie stark die Werte um ihren Gruppenmittelwert streuen.
* Mittlere Quadratsumme (Mean SQ)
  * Faktor
    * Durchschnittliche erklärte Streuung zwischen Gruppen
    * Gibt an, wie stark sich die Gruppenmittelwerte im Schnitt unterscheiden
  * Residuals
    * Fehlervarianz
    * Wie stark die Werte innerhalb der Gruppe im Durchschnitt streuen
    * Kann nicht durch den Faktor erklärt werden
* Jamovi:
  * ![232x95](/assets/eanjamovi.png)
* R Output:
  * ![415x132](/assets/eanrout.png)
* G\* Power
  * Zeigt die Power an
  * Wahrscheinlichkeit einen tatsächlichen Effekt zu entdecken wenn dieser da ist
  * Gibt Prozentzahl an

---

### <u>Vorgehen:</u>

1. Variationen bilden
   * Quadratsumme der Gesamtvariation
     * $QS_{\text{gesamt}} = \sum^j\sum^i (y_{ij} - \bar{\bar{y}})^2$
     * Abweichung der einzelnen Messwerte ($y_{ij}$) vom Gesamtmittelwert ($\bar{\bar{y}}$)
     * j = Anzahl der Faktorstufen
     * i = Anzahl der Personen
   * Systematische Variation
     * $QS_{\text{zw}} = \sum^j\sum^i (y_{ij} - \bar{y}_j)^2$
     * Abweichung der einzelnen Messwerte $y_{ij}$ von ihren Gruppenmittelwerten $\bar{y}_i$
   * Fehlervariation
     * $QS_{\text{inn}} = \sum^j (\bar{y_{j}} - \bar{\bar{y}})^2$
       * Quadrierte Abweichung der Gruppenmittelwerte $y_{j}$ zum Gesamtmittelwert $\bar{\bar{y}}$
1. Varianzen bilden
   * Quadratsummen werden durch Freiheitsgrade geteilt
   * Systematische Varianz
     * $$\sigma^2_{zw} = \dfrac{QS_{zw}}{df_{zw}}$$
   * Fehlervarianz
     * $$\sigma^2_{inn} = \dfrac{QS_{innn}}{df_{inn}}$$
   * Freiheitsgrade:
     * $df_{zw} = k-1$
     * $df_{inn} = N-k$
     * N = Alle Gruppen addiert
       * ($n_1+n_2 + ... + n_k)$
     * k = Anzahl der Gruppe
1. F-Test
   * Mit den 2 Varianzen wird dann der F-Test berechnet
   * $F=\dfrac{\text{systematische Varianz}} {\text{Fehlervarianz}}$
   * $$F = \dfrac{\sigma^2_{zw}} {\sigma^2_{inn}}$$
   * $F_{emp}\ge F_{krit}$
     * Signifikant und Nullhypothese wird abgelehnt

---

### <u>Navigation:</u>

* Zurück zu ANOVA:
  * [Zurück zur Übersicht](/anova)
* Zurück zu Voraussetzungspfad:
  * [Voraussetzungen](/faktoren-anzahl)

\#Test
