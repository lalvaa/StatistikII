---
title: Messwiederholungs-ANOVA
---

Die Messwiederholungs-ANOVA wird verwendet, wenn **mehrere Messungen an denselben Personen** durchgeführt werden, um zu prüfen, ob sich deren Mittelwerte **über verschiedene Zeitpunkte oder Bedingungen hinweg** signifikant unterscheiden.

Da dieselben Versuchspersonen mehrfach getestet werden, wird die **intersubjektive Streuung kontrolliert**, wodurch **eine höhere Teststärke** erreicht werden kann.

[Normalverteilungsannahme testen](/normalverteilungsannahme-testen)
[Varianzhomogenität bzw. Homoskedastizität](/varianzhomogenitaet-bzw-homoskedastizitaet)

---

### <u>Beispiel:</u>

„Untersucht wird, ob sich der Stresslevel bei denselben Personen über drei Zeitpunkte (vor, während und nach einer Prüfung) unterscheidet.“

* AV: Stresslevel
* UV: Zeitpunkt der Messung
  * Faktorstufe: Zeitpunkt der Messung
    * Vor, während, nach der Prüfung

---

### <u>Hypothesen:</u>

* $H_0: \mu_1 = \mu_2 = \; .; = \mu_p$
  * Die Mittelwerte der Faktoren bei den 3 Faktorstufen unterscheiden sich nicht
* $H_1: \mu_p \overset{\text{mind 1}}{\neq}  \mu_k$
  * Mindestens eine Faktorstufe unterscheidet sich im Mittelwert des Faktors signifikant von einem anderen.

---

### <u>Voraussetzungen:</u>

* AV metrisch skaliert
* Normalverteilte AV
  * Die Werte in allen untersuchten Populationen sind normalverteilt
* Varianzhomogenität
  * Die untersuchten Populationen haben alle die gleiche Varianz
* Unabhängigkeit
  * Alle Daten müssen unabhängig voneinander sein
* Sphärizität
  * Die Varianzen der Differenzen zwischen allen Messzeitpunkten ist gleich
  * Wird mit Mauchly-Test geprüft
  * Wir möchten nicht signifikant bei dem Test sein

\_\_\_-

### <u>Interpretation der Ergebnisse:</u>

* $F-Wert$:
  * Für jeden Effekt (z. B. Zeit, Gruppenzugehörigkeit, Interaktionen) wird ein eigener F-Wert berechnet.
  * Vergleich des F-Werts mit dem kritischen F-Wert:
    * $F_{emp}$ ≥ $F_{krit}$ → signifikant, H_0 wird abgelehnt
    * F ≈ 1
      → kein Effekt
    * F > 1
      → systematischer Effekt stärker als zufällige Varianz
    * F \< 1
      → mehr zufällige Streuung als systematische Unterschiede
  * Interpretation analog zur Einfaktoriellen ANOVA, aber für jeden Effekt einzeln
* $p-Wert$:
  * Für jeden getesteten Effekt wird ein p-Wert berechnet (z. B. Zeit, Gruppe, Interaktion)
  * Vergleich mit α:
    * p ≤ α → Effekt ist signifikant
    * Achtung: Mehrere Tests → α-Fehler-Kumulierung möglich → ggf. Korrekturverfahren
* Effektstärke η²
  * η² klassisch: Anteil der Gesamtvarianz, den ein Effekt erklärt
    * Nachteil: Gesamtvarianz umfasst alle Effekte und Fehlervarianz → verzerrte Schätzung
  * Partielles η²: Anteil der Varianz, den ein Effekt erklärt, unter Ausschluss anderer Effekte
    * Angegeben in %
    * Vergleichbar mit R² bei multipler Regression
    * Für jeden Effekt wird ein eigenes η²_partiell berechnet
    * Interpretation:
      * η²_partiell = 0,01 → kleiner Effekt
      * η²_partiell = 0,06 → mittlerer Effekt
      * η²_partiell = 0,14 → großer Effekt
* Effektgröße r
  * r = √η²_partiell (nur wenn Studiendesign vergleichbar)
  * Interpretation:
    * r = 0,10 → kleiner Effekt
    * r = 0,30 → mittlerer Effekt
    * r = 0,50 → großer Effekt
