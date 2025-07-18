---
title: Varianzhomogenität bzw. Homoskedastizität
---

Die Annahme der **Varianzhomogenität** (bei Gruppenvergleichen) bzw. **Homoskedastizität** (bei Regressionsmodellen) ist eine wichtige Voraussetzung,  insbesondere bei \*\*t-Tests \*\*, **Varianzanalysen (ANOVA)** und die **lineare Regression**.

Sie bedeutet, dass die **Streuung der Werte bzw. der Residuen in allen Gruppen bzw. über alle Prädiktorwerte hinweg gleich sein sollte**.

Anders als sonst:

* Wir möchten nicht signifikant werden

Eine Verletzung kann zu **verzerrten Standardfehlern und einer Erhöhten Wahrscheinlichkeit für den Fehler erster Art** führen.

---

### <u>Levene Test:</u>

* Prüft ob beide Stichproben aus Grundgesamtheiten mit den gleichen Varianzen stammen (=Varianzhomogenität) oder ob mögliche Unterschiede nur zufällig sind
* Wird wie ein 2-seitiger t-test gerechnet
* Hypothesen
  * H<sub>0</sub>: $\sigma_{1}^2 = \sigma_{2}^2$
  * H<sub>1</sub>: $\sigma_{1}^2 \neq \sigma_{2}^2$
* Entscheidung:
  * t<sub>df</sub> > t<sub>krit</sub> oder $\alpha$ > p
    * Signifikant Nullhypothese wird abgelehnt
  * <u>ACHTUNG:</u> hier wollen wir nicht signifikant werden da die Nullhypothese beibehalten wird sodass die Varianzhomogenität angenommen werden kann
* Formel:
  * t<sub>df</sub>$$t_{df} = \frac{\bar{x}_{1d} - \bar{x}_{2d}}{\sqrt{ \frac{\hat{\sigma}_{1d}^2}{n_1} + \frac{\hat{\sigma}_{2d}^2}{n_2} }}$$
  
  * Mittelwerte $$\bar{x}_{1d} = \frac{\sum_{i=1}^{n} \left| x_{di} - \bar{x}_1 \right|}{n_1}\; \text{;} \qquad \bar{x}_{2d} = \frac{\sum_{i=1}^{n} \left| x_{di} -\bar{x}_2 \right|}{n_2}$$
  
  * Varianzen $$\hat{\sigma}_{1d}^2 = \sqrt{ \frac{ \sum_{i=1}^{n} \left( x_{di,1} - \bar{x}_{1d} \right)^2 }{n - 1} } \; \text{;} \qquad \hat{\sigma}_{2d}^2 = \sqrt{ \frac{ \sum_{i=1}^{n} \left( x_{di,2} - \bar{x}_{2d} \right)^2 }{n - 1} }$$
  
  * d =  Anzahl der Messwerte

---

### <u>Navigation:</u>

* Voraussetzungspfad:
  * [Voraussetzungen](/varianzhomogenitaet-ja-nein)
* T-Tests:
  * [Einstichproben t-Test](/einstichproben-t-test)
  * [t-Test Für Abhängige Stichproben](/t-test-fuer-abhaengige-stichproben)
  * [t-Test für Unabhängige Stichproben](/t-test-fuer-unabhaengige-stichproben)
  * [T-Tests](/t-tests)
* ANOVA:
  * [ANOVA](/anova)
  * [Einfaktorielle ANOVA](/einfaktorielle-anova)
  * [Mehrfaktorielle ANOVA](/mehrfaktorielle-anova)
  * [Messwiederholungs ANOVA](/messwiederholungs-anova)
* Lineare Regression
  * [Lineare Regression](/lineare-regression)
  * [Einfache-lineare Regression](/einfache-lineare-regression)
  * [Multiple Lineare Regression](/Multiple-lineare-regression)
