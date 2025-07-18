---
title: T-Test für 2 unabhängige Stichproben
---

Der t-Test für 2 unabhängige Stichproben prüft ob ein Unterschied in der UV einen Unterschied in der AV herbeiführt.

[Normalverteilungsannahme testen](/normalverteilungsannahme-testen)
[Varianzhomogenität bzw. Homoskedastizität](/varianzhomogenitaet-bzw-homoskedastizitaet)

---

##### <u>Beispiel:</u>

Gibt es einen Unterschied im Stressniveau zwischen Studierenden die regelmäßig Sport treiben und welche die keinen Sport treiben?

* **Abhängige Variable**: Stressniveau
* **Unabhängige Variable**: Sport oder kein Sport
* **H₀**: Es gibt keinen Unterschied
* **H₁**: Es gibt einen Unterschied

---

##### <u>Voraussetzungen:</u>

* Normalverteilung:
  * Daten der Grundgesamtheit müssen normalverteilt sein
* Unabhängigkeit
  * Beobachtungen innerhalb einer Gruppe hängen nicht zusammen
  * Keine Stichprobenübergreifende Abhängigkeit
* Varianzhomogenität/Homoskedasität:
  * Die Varianzen beider Gruppen sind gleich

---

##### <u>Hypothesen:</u>

* Gerichtet:
  * **H₀**: μ<sub>1</sub> = μ<sub>2</sub>
  * **H₁**: μ<sub>1</sub> ≠ μ<sub>2</sub>
* Ungerichtet:
  * **H₀**: x̄<sub>D</sub> = 0
  * **H₁**: μ<sub>1</sub> >/\< μ<sub>2</sub>

---

##### <u>Entscheidung:</u>

* \| t<sub>df</sub> | ≥ t<sub>krit</sub>
* oder p ≤ α
* --> signifikant und **H₀** wird abgelehnt (gewünscht meistens)

---

##### <u>Formeln:</u>

* t<sub>df</sub> für n<sub>1</sub>=n<sub>2</sub>:
  $$t_{df} = \frac{\bar{x}_1 - \bar{x}_2}
{\sqrt{ \frac{\hat{\sigma}_1^2}{n_1} + \frac{\hat{\sigma}_2^2}{n_2} }} 
\quad$$
* t<sub>df</sub> für n<sub>1</sub>≠n<sub>2</sub>

$$t_{df} = \frac{\bar{x}_1 - \bar{x}_2}
{\sqrt{ \left( \frac{1}{n_1} + \frac{1}{n_2} \right) 
\cdot \frac{(n_1 - 1)\cdot \hat{\sigma}_1^2 + (n_2 - 1) \cdot \hat{\sigma}_2^2}{n_1 + n_2 - 2} }}
$$

* Freiheitsgrade (df):
  $$\quad df = n_A + n_B - 2$$

---

##### Navigation:

* Zurück zu T-Tests
  
  * [Zurück zur Übersicht](/t-tests)
* Zurück zu Voraussetzungen:
  
  * [Voraussetzungen](/varianzhomogenitaet-ja-nein)

\#Test
