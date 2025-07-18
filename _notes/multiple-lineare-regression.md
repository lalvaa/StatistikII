---
title: Multiple Lineare Regression
---

Die multiple lineare Regression untersucht den gleichzeitigen Einfluss **mehrerer unabhängiger Variablen (UVs)** auf **eine abhängige Variable (AV)**, um komplexere Vorhersagen zu ermöglichen.

Für die Vorhersage wird eine Regressionsgerade benutzt.

Anschließend kann man noch die Güte der Multiplen Linearen Regression berechnen , um eine Aussage darüber zu treffen wie gut die Regressionsgerade die Werte hervorsagt.

[Güte der linearen Regression](/guete-der-linearen-regression)
[Regressionsgerade; Multiple-lineare Regression](/regressionsgerade-multiple-lineare-regression)
[Normalverteilungsannahme testen](/normalverteilungsannahme-testen)
[Multikollinearität überprüfen](/Multikollinearitaet-ueberpruefen)
[Ausreißer überprüfen](/ausreisser-ueberpruefen)
[Varianzhomogenität bzw. Homoskedastizität](/varianzhomogenitaet-bzw-homoskedastizitaet)

---

##### <u>Beispiel:</u>

„Lässt sich der Prüfungserfolg durch Lernzeit, Motivation und Schlafdauer vorhersagen?“

* **UVs (Prädiktoren):** Lernzeit, Motivation, Schlafdauer
* **AV (Kriterium):** Prüfungserfolg

---

##### <u>Hypothesen</u>

* Es gibt 2 Unterschiedliche Arten der Hypothesen für die multiple lineare Regression

1. <u>Gesamtmodell-Hypothesen:</u>
   * $H_0:\beta_1=\beta_2 = ... = \beta_k = 0$
     * Alle Regressionskoeffizienten sind gleich null
     * (Nicht Intercept)
   * $H_1:\text{ Mindestens ein } \beta_i \neq 0$
     * Mindestens ein Regressionskoeffizient ist nicht null
   * Hiermit wird getestet ob das Modell insgesamt signifikant ist
1. <u>Einzelhypothesen:</u>
   1. $H_0:\beta_j = 0$
      * Prädiktor j hat keinen Einfluss auf das Kriterium
   * $H_1 : \beta_j \neq 0$
     * Prädiktor j hat Einfluss auf das Kriterium
   * Hiermit wird getestet ob ein einzelner Prädiktor UV einen signifikanten Einfluss auf die AV hat

---

##### <u>Interpretation der Ergebnisse:</u>

* $R^2$ (Güte der linearen Regression):
  * Multipler Determinationskoeffizient
  * Prozentangabe
  * Bsp.: Wie gut lässt sich das Kriterium durch die Prädiktoren vorhersagen
* $p$-Wert der einzelnen Prädiktoren (p-Wert des t-Tests):
  * $p\le \alpha$ --> signifikant
  * Gelten  **jeweils für einzelne Prädiktoren**
  * Bsp.: Hat der Prädiktor einen signifikanten Einfluss auf das Kriterium
    * **Der Prädiktor** hat einen **signifikanten Einfluss** auf das **Kriterium** — und dieser Zusammenhang **ist auch in der Population zu erwarten**, nicht nur in der Stichprobe.
* t-Wert der einzelnen Prädiktoren
  * $t_{emp} \ge t_{krit}$ --> signifikant
    * **Dieser Prädiktor** hat einen **signifikanten Einfluss** auf das **Kriterium** — und dieser Zusammenhang **ist auch in der Population zu erwarten**, nicht nur in der Stichprobe.
  * df:
    * $df = n - k - 1$
      * k =  Anzahl der Prädiktoren
      * n = Anzahl der Datenerhebung (bei 30 Datenerhebungen pro Prädiktor n=30)
        * (nicht $n= n_1 + n_2 +...+n_k$)
        * auch df für F-Test
* F-Test:
  * Entscheidet ob das gesamte Modell signifikant ist (mit allen Prädiktoren)
  * Der F-Wert an sich ist wie der t-wert
    * Vergleich von $F_{emp} \ge F_{krit}$ → signifikant
  * P-Wert
    * Dieser gibt an ob das Modell signifikant ist oder nicht
    * Bei Signifikanz:
      * Alle Prädiktoren (das Modell) erklären gemeinsam die Schwankungen des Kriteriums
  * Ein signifikanter F-Test bedeutet:
    * → Das **Modell erklärt signifikant Varianz**
    * → Aber: **Welche Prädiktoren** genau dafür verantwortlich sind, zeigen **nur die t-Tests / p-werte**
  * F-Test beantwortet: "Ist das Modell sinnvoll?"
  * t-Tests beantworten: "Wer trägt zur Vorhersage bei?"
  * Wir können aber ohne weitere Testung nicht sagen, ob z.b. ein Prädiktor der nicht signifikant ist nicht trzdm mit das Kriterium beeinflusst
    * Z.b.: durch Interaktionseffekte mit anderen Prädiktoren
* $\beta_k$
  * Die z-standardisierte Regressionsgewichte ($\beta_k$) bei der mehr-faktoriellen linearen Regression entsprechen den einzelnen z-Standardisierten Regressionsgewichten
  * $\hat{z}_{yi} = \dfrac{x_i - \bar{x}}{SD}$
* Intercept: $b_0 /a_{yx}$ oder auch Y-Achsenabschnitt
  * Der Wert des Kriteriums wenn die Prädiktoren 0 sind
  * Der Intercept ist ebenfalls ein geschätzter Regressionskoeffizient und hat einen eigenen p-Wert.
    * Allerdings ist seine Signifikanz **nicht entscheidend** für die Aussage des Regressionsmodells.
  * Bei nicht Signifikanz des Intercepts:
    * Wir können nicht sicher sagen welchen Wert das Kriterium hat wenn die Prädiktoren 0 sind.
    * ABER: Prädiktoren und Gesamtmodell können trotzdem vollkommen sinnvoll und signifikant sein
