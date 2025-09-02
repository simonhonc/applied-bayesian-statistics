# Kapitel 1.1 – Introduction

## Motivation
Statistische Inferenz beschäftigt sich mit der Frage, wie man aus Daten Rückschlüsse auf zugrunde liegende Strukturen ziehen kann.
Die bayesianische Sichtweise unterscheidet sich von der frequentistischen dadurch, dass Unsicherheit explizit mit Wahrscheinlichkeiten modelliert wird.

- **Frequentistisch:** Parameter sind feste, aber unbekannte Größen. Zufall steckt nur in den Daten.
- **Bayesianisch:** Parameter selbst werden als Zufallsvariablen betrachtet. Man bringt Vorwissen durch eine Priorverteilung ein und aktualisiert dieses mit Hilfe der Daten.

## Kernelemente der Bayesianischen Inferenz
1. **Prior-Verteilung**: beschreibt Vorwissen oder Annahmen über den Parameter vor der Beobachtung von Daten.
2. **Likelihood**: beschreibt, wie wahrscheinlich die Daten für verschiedene Werte des Parameters sind.
3. **Posterior-Verteilung**: Kombination von Prior und Likelihood; sie repräsentiert unser aktualisiertes Wissen nach den Daten.

Formal gilt:
$$
\pi(	heta \mid x) \propto \pi(	heta) \cdot f(x \mid 	heta)
$$

## Ziel
Ziel der Bayesianischen Inferenz ist es, die Posterior-Verteilung zu bestimmen und daraus Aussagen über den Parameter oder zukünftige Beobachtungen abzuleiten.

---

**Beispielhafte Fragen:**
- Wie hoch ist die Wahrscheinlichkeit, dass ein Medikament wirkt, gegeben die bisherigen Studien?
- Welche Werte sind für eine unbekannte Münzwahrscheinlichkeit $p$ nach 10 Würfen mit 7-mal Kopf plausibel?

---

## Zusammenfassung
Kapitel 1.1 führt die Grundidee ein: Statt Parameter als fixe, unbekannte Größen zu behandeln, modelliert man sie als Zufallsvariablen und macht Unsicherheit explizit sichtbar. Das zentrale Werkzeug ist der Bayes’sche Satz, der Vorwissen und Daten verknüpft.
