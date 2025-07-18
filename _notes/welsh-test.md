---
title: Welsh-Test (T-Tests)
---

Der Welsh-Test ist eine Variante des t-Tests für **unabhängige Stichproben**.
Dieser wird verwendet, wenn die Varianzen der beiden Gruppen ungleich sind.

* Verletzung der Varianzhomogenität

[Normalverteilungsannahme testen](/normalverteilungsannahme-testen)

---

### Beispiel:

Gibt es einen Unterschied im Prüfungsstress zwischen Studierenden an zwei Universitäten (Stress-werte streuen unterschiedlich stark) ?

* **Abhängige Variable (AV):** Prüfungsstress
* **Unabhängige Variable (UV):** Universität A oder B
* **H₀**: Es gibt keinen Unterschied
* **H₁**: Es gibt einen Unterschied

---

### <u>Voraussetzungen:</u>

* Normalverteilung:
  * Daten der Grundgesamtheit müssen normalverteilt sein
* Unabhängigkeit
  * Beobachtungen innerhalb einer Gruppe hängen nicht zusammen
  * Keine Stichprobenübergreifende Abhängigkeit

---

### <u>Hypothesen:</u>

* Gerichtet:
  * **H₀**: μ<sub>1</sub> = μ<sub>2</sub>
  * **H₁**: μ<sub>1</sub> ≠ μ<sub>2</sub>
* Ungerichtet:
  * **H₀**: x̄<sub>D</sub> = 0
  * **H₁**: μ<sub>1</sub> >/\< μ<sub>2</sub>

---

### <u>Entscheidung:</u>

* \| t<sub>df</sub> | ≥ t<sub>krit</sub>
* oder p ≤ α
* --> signifikant und **H₀** wird abgelehnt (gewünscht meistens)

---

### <u>Formeln:</u>

* t<sub>df</sub>
  $$
t_{df} = \frac{\bar{x}_1 - \bar{x}_2}{\sqrt{\frac{\hat{\sigma}_1^2}{n_1} + \frac{\hat{\sigma}_2^2}{n_2}}}
$$
  $$
t_{df} = \frac{(\bar{x}_1 - \bar{x}_2)}{SE_{diff}}
$$

* Freiheitsgrade(df)
  
  * wird abgerundet auf die nächste ganze Zahl
    $$
df = \frac{\left( \frac{\hat{\sigma}_1^2}{n_1} + \frac{\hat{\sigma}_2^2}{n_2} \right)^2}{\frac{\left( \frac{\hat{\sigma}_1^2}{n_1} \right)^2}{n_1 - 1} + \frac{\left( \frac{\hat{\sigma}_2^2}{n_2} \right)^2}{n_2 - 1}}
$$

---

### Navigation:

* Zurück zu T-Tests:
  
  * [Zurück zur Übersicht](/t-tests)
* Zurück zu Voraussetzungen
  
  * [Voraussetzungen](/varianzhomogenitaet-ja-nein)

\#Test
