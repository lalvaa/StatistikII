---
title: Einfache Lineare Regression
---

Die einfache lineare Regression prüft den Zusammenhang zwischen **einer unabhängigen Variable (UV)** und **einer abhängigen Variable (AV)**, um den Einfluss der UV auf die AV vorherzusagen.

Für die Vorhersage wird eine Regressionsgerade benutzt wodurch man Vorhersagen treffen kann. Hinterher wird noch die Güte berechnet um eine Aussage darüber zu treffen wie gut die Regressionsgerade ist

* Idr. möchte man generalisierbare Aussagen über die gesamte Population ableiten (nur möglich wenn die Daten aus einer Stichprobe stammen, nicht wenn die Daten nur für eine Person gelten)

[Güte der linearen Regression](/guete-der-linearen-regression)
[Regressionsgerade; Einfache-lineare Regression](/regressionsgerade-einfache-lineare-regression)
[Normalverteilungsannahme testen](/Voraussetzungstests/normalverteilungsannahme-testen)
[Varianzhomogenität bzw. Homoskedastizität](/Voraussetzungstests/varianzhomogenitaet-bzw-homoskedastizitaet)

---

### <u>Beispiel:</u>

„Lässt sich der Prüfungserfolg durch die Lernzeit vorhersagen?“

* **UV (Prädiktor):** Lernzeit
* **AV (Kriterium):** Prüfungserfolg

---

### <u>Hypothesen:</u>

* $H_0:\beta_1 =0$
  * Der Prädiktor hat keinen Einfluss auf das Kriterium
* $H_1: \beta_1 \neq 0$  (ungerichtet)
* $H_1: \beta_1 >/< 0$  (gerichtet)
  * Wir möchten die H<sub>0</sub> ablehnen um zu Beweisen, dass die UV einen signifikanten Einfluss auf die AV hat
  * Positiv oder negativer Einfluss
  * Relativ unwichtig da wir wsh nur mit Jamovi Outputs arbeiten werden

---

### <u>Interpretation der Ergebnisse:</u>

* $R^2$ (Güte der linearen Regression):
  * Prozentangabe
  * Bsp.: Wie gut lässt sich das Kriterium durch den Prädiktor vorhersagen
* $p$-Wert des Prädiktors (p-Wert des t-Tests):
  * $p\le \alpha$ --> signifikant
  * Bsp.: Hat der Prädiktor einen signifikanten Einfluss auf das Kriterium
  * **Der Prädiktor** hat einen **signifikanten Einfluss** auf das **Kriterium** — und dieser Zusammenhang **ist auch in der Population zu erwarten**, nicht nur in der Stichprobe.
* t-Wert
  * $t_{emp} \ge t_{krit}$ --> signifikant
  * df:
    * $df = n - k - 1$
      * k =  Anzahl der Prädiktoren (hier 1--> df = n-2)
* F-test
  * Hier entspricht der F-Wert dem Quadrat des t-Werts, da es nur einen Prädiktor gibt:
    → $F = t^2$
    → $F_{emp} \ge F_{krit}$
    → Signifikant
    → Ein signifikanter F-Test bedeutet:
    → Der **Prädiktor erklärt signifikant Varianz**
* Intercept: $b_0 /a_{yx}$ oder auch Y-Achsenabschnitt
  * Der Wert des Kriteriums wenn der Prädiktor 0 ist
  * Der Intercept ist ebenfalls ein geschätzter Regressionskoeffizient und hat einen eigenen p-Wert.
    * Allerdings ist seine Signifikanz **nicht entscheidend** für die Aussage des Regressionsmodells.
  * Bei nicht Signifikanz des Intercepts:
    * Wir können nicht sicher sagen welchen Wert das Kriterium hat wenn der Prädiktor 0 ist.
    * ABER: Prädiktor und Gesamtmodell können trotzdem vollkommen sinnvoll und signifikant sein
* Meist wird nach dem $R^2$-Wert oder p-Wert des Prädiktors gefragt

---