* Meist wird nach dem $R^2$-Wert oder p-Wert der Prädiktoren gefragt

---

##### <u>Jamovi Output:</u>

* Wir werden meist einen Jamovi Output bei der Klausur bekommen welchen wir dann interpretieren müsse

* Variablen in Jamovi
  
  * AV = Kriterium = Dependent Variable
  * UV = Prädiktoren = Covariate
  * R = Korrelation zwischen Vorhergesagtem und tatsächlichem Wert
    * Besser gesagt wie eng liegen die Werte an der Regressionsgerade
    * Bei hoher Streuung der Residuen ist R relativ kleiner bei kleiner Streuung relativ hoch
  * $R^2$
    * Bestimmtheitsmaß (%) wie viel der Varianz des Kriteriums durch die Prädiktoren erklärt werden können
  * $SE$
    * Gibt an wie stark die geschätzten Regressionsgewichte streuen
  * t-Wert
    * $t_{emp}$-Wert der einzelnen Prädiktoren
  * F-Wert
    * Ist das gesamte Modell signifikant unter Betrachtung aller Prädiktoren
  * Intercept: $b_0 /a_{yx}$ oder auch Y-Achsenabschnitt
    * Der Wert des Kriteriums wenn die Prädiktoren 0 sind
* Beispiel in Jamovi:
  
  * ![395x180](_notes/Tabelle-Jamovi-MLR.png)
  * "Hängt Dans Grumpyness mit seiner Menge an Schlaf und der Menge an Schlaf zusammen die sein Baby schläft?"
    * UV/Prädiktor/dan.sleep:
      * Signifikanz des Prädiktors:
        * Sehr hohe Signifikanz
          → dan.sleep hat einen negativen Zusammenhang mit dan.grump
          → Mehr Schlaf = Weniger Grumpyness
      * Mit jeder zusätzliche Stunde schlaf reduziert sich Dans Grumpyness um $\approx 8,95$ Punkte
    * UV/Prädiktor/baby.sleep:
      * Signifikanz des Prädiktors:
        * Keine Signifikanz
          → baby.sleep hat keinen Zusammenhang mit dan.grump
    * Intercept: $b_0 / a_{yx}$ oder auch Y-Achsenabschnitt
      * Wenn Dan 0 Stunden schläft wird ein Grumpyness-Wert von $\approx 125,966$ vorhergesagt
    * $R^2$ = 0,816
      * 81,6% der Schwankungen in Dans Grumpyness lassen sich durch beide Prädiktoren erklären
      * 18,4% werden durch andere nicht im Modell erhaltene Faktoren beeinflusst
    * $R$ = 0.903
      * Die Korrelation zwischen den Prädiktoren und dem Kriterium
    * Wir können nur Aussagen über Dan machen nicht die gesamte Population, da wir keine Stichprobenmessung durchgeführt haben

---

##### <u>Voraussetzungen</u>

* Unabhängigkeit
  * Werte der einzelnen Personen müssen unabhängig voneinander sein
* Lineare Beziehung
  * Der Zusammenhang zwischen dem Erwartungswert des Kriteriums und des Prädiktors muss in der Population linear sein
  * Gegeben durch eine Gleichung
    * $E(y\;|\; x_1 , ... ,x_k) = \beta_{0} + \beta_1 \cdot x_1 \; + ... + \; \beta_k \cdot x_k$
  * Lineare Zusammenhänge = Wenn x-Werte steigen/sinken, steigen/sinken y -Werte
  * ![277x199](_notes/Nicht-lineare-Zusammenhaenge.png)
* Metrisches Skalenniveaus des Kriteriums
  * AV muss Metrisch skaliert sein (Intervall / Verhältnis)
  * UV kann beliebiges Skalenniveau besitzen
* Normalverteilung der Residuen
  * Die Fehlerwerte sind normalverteilt
  * Kriterium und Prädiktor müssen nicht NVT sein es hilft aber
* Homoskedastizität der Residuen
  * Die Varianz der Residuen ist an allen Stellen von x gleich groß
    * Varianz der Residuen: $\sigma^2_{e}$
  * "Fehler sind überall gleich verteilt, unabhängig vom Wert des Pradiktoren"
  * Überprüfung durch Arrayverteilung
    * Verteilung der Residuen (Z.B. Grafisch)
    * ![254x84](_notes/Arrayverteilung.png)
* Keine Multikollinearität
  * Die UVs dürfen nicht stark miteinander korrelieren
* Additivität
  * Der kombinierte Effekt der UVs auf die AV ist additiv
  * Kein Interaktionseffekt ohne Modifikation im Modell

---

##### <u>Supressoreffekt:</u>

* Ein Prädiktor der kaum oder gar nicht mit dem Kriterium korreliert allerdings trzdm. die Vorhersage verbessert
  * Aufgrund von starker Korrelation mit einem anderen Prädiktor
* $R^2_{y,12} > r^2_{y1}+r^2_{y2}$
  * Die Summe der einzelnen Korrelationen (r²) ist kleiner als R²
* Ein Supressor hat häufig ein auffallend hohes Regressionsgewicht obwohl die einfache Korrelation mit dem Kriterium niedrig/null ist

---

##### <u>Navigation:</u>

* Zurück zu Lineare Regression:
  * [Zurück zur Übersicht](/lineare-regression)
* Zurück zu Voraussetzungspfad
  * [Voraussetzungen](/anzahl-der-praediktoren)

\#Test
