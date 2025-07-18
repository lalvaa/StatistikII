---
title: Kontrastanalyse (ANOVA)
---

Wird verwendet, **wenn ein Effekt in der ANOVA signifikant** ist und man **gezielte Hypothesen** zu bestimmten Gruppenvergleichen hat.

* Anders als der Post-hoc-Test, der **alle Gruppen** miteinander vergleicht, testet die Kontrastanalyse **gezielt vorher definierte Vergleiche**.

Das Ziel ist es Herauszufinden, **welche spezifischen Unterschiede zwischen Gruppen** für den Gesamteffekt verantwortlich sind.

* Beispiel: Testet man 3 Gruppen (A, B, C), kann man z. B. gezielt prüfen:  
  \* „Unterscheidet sich Gruppe A vom Mittelwert aus B und C?“

[Normalverteilungsannahme testen](/normalverteilungsannahme-testen)
[Varianzhomogenität bzw. Homoskedastizität](/varianzhomogenitaet-bzw-homoskedastizitaet)

---

##### <u>Beispiel:</u>

„In der Kontrastanalyse wurde getestet, ob sich bei Medikamenteneinnahme die Gruppe mit einer hohen Dosis (C) signifikant vom Depressions-Durchschnitt der Gruppen Placebo (A) und niedrige Dosis (B) unterscheidet."

* AV: Depression
* UV: Medikament
  * Faktorstufen Medikamenten-Dosis
    * Placebo vs. niedrig vs. hoch

---

##### <u>Wie funktioniert’s?</u>

* Jede Hypothese wird als **Kontrast** formuliert:
  * Man weist den Gruppen **Kontrastkoeffizienten** zu, die sich zu 0 addieren.
  * Beispiel: A = 2, B = –1, C = –1 → Testet A vs. (B und C)
* Es wird dann ein **Kontrast-F-Wert** oder **t-Wert** berechnet.

---

##### <u>Voraussetzung:</u>

* AV metrisch skaliert
* Normalverteilte AV
  * Die Werte in allen untersuchten Populationen sind normalverteilt
* Varianzhomogenität
  * Die untersuchten Populationen haben alle die gleiche Varianz
* Unabhängigkeit
  * Alle Daten müssen unabhängig voneinander sein
* Kontraste müssen **orthogonal** sein, wenn mehrere verwendet werden
  * (d. h. unabhängig voneinander)

---

##### <u>Interpretation der Ergebnisse:</u>

* Kontrastwert
  * Für jeden Kontrast wird ein eigener Wert berechnet
  * Gibt den gewichteten Mittelwertsunterschied zwischen den Gruppen an
  * Ein hoher absoluter Kontrastwert zeigt große Unterschiede entlang der definierten Gewichtung
* t-Wert
  * Der t-Wert ist die Prüfgröße des Kontrasts
  * Vergleich mit dem kritischen t-Wert oder p-Wert
  * $t_{emp} \ge t_{krit}$ → signifikant, Nullhypothese wird abgelehnt
  * $t \approx 0$ → kein Unterschied entsprechend des Kontrasts
* p-Wert
  * Gibt die Wahrscheinlichkeit an, unter der Nullhypothese einen so starken oder stärkeren Unterschied zu finden
  * $p \le \alpha$ → Kontrast ist signifikant
  * $p > \alpha$ → Kontrast nicht signifikant
* Effektstärke r
  * Effektgröße für den Kontrast
  * $r = \sqrt{\dfrac{t^2}{t^2 + df}}$
    * $r = 0{,}10$ → kleiner Effekt
    * $r = 0{,}30$ → mittlerer Effekt
    * $r = 0{,}50$ → großer Effekt
* Was bedeutet ein signifikanter Kontrast?
  * Es besteht ein signifikanter Unterschied genau entlang der definierten Kontraststruktur
  * Nur die geprüfte Hypothese ist abgesichert, nicht andere mögliche Gruppenkonstellationen
  * Interpretation immer bezogen auf den geplanten Kontrast (z. B. Gruppe A + B vs. Gruppe C)

---

##### <u>Jamovi, R Outputs und G\* Power:</u>

* Kontrastwert
  * Gibt die gerichtete Differenz zwischen Gruppenmittelwerten an, basierend auf vorgegebenen Kontrastgewichten
  * Ermöglicht gezielte Hypothesentests (z. B. Gruppe A + B vs. C)
* t-Wert
  * Teststatistik für den Kontrast
  * Zeigt, ob der Unterschied entlang der Kontraststruktur signifikant ist
  * Je größer der Betrag, desto stärker der Unterschied
* p-Wert
  * Gibt an, ob der Kontrast signifikant ist
  * $p \le \alpha$ → Kontrast ist signifikant
  * $p > \alpha$ → Kontrast ist nicht signifikant
* Effektstärke r
  * Zeigt die Größe des Unterschieds entlang des Kontrasts
  * Wird häufig zusätzlich zum t-Wert berechnet
  * $r = \sqrt{\dfrac{t^2}{t^2 + df}}$
* Jamovi
  * Kontraste werden meist unter „Kontrastanalyse“ im ANOVA-Modul angezeigt
  * Ergebnisse beinhalten Kontrastwert, t-Wert, p-Wert und ggf. Effektgröße
* G\* Power
  * Berechnung erfolgt wie bei t-Tests
  * Effektstärke wird über $r$ oder $d$ eingegeben
  * Power zeigt, wie wahrscheinlich ein echter Kontrasteffekt entdeckt wird

---

##### <u>Vorgehen:</u>

1. Kontraste definieren
   * Vorab geplante Gewichtungen zwischen Gruppen (Kontrastgewichte)
   * Beispiel: Gruppe A = -1, Gruppe B = -1, Gruppe C = +2 → C wird mit Mittelwert von A und B verglichen
1. Kontrastwert berechnen
   * $K = \sum c_j \cdot \bar{y}_j$
   * $c_j$ = Kontrastgewicht der Gruppe j
   * $\bar{y}_j$ = Mittelwert der Gruppe j
   * Ergibt den gewichteten Unterschied zwischen Gruppenmitteln
1. Prüfgröße berechnen
   * $t = \dfrac{K}{\sqrt{MS_{\text{Fehler}} \cdot \sum \dfrac{c_j^2}{n_j}}}$
   * $MS_{\text{Fehler}}$ = Fehlervarianz aus ANOVA
   * $n_j$ = Gruppengröße
   * Gibt an, ob der Kontrast signifikant ist
1. Hypothesentest
   * Vergleich mit kritischem t-Wert oder Betrachtung des p-Werts
   * $p \le \alpha$ → signifikanter Unterschied im Kontrast
   * $p > \alpha$ → kein signifikanter Unterschied
1. Interpretation
   * Nur der getestete Kontrast ist interpretierbar
   * Keine Aussage über andere Gruppenvergleiche

---

##### <u>Navigation:</u>

* Zurück zu ANOVA:
  * [Zurück zur Übersicht](/anova)
* Zurück zur Voraussetzungspfad
  * [Gruppenvergleich](/gruppenvergleich)
