---
title: Mehrfaktorielle ANOVA
---

**Die mehrfaktorielle ANOVA** wird verwendet, wenn der Einfluss von **zwei oder mehr unabhängigen Variablen (Faktoren)** mit mehreren Faktorstufen auf eine **metrische abhängige Variable** untersucht werden soll.

Dabei interessiert nicht nur der **Haupteffekt** jedes einzelnen Faktors, sondern auch, ob es eine **Wechselwirkung (Interaktion)** zwischen den Faktoren gibt, also ob sich die Wirkung eines Faktors abhängig vom Ausprägungsgrad eines anderen Faktors verändert.

Die ANOVA ist ein erweiterter t-test. Auch hier wollen wir die Nullhypothese ablehnen.

* [Normalverteilungsannahme testen](/Voraussetzungstests/normalverteilungsannahme-testen)
* [Varianzhomogenität bzw. Homoskedastizität](/Voraussetzungstests/varianzhomogenitaet-bzw-homoskedastizitaet)

---

### <u>Beispiel:</u>

Eine Forscherin möchte untersuchen, wie sich **Koffeinkonsum (niedrig vs. hoch)** und **Tageszeit (Vormittag vs. Nachmittag)** auf die **Konzentrationsleistung** auswirken.

* **AV**: Konzentrationsleistung
* **UV/Faktor 1**: Koffeinkonsum
  * **Faktorstufen:** niedrig vs mittel vs hoch
* **UV/Faktor 2**: Tageszeit
  * **Faktorstufen:** Vormittag vs. Nachmittag

---

### <u>Zu Untersuchen:</u>

* Haupteffekt
  * Beeinflussen **die einzelnen Faktoren unabhängig voneinander** die abhängige Variable (AV)?
* Interaktionseffekte:
  * Beeinflussen alle Faktoren in Kombination die AV

---

### <u>Hypothesen:</u>

* **H₀ (Für jeden Faktor j):**
  * Die Mittelwerte der Stufen von diesem Faktor unterscheiden sich **nicht**
    * kein Effekt dieses Faktors
  * Anzahl der $H_0 = j \cdot H_0$
* \*\*H₀ (Für alle Interaktionseffekte):
  * Es gibt **keine Wechselwirkung** zwischen 2 oder mehr Faktoren
  * der Effekt von A ist **unabhängig** von den Stufen von B (und umgekehrt).
  * Anzahl abhängig von anzahl der Faktoren
    * bei 3: A×B; A×C; B×C; A×B×C
* $H_1$ (Für jeden Faktor j):
  * Die Mittelwerte der Stufen von diesem Faktor unterscheiden sich
    * Faktor hat Effekt
  * Anzahl $H_1 = H_0$
* $H_1$ (Für alle Interaktionseffekte):
  * Der Effekt eines Faktors **ändert sich abhängig vom anderen /anderen Faktor/-en**
  * Es liegt eine **Interaktion** vor

---

### <u>Voraussetzungen:</u>

* AV metrisch skaliert
* Normalverteilte AV
  * Die Werte in allen untersuchten Populationen sind normalverteilt
* Varianzhomogenität
  * Die untersuchten Populationen haben alle die gleiche Varianz
* Unabhängigkeit
  * Alle Daten müssen unabhängig voneinander sein

\_\_\_-

### <u>Interpretation der Ergebnisse:</u>

* $F-Wert$
  * Für **jeden einzelnen Effekt (Haupteffekte & Interaktionen)** wird **ein eigener F-Wert** berechnet.
  * Vergleich jedes **F-Werts** mit dem entsprechenden **kritischen F-Wert**
    * $F_{emp} \ge F_{krit}$ → **Signifikanz**, $H_0$ wird abgelehnt
    * $F \approx 1$ → **Kein Effekt**
    * $F > 1$ → **Starker Effekt**
    * $F < 1$ → **Zufällige Streuung größer als systematische Unterschiede**
  * Interpretation analog zur Einfaktoriellen ANOVA aber **für jeden Effekt separat**
* $p-Wert$:
  * Wird für **jeden getesteten Effekt** (z. B. Faktor A, B, A×B) berechnet
  * Vergleich mit $\alpha$:
    * $p \le \alpha$ → Effekt ist signifikant
  * Achtung: Viele Tests → **Fehlerrate steigt** → ggf. Korrekturen nötig
