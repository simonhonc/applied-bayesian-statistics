## Kapitel 1.2 – Why Bayesian Inference?

### Ausgangsfrage

Die klassische Statistik baut im Wesentlichen auf zwei Säulen:

1. **Konfidenzintervalle**
2. **Hypothesentests**

Diese Verfahren sind mächtig, haben aber entscheidende Schwächen. Bayesianische Inferenz wurde entwickelt, um genau diese Probleme zu überwinden.

---

### Beispiel 1.1 – Newcombs Messung der Lichtgeschwindigkeit

Um die Unterschiede greifbar zu machen, betrachten wir ein historisches Experiment.

Der Astronom **Simon Newcomb** führte 1882 eine Reihe von Messungen zur **Lichtgeschwindigkeit** durch.
Er maß die Zeit, die ein Lichtsignal brauchte, um von seinem Labor am Potomac River zu einem Spiegel am Washington Monument und wieder zurück zu gelangen – eine Strecke von 7400 Metern.

Seine erste Messung ergab:

$$
24.828 \, \text{Millionstel Sekunden}.
$$

Wir nehmen an, dass die Messungen normalverteilt sind:

$$
X_i \sim N(\mu, \sigma^2),
$$

mit bekannter Messvarianz $\sigma^2 = 0.005^2$. Ziel ist es, das wahre $\mu$ zu schätzen.

---

### Konfidenzintervalle im frequentistischen Ansatz

Ein 95%-Konfidenzintervall für $\mu$ ergibt sich aus:

$$
\bar{X} \pm z_{0.975} \cdot \frac{\sigma}{\sqrt{n}},
$$

wobei $\bar{X}$ der Stichprobenmittelwert und $z_{0.975}$ das 97,5%-Quantil der Standardnormalverteilung ist.

Interpretation: In 95 % aller möglichen Zufallsstichproben liegt der wahre Parameter $\mu$ in diesem Intervall.

---

### Simulationsexperiment zur Coverage

Doch was bedeutet „95 %“ wirklich?

Newcomb (bzw. hier im Gedankenexperiment) wiederholt man folgendes:

* Ziehe 1000 Stichproben der Größe $n=10$ aus $N(24.828, 0.005^2)$.
* Berechne für jede Stichprobe ein 95%-Konfidenzintervall.
* Prüfe, ob der wahre Wert $\mu = 24.828$ im Intervall liegt.

Ergebnis:

* In etwa **952 von 1000 Intervallen** liegt der wahre Wert.
* In etwa **48 von 1000 Intervallen** liegt er nicht.

Das illustriert die Definition: Konfidenzintervalle garantieren keine Aussage über eine **konkrete** Stichprobe, sondern nur über das **langfristige Verhalten** der Methode.

---

### Problem der Interpretation

In der Praxis ziehen wir nur **eine** Stichprobe. Dann gilt:

* Entweder enthält das Intervall den wahren Wert – oder eben nicht.
* Wir wissen es nicht.

Wir „trösten“ uns nur damit, dass die Methode langfristig 95 % der Zeit korrekt ist.
Dies führt oft zu Missverständnissen, wenn Anwender glauben, dass „mit 95 % Wahrscheinlichkeit der wahre Wert im Intervall liegt“ – eine Aussage, die frequentistisch nicht korrekt ist.

---

### Bayesianische Credible Intervals

Bayesianische Statistik löst dieses Problem.

Ein **Credible Interval** erlaubt die Aussage:

$$
P(\mu \in [a,b] \mid \text{Daten}) = 0.95.
$$

Das bedeutet: Mit 95 % Wahrscheinlichkeit liegt der Parameter im Intervall – gegeben unsere Daten und unser Modell.

Die Interpretation ist direkter und entspricht der Intuition vieler Anwender. Allerdings braucht man dazu zusätzliche Struktur: einen **Prior** für den Parameter.

---

### Hypothesentests – frequentistisch

Auch bei Hypothesentests treten ähnliche Probleme auf.

Nehmen wir an, wir wollen testen:

$$
H_0: \mu \leq 24.828 \quad \text{gegen} \quad H_1: \mu > 24.828.
$$

Dazu definiert man eine Teststatistik (z. B. einen standardisierten Mittelwert) und berechnet einen **P-Wert**:

$$
p = P(\text{Daten so extrem wie beobachtet} \mid H_0).
$$

* Kleine P-Werte → sprechen gegen $H_0$.
* Große P-Werte → sprechen nicht für $H_0$, sondern nur dafür, dass die Daten mit $H_0$ vereinbar sind.

Missverständnis: Viele interpretieren den P-Wert fälschlich als Wahrscheinlichkeit, dass $H_0$ wahr ist. Das ist **nicht korrekt**.

---

### Problem des P-Wertes

* Der P-Wert ist keine direkte Wahrscheinlichkeit für Hypothesen.
* Er basiert auch auf **nicht beobachteten Datenpunkten** (sampling distribution), was das **Likelihood-Prinzip** verletzt.
* In klinischen Studien mit Zwischenanalysen oder Abbrüchen führt dies zu ernsten praktischen Problemen.

---

### Bayesianische Hypothesentests

Die bayesianische Alternative (nach **Jeffreys, 1961**) ist deutlich einfacher und intuitiver:

* Hypothesen erhalten direkte Wahrscheinlichkeiten.
* Wir berechnen die Posterior-Wahrscheinlichkeit von $H_0$ und $H_1$ gegeben die Daten.
* Ergebnis: Wir wissen, wie wahrscheinlich jede Hypothese ist.

Das ist nicht nur konsistenter, sondern auch für Anwender klarer zu interpretieren.

---

### Zusammenfassung

Kapitel 1.2 zeigt anhand des Beispiels „Newcombs Lichtgeschwindigkeit“ die Kernschwächen der klassischen Statistik:

* Konfidenzintervalle liefern keine Wahrscheinlichkeiten für Parameter.
* P-Werte werden oft missverstanden und verletzen fundamentale Prinzipien.

Die Bayesianische Inferenz bietet Lösungen:

* **Credible Intervals**, die direkt die Wahrscheinlichkeit für Parameter ausdrücken.
* **Bayesianische Hypothesentests**, die Hypothesen selbst Wahrscheinlichkeiten zuweisen.

Damit liefert sie eine klarere und konsistentere Grundlage für Inferenz unter Unsicherheit.

