---
title: Zwei Unabhänggige Stichproben
---

Der z-Test für 2 unabhängige Stichproben prüft, ob sich zwei empirisch beobachtete Korrelationen aus verschiedenen Gruppen signifikant voneinander unterscheiden.

Zuerst wird der empirische Korrelationswert der beiden Stichproben berechnet. Dieser ist allerdings nicht vergleichbar weswegen wir ihn Fisher-Z-Transformieren müssen um diese dann hinterher vergleichen zu können.

Man möchte zeigen, dass sich zwei Korrelationen voneinander unterscheiden

---

##### <u>Beispiel:</u>

„Unterscheidet sich der Zusammenhang zwischen Lernzeit und Prüfungserfolg bei Bachelor- vs. Master studierenden?“

* UV: Lernzeit (Prädiktor)
* AV: Prüfungserfolg (Kriterium)
* Gruppierungsvariable: Bachelor vs. Master

---

##### <u>Hypothesen:</u>

* $H_{o}: \rho_1 = \rho_{1}$
  * Die Korrelationen unterscheiden sich nicht
* $H_{1}: \rho_1 \neq \rho_{2}$ (Ungerichtet) ($\rho \overset{\text{auch manchmal}}= \varrho)$
* $H_{1}: \rho_1 >/< \rho_{2}$ (Gerichtet)
  * Wir möchten Signifikant werden und die Nullhypothese ablehnen um zu zeigen, dass sich die 2 Stichproben Korrelationen signifikant voneinander unterscheiden

---

##### <u>Entscheidung:</u>

* $z_{emp} \ge z_{krit}$
* $\alpha \ge p$
  * Signifikant und Nullhypothese wird abgelehnt

---

##### <u>Voraussetzungen:</u>

* Metrisch skalierte Variablen
  * Beide Variablen (UV&AV) müssen Intervall- oder Verhältnisskaliert sein
* Linearer Zusammenhang
  * Der Zusammenhang zwischen den Variablen sollte linear sein
* Keine Starken Ausreißer
  * Ausreißer können die Korrelation stark verzerren
* Zwei unabhängige Stichproben
* (Für beide Gruppen: n $\ge$ 30)

---

##### <u>Vorgehen:</u>

1. Berechnung empirischer Korrelationswerts $r$ der 2 Stichprobe
   * PMK muss berechnet werden$$r_{xy} = \dfrac {\frac{1}{n-1} \cdot \sum_{i=1}^{n}(x_i - \bar{x})(y_i - \bar{y})}{\sigma_x \cdot \sigma_y}$$
1. Die 2 r´s müssen Fischer Z-transformiert werden
   * $Z =\frac{1}{2} \cdot \ln{\left( \dfrac{1 + r}{1 - r}\right) }$
   * $Z_1 \text{ und } Z_2$ sind die jeweiligen Z werte der Stichproben
1. Z-Werte in die Teststatistik einsetzten
   * $z = \dfrac{Z_1 - Z_2} {\sqrt{\frac{1}{n_1-3} + \frac{1}{n_2 -3}}}$
1. Berechneten z-Wert mit dem kritischen z-Wert vergleichen

---

##### <u>Navigation:</u>

* Zurück zu Zusammenhangsanalyse:
  * [z-Tests für Korrelation](/z-Tests-fuer-Korrelation)
* Zurück zu Voraussetzungen:
  * [Voraussetzungen](/stichprobenanzahl-korrelation)

\#Test