* Effektstärke $\eta^2$
  * $\eta^2$ (Eta-Quadrat, klassisch)
    * **Wie viel Prozent der Gesamtvarianz** wird durch *diesen einen Effekt* erklärt?
    * Problem bei Mehrfaktoriellen Designs:
      * Die **Gesamtvarianz** enthält **alle Effekte + Fehlervarianz**
      * → Wenn viele Effekte getestet werden, **„konkurrieren“ sie um Erklärungsanteile**
        → **Schätzung wird verzerrt** (z. B. zu klein)
    * **Sozusagen die %-Anzahl für einen Effekt ohne herauszurechnen wie dieser durch andere Faktoren beeinflusst wird**
  * $\eta^2_{\text{partiell}}$ (partielles Eta-Quadrat)
    * Effektstärke
    * **Wie viel Varianz kann der Effekt erklären**, **unter Ausschluss** der anderen Effekte?
    * %-Angabe wie stark ein einzelner Effekt (Faktor oder Interaktion) die Varianz des Kriteriums erklärt
      * $\eta^2_{\text{partiell}} = 0{,}01$ → kleiner Effekt
      * $\eta^2_{\text{partiell}} = 0{,}06$ → mittlerer Effekt
      * $\eta^2_{\text{partiell}} = 0{,}14$ → großer Effekt
    * Vergleichbar mit **$R^2$ bei multipler Regression** für einen einzelnen Prädiktor
    * **Besser geeignet für mehrfaktorielle Designs**, weil:
      * Unabhängig von der Anzahl anderer Effekte
      * Zeigt **den Einfluss eines Faktors isoliert betrachtet**
      * Vergleichbar zwischen Modellen und Studien
    * Für jeden Effekt (Faktor und Interaktion) wird ein $\eta^2_{partiell}$ berechnet
* Effektgröße r
  * $r=\sqrt{\eta^2_{p}^2}$ wenn Studiendesign vergleichbar ist
  * Zeigt die Größe eines Zusammenhangs oder Unterschieds an
    * $r = 0{,}10$ : kleiner Effekt
    * $r = 0,30$  : mittlerer Effekt
    * $r = 0{,}50$ : großer Effekt
* Was bedeutet ein Signifikanter Test?:
  * **Signifikanter Haupteffekt**:
    * Ein Faktor beeinflusst die AV **unabhängig von den anderen Faktoren**
  * **Signifikanter Interaktionseffekt**
    * Die Wirkung eines Faktors **hängt vom anderen Faktor ab**
* Post-hoc
  * Zeigen **zwischen welchen Stufen eines Faktors** die Unterschiede liegen
  * Für **jeden signifikanten Haupteffekt einzeln**
    * z. B. bei **Faktor A (z. B. Medikament)**: Gruppen A1 vs A2 vs A3
  * **Nicht für Interaktionen geeignet**
    * dort eher: **einfache Haupteffekte analysieren**
  * Wie bei Einfaktoriell:
    * ANOVA: **„Es gibt Unterschiede“**
    * Post-hoc: **„Wo genau sind die Unterschiede?“**

---

### <u>Jamovi, R Outputs und G\* Power:</u>

* Residuals (Fehlervarianz)
  * **Fehlervarianz** bzw. **Varianz innerhalb der Gruppen**
  * Zeigt, **wie stark die Werte innerhalb einer Zelle (Gruppe von Faktorstufenkombinationen)** voneinander abweichen
    * also **nicht durch die Haupt- oder Interaktionseffekte erklärbar**.
    * **Viel Varianz**:  
      → Das Modell erklärt wenig (schlechte Modellpassung)
    * **Wenig Varianz**:  
      → Das Modell erklärt viel (gute Modellpassung)
* Quadratsumme (Sum Sq)
  * **Haupteffekte (einzelne Faktoren)**
    * Erklärte Streuung **durch einzelne Faktoren**
    * Zeigt, **wie stark sich die Mittelwerte der Faktorstufen unterscheiden**
    * Beispiel: Sum Sq von `drug` → Erklärte Varianz durch Medikament
  * **Interaktionseffekte (z. B. A × B)**
    * Zusätzliche erklärte Streuung durch das **Zusammenspiel der Faktoren**
    * Zeigt, ob **der Effekt eines Faktors vom anderen abhängt**
      * Beispiel: `drug * therapy` → Interaktion zwischen Medikament und Therapieform
  * **Residuals (Fehlervarianz)**
    * **Nicht erklärte Varianz**
    * Zeigt, **wie stark die Werte um die Zellenmittelwerte streuen**
    * Nicht durch Haupt- oder Interaktionseffekte erklärbar
