---
title: Einstichproben T-Test
---

Der Einstichproben t-test vergleicht Mittelwerte (x̄) einer Stichprobe mit einer Konstante (μ).

[Normalverteilungsannahme testen](/normalverteilungsannahme-testen)
[Varianzhomogenität bzw. Homoskedastizität](/varianzhomogenitaet-bzw-homoskedastizitaet)

---

##### <u>Beispiel:</u>

Unterscheidet sich der durchschnittliche Stress-wert von Studierenden an der IPU (x̄) von dem bundesweiten Mittelwert (μ) ?

* **Merkmal (AV)** : Stress-wert
* **H₀**: Es gibt keinen Unterschied
* **H₁**: Es gibt einen Unterschied

---

#### <u>Voraussetzungen:</u>

* Eine Stichprobe
* Merkmal AV
  * Muss in der Grundgesamtheit und Stichprobe Normalverteilt sein
* Messwert AV
  * muss metrisch sein
* Messwerte der Personen
  * müssen voneinander unabhängig sein
  * (Zufalls Stichprobe)

---

#### <u>Konstante μ:</u>

* z.B.: Angenommener Mittelwert der Grundgesamtheit
* oder ein Grenzwert ab dem z.B. psychische Störungen diagnostiziert werden

---

#### <u>Hypothese:</u>

* Gerichtete Hypothese 
  * **H₀**: x̄=μ
  * **H₁**: x̄≠μ
* Ungerichtete Hypothese:
  * **H₀**: x̄=μ
  * **H₁**: x̄ >/\< μ

---

#### <u>Entscheidung:</u>

* \| t<sub>df</sub> | ≥ t<sub>krit</sub>
* oder p ≤ α
* --> signifikant und **H₀** wird abgelehnt (gewünscht meistens)

---

#### <u>Formel:</u>

* t<sub>df</sub> :
  $$t_{df} = \frac{\bar{x} - \mu}{SE} \quad \text{oder} \quad t_{df} = \sqrt{n} \cdot \frac{\bar{x} - \mu}{SD}$$

* df = n-1

* Standardfehler SE
  $$SE = \frac{SD}{\sqrt{n}}$$
  
  * Wie stark der Mittelwert einer Stichprobe vom wahren Mittelwert der Population abweicht
* Standardabweichung SD:
  $$SD = \sqrt{\frac{1}{n - 1} \sum_{i=1}^{n} (x_i - \bar{x})^2}$$
  
  * Wie stark die Werte im durchschnitt von dem Mittelwert abweichen

---

#### Navigation

* Zurück zu T-Tests:
  
  * [Zurück zur Übersicht](/t-tests)
* Zurück zu Voraussetzungen
  
  * [Voraussetzungen](/stichprobenanzahl)

\#Test
