---
title: T-Tests für Abhängige Stichproben
---

Der t-Test für Abhängige Stichproben prüft ob sich die Mittelwerte von 2 Stichproben signifikant voneinander unterscheiden.

[Normalverteilungsannahme testen](/normalverteilungsannahme-testen)
[Varianzhomogenität bzw. Homoskedastizität](/varianzhomogenitaet-bzw-homoskedastizitaet)

---

### Beispiel:

Gibt es einen Unterschied im durchschnittlichen Stressniveau von Studierenden vor und nach einer Aufmerksamkeitsübung?

* Merkmal (AV):
  * Stress-wert
* Unabhängige Variable (UV):
  * Zeitpunkt der Messung (t<sub>1</sub> / t<sub>2</sub>)
* **H₀**: Es gibt keinen Unterschied
* **H₁**: Es gibt einen Unterschied

---

### <u>Abhängigkeit aufgrund von:</u>

* Messwiederholung
* 2 verschiedene Messinstrumente
  * Jede Person durchläuft 2 Testungen
* Inhaltliche Gründe
  * 2 Personen werden zu einem Beobachtungspaar
  * z.B. Eltern-Kind-Dyaden

---

### <u>Voraussetzungen:</u>

* Normalverteilung
  * Daten der Grundgesamtheit sind normalverteilt
* Unabhängigkeit:
  * Beobachtungen innerhalb einer Gruppe hängen nicht zusammen
  * Keine Stichprobenübergreifende Abhängigkeit
* Varianzhomogenität/Homoskedasität:
  * Die Varianzen beider Gruppen sind gleich

---

### <u>Hypothesen:</u>

* Gerichtet:
  * **H₀**: x̄<sub>D</sub> = 0
  * **H₁**: x̄<sub>D</sub> ≠ 0
* Ungerichtet:
  * **H₀**: x̄<sub>D</sub> = 0
  * **H₁**: x̄<sub>D</sub> >/\< 0

---

### <u>Entscheidung:</u>

* \| t<sub>df</sub> | ≥ t<sub>krit</sub>
* oder p ≤ α
* --> signifikant und **H₀** wird abgelehnt (gewünscht meistens)

---

### <u>Formeln:</u>

* t<sub>df</sub> :
  $$t_{df} = \frac{\bar{x_{D}}}{SE_{D}} \quad \text{oder} \quad t_{df} = \sqrt{n} \cdot \frac{\bar{x_{D}}}{SD_{D}}$$

* 

* Mittelwert:
  $$\bar{x_{D}}= \bar{x_{1}} - \bar{x_{2}}$$
* Standardfehler SE
  $$SE_D = \frac{\hat{\sigma_{D}}}{\sqrt{N}}$$
* Varianz:
  $$\hat{\sigma}_{D} = \sqrt{ \frac{ \sum_{i=1}^{n} (x_{Di} - \bar{x}_{D})^2 }{N - 1} }$$
* Freiheitsgrade (df) = n-1 (n-Paare)

---

### Navigation:

* Zurück zu Stichproben:
  
  * [Zurück zur Übersicht](/t-tests)
* Zurück zu Voraussetzungen:
  
  * [Voraussetzungen](/abhaengigkeit-nvt)

\#Test