* Mittlere Quadratsumme (Mean Sq)
  * **Faktor / Interaktion**
    * Durchschnittlich erklärte Varianz **pro Freiheitsgrad**
    * Gibt an, **wie stark sich die Mittelwerte der Gruppen im Durchschnitt unterscheiden**
  * **Residuals**
    * **Fehlervarianz pro Freiheitsgrad**
    * Zeigt, **wie stark die Einzelwerte innerhalb der Zellen im Durchschnitt abweichen**
    * Grundlage für F-Berechnung
* Jamovi:
  * ![258x95](/assets/manojameins.png)
* R Output:
  * ![326x103](/assets/manor.png)
* G\* Power
  * Zeigt die **Power (Teststärke)** an
    * Wahrscheinlichkeit, einen tatsächlichen Effekt auch wirklich zu entdecken
    * Kann nur für partielle Effektgröße eindeutig bestimmt werden
  * Wird in **Prozent** angegeben (z. B. 95 %)
  * Wichtig für Planung und Interpretation von Studien

---

### <u>Vorgehen:</u>

1. **Variationen bilden**
   * **Gesamtvariation (Quadratsumme Gesamt)**
     * $QS_{\text{gesamt}} = \sum^j\sum^i (y_{ij} - \bar{\bar{y}})^2$
     * Abweichung jedes Messwerts vom Gesamtmittelwert
   * **Haupteffekte & Interaktionseffekte (systematische Variation)**
     * $QS_A$, $QS_B$, $QS_{A \times B}$
       * Abweichung der Zellmittelwerte (z. B. Kombinationen aus A und B) vom Gesamtmittelwert
       * Erklären jeweils die Varianz durch Faktor A, Faktor B und deren Interaktion
   * **Fehlervariation (Residuals)**
     * $QS_{\text{inn}} = \sum (y_{ij} - \bar{y}_{Zelle})^2$
     * Abweichung der Einzelwerte vom jeweiligen Zellmittelwert
     * Kann durch keinen Faktor erklärt werden
1. **Varianzen berechnen**
   * Quadratsummen werden durch die zugehörigen Freiheitsgrade geteilt
   * **Systematische Varianz (für jeden Effekt)**
     * $\sigma^2_{A} = \dfrac{QS_A}{df_A}$
     * $\sigma^2_{B} = \dfrac{QS_B}{df_B}$
     * $\sigma^2_{A \times B} = \dfrac{QS_{A \times B}}{df_{A \times B}}$
   * **Fehlervarianz (Residuals)**
     * $\sigma^2_{\text{inn}} = \dfrac{QS_{\text{inn}}}{df_{\text{inn}}}$
   * **Freiheitsgrade**
     * $df_A = a - 1$
     * $df_B = b - 1$
     * $df_{A \times B} = (a - 1)(b - 1)$
     * $df_{\text{inn}} = N - ab$
       * $a$ = Anzahl Stufen von Faktor A
       * $b$ = Anzahl Stufen von Faktor B
       * $N$ = Gesamtanzahl der Beobachtungen
1. **F-Test berechnen**
   * Für jeden Effekt wird ein separater F-Wert berechnet:
     * $F_A = \dfrac{\sigma^2_A}{\sigma^2_{\text{inn}}}$
     * $F_B = \dfrac{\sigma^2_B}{\sigma^2_{\text{inn}}}$
     * $F_{A \times B} = \dfrac{\sigma^2_{A \times B}}{\sigma^2_{\text{inn}}}$
   * **Vergleich mit kritischem F-Wert**
     * $F_{emp} \ge F_{krit}$  
       → Signifikant, Nullhypothese für den jeweiligen Effekt wird abgelehnt

---

### <u>Navigation:</u>

* Zurück zu ANOVA:
  * [Zurück zur Übersicht](/anova)
* Zurück zu Voraussetzungen:
  * [Voraussetzungen](/faktoren-anzahl)

\#Test
