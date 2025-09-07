## Kapitel 1.1 – Einleitung

Dieses Skript führt in die **Bayesianische Inferenz** ein. Im ersten Kapitel geht es darum, den thematischen Rahmen zu setzen: Welche Themen werden behandelt, wie hängen sie zusammen und welche Methoden stehen im Mittelpunkt?  

Die Übersicht zeigt zwei große Blöcke von Inhalten: **Grundlagen** und **Vertiefungen**.  

---

### Überblick A – Grundlagen der Bayesianischen Inferenz

Die ersten Themen führen schrittweise in die Denkweise und Methoden der Bayesianischen Statistik ein:  

1. **Bayes’ Theorem – diskrete und kontinuierliche Version**  
   Das zentrale Fundament: der Bayes’sche Satz. In der diskreten Form arbeitet man mit Summen, in der kontinuierlichen Version mit Integralen. Dieses Theorem ist das Herzstück der Bayesianischen Statistik.  

2. **Konjugierte Beispiele: Binomial, Exponential**  
   Bei konjugierten Verteilungen ergibt sich der Posterior aus Prior und Likelihood in geschlossener Form. Beispiele wie das Binomialmodell (z. B. Münzwurf) oder das Exponentialmodell (z. B. Wartezeiten) zeigen das Prinzip klar.  

3. **Simulation-basierte Posterior-Berechnung**  
   Viele Posterior-Verteilungen lassen sich nicht analytisch lösen. Monte-Carlo-Methoden ermöglichen es, Posterior-Verteilungen durch Ziehen vieler Stichproben zu approximieren.  

4. **Einführung in WinBUGS**  
   WinBUGS ist eine Software speziell für Bayesianische Statistik. Sie erlaubt es, komplexe Modelle mit minimalem Programmieraufwand zu formulieren und Posterior-Verteilungen über Simulation zu berechnen.  

5. **Regression, ANOVA, GLM, hierarchische Modelle, Survival Analysis, State-Space-Modelle, Copulas**  
   Aufbauend auf den Grundlagen werden klassische statistische Modelle in bayesianischer Form betrachtet: lineare Regression, Varianzanalysen, generalisierte lineare Modelle (z. B. für Binär- oder Zähldaten), hierarchische Strukturen (mehrstufige Modelle), Modelle für Überlebenszeiten, Zustandsraumdarstellungen für Zeitreihen sowie Copula-Modelle, die Abhängigkeiten zwischen Variablen beschreiben.  

6. **Model Checking mit WinBUGS**  
   Modelle müssen überprüft werden. Bayesianische Modellüberprüfung (Posterior-Predictive Checks) bietet dafür Werkzeuge, die direkt Wahrscheinlichkeiten nutzen.  

7. **Konvergenzdiagnostik mit CODA**  
   Simulationen (z. B. MCMC) müssen überprüft werden, um sicherzugehen, dass sie stabil und repräsentativ sind. Mit Paketen wie CODA (in R) lassen sich Konvergenzdiagnosen durchführen.  

---

### Überblick B – Vertiefende Themen

Der zweite Block geht über die Grundlagen hinaus und behandelt anspruchsvollere Methoden und Konzepte:  

1. **Weitere konjugierte Beispiele: Poisson, Normal, Exponential Family**  
   Die Prinzipien konjugierter Priors werden auf weitere Verteilungen ausgeweitet, darunter das Poisson-Modell (z. B. Zähldaten) und die Normalverteilung.  

2. **Spezifikation von Priors**  
   Die Wahl des Priors ist ein zentrales Thema. Hier geht es darum, wie man Vorwissen in geeigneter Form mathematisch ausdrückt.  

3. **Likelihood-Prinzip**  
   Ein philosophischer Kernpunkt der Statistik: Entscheidungen und Inferenz sollen allein auf der Likelihood basieren, nicht auf nicht beobachteten Daten.  

4. **Multivariate und hierarchische Modelle**  
   Modelle für mehrere Variablen und für Daten mit mehrstufigen Strukturen sind ein zentrales Feld der Anwendung.  

5. **Techniken für Posterior-Berechnung**  
   Neben einfachen Simulationen werden weiterführende Methoden vorgestellt, um Posterior-Verteilungen effizient zu approximieren.  

6. **Normalapproximation**  
   Unter bestimmten Bedingungen lassen sich Posterior-Verteilungen durch Normalverteilungen annähern.  

7. **Nicht-iterative Simulation**  
   Methoden, die Posterior-Verteilungen direkt, ohne iterative Verfahren, simulieren.  

8. **Markov Chain Monte Carlo (MCMC)**  
   Ein Herzstück der modernen Bayesianischen Statistik: MCMC-Algorithmen erlauben die Approximation auch in sehr komplexen Modellen.  

9. **Bayes-Faktoren, Modellprüfung und Modellauswahl**  
   Mit Bayes-Faktoren können Hypothesen und Modelle verglichen werden. Bayesianische Modellprüfung ergänzt dies mit Wahrscheinlichkeits-basierten Checks.  

10. **Entscheidungstheorie**  
   Bayesianische Statistik liefert nicht nur Schätzungen, sondern auch Grundlagen für rationale Entscheidungen unter Unsicherheit.  

---

### Hinweise zum Einsatz von Software

- **R** wird in vielen Beispielen verwendet und liefert die Basisumgebung.  
- **WinBUGS** wird vollständig eingesetzt, um Bayesianische Modelle praktisch umzusetzen.  
- Andere Software kann ergänzend genutzt werden – aber auf eigenes Risiko.  

---

### Zusammenfassung  

Kapitel 1.1 gibt einen umfassenden Überblick:  
- **Teil A** stellt die Grundlagen vor – von Bayes’ Theorem über konjugierte Modelle bis hin zu Simulation und klassischen statistischen Methoden in bayesianischer Form.  
- **Teil B** geht in die Tiefe – mit erweiterten Modellklassen, theoretischen Prinzipien, Simulationstechniken wie MCMC, Modellvergleich und Entscheidungstheorie.  
- Ergänzt wird dies durch klare Hinweise zur **Softwareunterstützung**.  

👉 Damit ist klar: Der Leser kann im weiteren Verlauf sowohl die mathematischen Grundlagen verstehen als auch lernen, wie man sie praktisch einsetzt und erweitert.  