* Was bedeutet ein signifikanter Test?
  * Signifikanter Haupteffekt (z. B. Zeit):
    * Es gibt Unterschiede zwischen Messzeitpunkten
  * Signifikanter Interaktionseffekt (z. B. Zeit × Gruppe):
    * Der Effekt eines Faktors hängt vom anderen ab
* Post-hoc
  * Zeigt, zwischen welchen Faktorstufen sich die AV unterscheidet
  * 

---

### <u>Jamovi, R Outputs und G\* Power:</u>

* Residuals (Fehlervarianz)
  * Fehlervarianz bzw. Varianz innerhalb der Personen
  * Zeigt, wie stark die Werte einer Person über die Zeit schwanken – also nicht durch den Messzeitpunkt erklärbar
  * Viel Varianz → Modell erklärt wenig
  * Wenig Varianz → Modell erklärt viel
* Quadratsumme (Sum Sq)
  * Haupteffekt (z. B. Zeit):
    * $QS_{\text{Effekt}} = \sum_i (\bar{y}_{i.} - \bar{\bar{y}})^2$
    * Erklärte Streuung durch Effektpunkte
  * Residuals (Fehlervarianz):
    * $QS_{\text{Fehler}} = \sum_{i,j} (y_{ij} - \bar{y}_{i.})^2$
    * Nicht erklärte Varianz (innerhalb der Personen)
* Mittlere Quadratsumme (Mean Sq)
  * Effekt (z. B. Zeit):
    * $MS_{\text{Effekt}} = \dfrac{QS_{\text{Effekt}}}{df_{\text{Effekt}}}$
  * Residuals:
    * $MS_{\text{Fehler}} = \dfrac{QS_{\text{Fehler}}}{df_{\text{Fehler}}}$
* F-Wert
  * $F = \dfrac{MS_{\text{Effekt}}}{MS_{\text{Fehler}}}$
* Jamovi:
  * ![271x155](/assets/mwanojameins.png)
* G\* Power
  * Zeigt die Teststärke (Power)
  * Wahrscheinlichkeit, einen vorhandenen Effekt zu entdecken
  * Wird in Prozent angegeben (z. B. 95 %)
  * Wichtig zur Einschätzung von Stichprobengröße und Effektentdeckung

---

### <u>Vorgehen:</u>

1. Variationen bilden
   * Gesamtvariation (Quadratsumme gesamt)
     * $QS_{\text{gesamt}} = \sum_{i,j} (y_{ij} - \bar{\bar{y}})^2$
     * Abweichung jedes Messwerts vom Gesamtmittelwert über alle Zeitpunkte und Personen
   * Effekt der Messwiederholung (z. B. Zeit)
     * $QS_{\text{Zeit}} = \sum_j n (\bar{y}_{.j} - \bar{\bar{y}})^2$
     * Abweichung der Mittelwerte der Zeitpunkte vom Gesamtmittelwert
   * Fehlervariation (Residuals)
     * $QS_{\text{Fehler}} = \sum_{i,j} (y_{ij} - \bar{y}_{i.} - \bar{y}_{.j} + \bar{\bar{y}})^2$
     * Abweichung der Einzelwerte von Personen- und Zeitmittelwerten
1. Varianzen berechnen

* Systematische Varianz (Zeit)
  * $\sigma^2_{\text{Zeit}} = \dfrac{QS_{\text{Zeit}}}{df_{\text{Zeit}}}$
* Fehlervarianz (Residuals)
  * $\sigma^2_{\text{Fehler}} = \dfrac{QS_{\text{Fehler}}}{df_{\text{Fehler}}}$
* Freiheitsgrade
  * $df_{\text{Zeit}} = k - 1$
  * $df_{\text{Fehler}} = (n - 1)(k - 1)$
  * $k$ = Anzahl Messzeitpunkte, $n$ = Anzahl Personen

1. F-Test berechnen
   * $F = \dfrac{\sigma^2_{\text{Zeit}}}{\sigma^2_{\text{Fehler}}}$
   * Vergleich mit kritischem F-Wert
     * $F_{emp} \ge F_{krit}$ → Signifikant, Nullhypothese wird abgelehnt

---

### <u>Navigation:</u>

* Zurück zu ANOVA:
  * [Zurück zur Übersicht](/anova)
* Voraussetzungspfad:
  * [Voraussetzungen](/messwiederholung)

\#Test
