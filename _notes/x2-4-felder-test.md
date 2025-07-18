---
title: Chi-Quadrat 4-Felder Test
---

Der $x^{2}$-4 Felder Test wird für 2 nominal skalierte Variablen mit jeweils 2 Ausprägungen durchgeführt.

Es wird geprüft ob zwischen beiden Merkmalen ein Zusammenhang besteht und ob die beobachtete Häufigkeit signifikant von der erwarteten Häufigkeit abweicht.

* Hierbei entspricht die erwartete Häufigkeit einer Verteilung in der die Variablen nicht zusammenhängen
* der **Chi-Quadrat 4-Felder-Test** ist gewissermaßen das **nicht-parametrische Gegenstück zum t-Test für unabhängige Stichproben**, **aber für kategoriale Variablen**.

---

### <u>Beispiel:</u>

„Unterscheidet sich die Prüfungsangst (ja/nein) zwischen Studierenden aus Bachelor- und Masterstudiengängen?“

* **UV:** Studiengang (Bachelor vs. Master)
* **AV:** Prüfungsangst (ja / nein)

---

### <u>Hypothesen:</u>

* H<sub>0</sub>: zwischen den 2 Gruppen besteht kein Zusammenhang in der Population
  * Häufigkeit bzw. Anteile sind gleich
* H<sub>1</sub>: Zwischen den Variablen besteht ein Zusammenhang in der Population
  * Wir möchten signifikant werden um zu beweisen das es einen Unterschied zwischen den 2 Gruppen gibt

---

### <u>Voraussetzung:</sub>

* Nominalskalierte Variable

---

### <u>Entscheidung:</u>

* ${x_{emp}}^2 > {x_{krit}}^2$
* $\alpha \ge p$
  * Signifikant und Nullhypothese wird abgelehnt

---

### <u>Prüfgröße x²:</u>

* ${x_{emp}}^2 = \sum_{i=1}^{k} \sum_{j=1}^{l} \dfrac{ (n_{bij} - n_{eij})^2}{n_{eij}}$
  * $n_{bij}$ = Anzahl beobachteter Häufigkeit der Merkmalskombination ij
  * $n_{ej}$ = Anzahl der erwartete Häufigkeit der Merkmalskombination ij
  * k = Anzahl der Stufen des Merkmals A
  * l = Anzahl der Stufen des Merkmals B
  * df = k-1
    ![285x336](_notes/x2-4-Felder-Test-2.png)![342x107](_notes/x2-4-Felder-Test-1.png)

---

### Navigation:

* Zurück zu Chi-Quadrat-Tests:
  
  * [Zurück zur Übersicht](/chi-quadrat-tests)
* Zurück zu Voraussetzungen:
  
  * [Voraussetzungen](/variablen-anzahl)

\#Test
