---
title: Einstichproben z-Test
---

Der 1-Stichprobentest für Korrelation prüft, ob die beobachtete Korrelation zweier Variablen in einer Stichprobe signifikant von einem vorgegebenen theoretisch angenommenen Populationswert (ρ<sub>0</sub>) unterscheidet.

Hierbei wird die empirisch gefundene Korrelation **r** zunächst mittels **Fisher-Z-Transformation** transformiert, um sie **vergleichbar** mit dem theoretischen Populationswert zu machen.

Danach prüft man mit einem **z-Test**, ob der Unterschied zwischen $Z_r$ und $Z_{ρ_0}$ signifikant ist.

---

### <u>Beispiel:</u>

„Unterscheidet sich die Korrelation zwischen Lernzeit und Prüfungserfolg bei der IPU **signifikant von einem bundesweiten Wert von ρ = 0,5**?“

* Variable 1 (UV/Prädiktor):
  * Lernzeit
* Variable 2 (AV/Kriterium):
  * Prüfungserfolg

---

### <u>Hypothesen:</u>

* $H_{o}: \rho = \rho_{0}$
* $H_{1}: \rho \neq \rho_{0}$ (Ungerichtet)
* $H_{1}: \rho >/< \rho_{0}$ (Gerichtet)
  * Üblicherweise wird gestestet ob sich eine Korrelation signifikant von 0 unterscheidet ($\rho_{0} = 0$)
  * $\rho_{0}$ ist der Populationsmittelwert
  * Wir möchten signifikant werden und die H<sub>0</sub> ablehnen

---

### <u>Entscheidung:</u>

* $z_{emp} \ge z_{krit}$
* $\alpha \ge p$
  * Signifikant und Nullhypothese wird abgelehnt

---

### <u>Voraussetzungen:</u>

* Metrisch skalierte Variablen
  * Beide Variablen (UV&AV) müssen Intervall- oder Verhältnisskaliert sein
* Linearer Zusammenhang
  * Der Zusammenhang zwischen den Variablen sollte linear sein
* Keine Starken Ausreißer
  * Ausreißer können die Korrelation stark verzerren
* Annahme über Populationskorrelation
  * Es muss ein theoretischer/erwarteter Wert für die Korrelation vorliegen
* (n $\ge$ 30)

---

### <u>Vorgehen:</u>

1. Berechnung empirischer Korrelationswerts $r_{emp}$ der Stichprobe
   * PMK muss berechnet werden$$r_{xy} = \dfrac {\frac{1}{n-1} \cdot \sum_{i=1}^{n}(x_i - \bar{x})(y_i - \bar{y})}{\sigma_x \cdot \sigma_y}$$
1. r muss Fischer Z-transformiert werden
   * $Z =\frac{1}{2} \cdot \ln{\left( \dfrac{1 + r}{1 - r}\right) }$
   * $Z$ = transformierter r-Wert der Stichprobe
   * $Z_0$ wird angegeben
     * $Z_0 = \frac{1}{2} \cdot \ln\left(\frac{1+\rho_0}{1-\rho_0}\right)$
1. Z-Wert in die Teststatistik einsetzten
   * $z = \sqrt{n-3} \cdot ( Z -Z_0)$
1. Berechneten z-Wert mit dem kritischen z-Wert vergleichen

---

### Navigation:

* Zurück zu Zusammenhangsanalyse:
  * [Zurück zur Übersicht](/z-Tests-fuer-Korrelation)
* Zurück zu Voraussetzungen:
  * [Voraussetzungen](/stichprobenanzahl-korrelation)

\#Test
