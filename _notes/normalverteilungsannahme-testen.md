---
title: Normalverteilungsannahme testen
---


In vielen statistischen Verfahren ist die Annahme der **Normalverteilung** zentral, um gültige Signifikanztests (z. B. t- oder F-Tests) durchzuführen.
Dabei hängt es vom Verfahren ab, **welche Variable normalverteilt sein muss**:

* Beim **t-Test** (einfach, abhängig, unabhängig) wird die Normalverteilung der **Merkmalsverteilung** in der Population bzw. der **Gruppen** oder **Differenzwerte** angenommen.
* Bei der **linearen Regression** (einfach & multipel) müssen die **Residuen** des Modells normalverteilt sein – **nicht** die AV oder Prädiktoren.
* Bei **ANOVA**-Verfahren gilt dasselbe wie beim t-Test: Die **AV** sollte in jeder Gruppe normalverteilt sein.

Die Tests und Visualisierungen (Q-Q-Plot, Histogramm, Shapiro-Wilk etc.) bleiben gleich – nur der **Bezugspunkt** unterscheidet sich je nach Test.

---

### <u>Varianten:</u>

1. Grafische Analyse: Q-Q Plot
   
   * Vergleicht empirische Daten mit einer Theoretischen Verteilung
   * Normalverteilt:
     * Punkte liegen auf einer Linie
     * Leichte Schwankungen meist trzdm zu erkennen
       ![363x169](qqnvt.png)
   * Schiefe Verteilung:
     * Viele Werte sind kleiner/größer als erwartet			![362x155](qqschief.png)
   * Leptokurtisch
     * Starke Kniche an beiden Enden
     * Datenverteilung sehr gehäuft in der Mitte
       ![361x183](qqlepto.png)
1. Für n\<50: Shapiro-Wilk-Test
   
   * Hypothesentest:
     * **H₀**: Empirische Verteilung entspricht der theoretischen Verteilung (Normalverteilung)
     * **H₁**: Es gibt einen Unterschied
   * Entscheidung:
     * W<sub>emp</sub> \< W<sub>krit</sub> oder p \< $\alpha$
       * Signifikant und Nullhypothese wird abgelehnt
     * <u>ACHTUNG:</u> hier wollen wir nicht signifikant werden da die Nullhypothese beibehalten wird sodass die Normalverteilung angenommen werden kann
   * Prüfgrößen W<sub>krit</sub>:
     * W<sub>krit</sub> liegt tabelliert vor
     * W= $\frac{\text{Varianz der erwarteten Quantile}}{\text{Varianz der Stichprobe}}$
     * Wertebereich: 0-1
       * =1 wenn Varianz der Stichprobe der Varianz der Normalverteilung entspricht
1. Für n>50: Kolmogorov-Smirnov-Test
   
   * "KSx2-anpassungstest"
   * Geringere Teststärke als SW-Test
   * Nicht Robust wenn Populationsmittelwert $\mu$ und Standartabweichung $\text{SD}$ nicht bekannt sind
   * behält H<sub>0</sub> länger bei
   * Testet ob x-Werte der empirischen Verteilung $\phi$(x) , x-Werten einer theoretischen Normalverteilung $\phi$<sub>0</sub>(x) entsprechen
   * Hypothesen:
     * **H₀**: $\phi$(x) = $\phi$<sub>0</sub>(x)  (NVT)
     * H<sub>1</sub>: $\phi$(x) $\neq$ $\phi$<sub>0</sub>(x)  (keine NVT)
   * Entscheidung:
     * D<sub>max</sub> > D<sub>krit</sub> oder p \< $\alpha$
       * Signifikant und Nullhypothese wird abgelehnt
     * <u>ACHTUNG:</u> hier wollen wir nicht signifikant werden da die Nullhypothese beibehalten wird sodass die Normalverteilung angenommen werden kann
       * Und D wert soll kleiner sein als kritischer Wert
   * Prüfgröße D<sub>max</sub>:
     * x-Wert bei dem die Differenz zwischen empirischen und theoretischer Verteilung maximal ist

### <u>Navigation:</u>

* Voraussetzungspfad:
  
  * [Voraussetzungen](/normalverteilung-und-av-pruefen)
* T-Test:
  
  * [T-Tests](/t-tests)
  * [Einstichproben t-Test](/einstichproben-t-test)
  * [t-Test für Unabhängige Stichproben](/t-test-fuer-unabhaengige-stichproben)
  * [t-Test Für Abhängige Stichproben](/t-test-fuer-abhaengige-stichproben)
  * [Welsh-Test](/welsh-test)
* Lineare Regression:
  
  * [Lineare Regression](/lineare-regression)
  * [Einfache-lineare Regression](/einfache-lineare-regression)
  * [Multiple Lineare Regression](/Multiple-lineare-regression)
* ANOVA
  
  * [ANOVA](/anova)
  * [Einfaktorielle ANOVA](/einfaktorielle-anova)
  * [Mehrfaktorielle ANOVA](/mehrfaktorielle-anova)