### <u>Jamovi Output:</u>

* Dieser wird hier nur als Jamovi output angegeben und muss nicht selbst berechnet werden.

* Variablen in Jamovi
  
  * AV = Kriterium = Dependent Variable
  * UV = Prädiktor = Covariate
  * R = Korrelation zwischen Vorhergesagtem und tatsächlichem Wert
    * Besser gesagt wie eng liegen die Werte an der Regressionsgerade
    * Bei hoher Streuung der Residuen ist R relativ kleiner bei kleiner Streuung relativ hoch
    * $R = \; \beta \; = \; r_{xy}$  nur bei einfacher linearer Regression
      * Das z-standardisierte Regressionsgewicht ($\beta$)entspricht der Korrelation zwischen dem Prädiktor und Kriterium
  * $R^2$
    * Bestimmtheitsmaß (%) wie viel der Varianz des Kriteriums durch den Prädiktor erklärt werden kann
  * $SE$
    * Wie stark schwankt der geschätzte Wert
  * t-Wert
    * $t_{emp}$-Wert des Prädiktors
  * Intercept: $b_0 /a_{yx}$ oder auch Y-Achsenabschnitt
    * Der Wert des Kriteriums wenn der Prädiktor 0 ist
* Beispiel in Jamovi:
  
  * ![375x198](_notes/Tabelle-Jamovi-ELR.png)
  * "Hängt Dans Grumpyness mit seinem Schlafmangel zusammen?"
    * UV/Prädiktor/dan.sleep:
      * Mit jeder zusätzlichen Stunde Schlaf reduziert sich Dans Grumpyness im Durchschnitt um 8,94 Punkte.
      * Signifikanz des Prädiktors p:
        * Der p-Wert des Prädiktors gibt an wie/ob signifikant der Prädiktor mit dem Kriterium Zusammenhängt
        * Hier: Schlaf und Grumpyness haben einen sehr hohen signifikanten negativen Zusammenhang
      * -->Mehr Schlaf=Weniger Grumpyness
    * Intercept: $b_0 /a_{yx}$
      * Wenn Dan 0 Stunden schläft, wird ein Grumpyness-Wert von 125,96 vorhergesagt.
    * $R^2$ = 0,82
      * 82% der Schwankungen in Dans Grumpyness lassen sich durch seine Schlafdauer erklären
      * Nur 18% des Kriteriums werden durch andere im Modell nicht enthaltende Faktoren beeinflusst
    * $R$ = 0,9
      * Die Korrelation zwischen dem Prädiktor und dem Kriterium beträgt 0,9
    * Wir können hier nur Aussagen über Dan machen nicht eine Population da wir nicht eine Stichprobenmessung durchgeführt haben sondern nur Werte von Dan erhoben haben

---

### <u>Voraussetzungen</u>

* Unabhängigkeit
  * Werte der einzelnen Personen müssen unabhängig voneinander sein
* Lineare Beziehung
  * Der Zusammenhang zwischen dem Erwartungswert des Kriteriums und des Prädiktors muss in der Population linear sein
  * Gegeben durch eine Gleichung
    * $E(y\;|\; x_1 , ... ,x_k) = \beta_{0} + \beta_1 \cdot x_1 \; + ... + \; \beta_k \cdot x_k$
  * Lineare Zusammenhänge = Wenn x-Werte steigen/sinken, steigen/sinken y
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
    * Verteilung der Residuen zeigt ob Homoskedastizität gegeben ist
    * Z.B.: Durch Grafische Darstellung
    * ![254x84](_notes/Arrayverteilung.png)

---

### <u>Residuen:</u>

Abweichungen zwischen den tatsächlichen Werten und den vom Regressionsmodell vorhergesagten Werten

---

### <u>Navigation:</u>

* Zurück zu Zusammenhangsanalyse:
  * [Zurück zur Übersicht](/lineare-regression)
* Zurück zu Voraussetzungen:
  * [Voraussetzungen](/anzahl-der-praediktoren)

\#Test
