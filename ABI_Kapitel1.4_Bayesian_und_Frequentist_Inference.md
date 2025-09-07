## Kapitel 1.4 – Bayesian und Frequentist Inference

Statistische Inferenz – also das Schließen von Daten auf zugrunde liegende Strukturen – wird traditionell in zwei große Ansätze unterteilt. Beide haben ihre eigene Philosophie, ihre eigenen Methoden und ihre eigenen Stärken.

---

### Zwei Hauptansätze

1. **Bayesianische Inferenz**  
   - Parameter werden als **Zufallsvariablen** behandelt.  
   - Wahrscheinlichkeiten beschreiben nicht nur Daten, sondern auch die Unsicherheit über Parameter.  
   - Für viele bedeutet das auch, subjektive Einschätzungen oder Expertenwissen als Prior einzubringen.  

2. **Frequentistische Inferenz**  
   - Parameter sind **fixe, unbekannte Größen**.  
   - Wahrscheinlichkeiten beziehen sich ausschließlich auf zufällige Daten in wiederholten Experimenten.  
   - Die zentrale Idee: relative Häufigkeit in der langen Frist.  

Diese Unterscheidung hat über Jahrzehnte zu Kontroversen geführt. Aber in der Praxis muss man keinen Lagerkampf führen – beide Sichtweisen können sich ergänzen.

---

### Ein motivierendes Beispiel: CPCRA AIDS Trial

Ein bekanntes Beispiel für die Unterschiede in der Interpretation ist die **CPCRA AIDS Studie** (Carlin & Hodges, 1999, *Biometrics*).  
- Untersucht wurden zwei Behandlungen gegen *Mycobacterium avium complex*, eine häufige Infektion bei HIV-Patienten im Spätstadium.  
- 69 Patienten in 11 Kliniken nahmen teil.  
- Ergebnisse: 5 Todesfälle in Behandlungsgruppe 1, 13 Todesfälle in Gruppe 2.  

Die primären Endpunktdaten zeigen, wie Ereignisse und Überlebenszeiten über die Gruppen verteilt sind. Eine große Tabelle listet Patientencodes, Gruppe, Überlebenszeit und ob es sich um einen Todesfall oder eine zensierte Beobachtung handelt.  

---

### Unterschiedliche Analysen – unterschiedliche Schlüsse

Die Daten wurden vom **Data Safety and Monitoring Board** mit einem **Cox Proportional Hazards Modell** ausgewertet.  

- **Stratifizierte Analyse:**  
  - Hazard Ratio: 1.9  
  - 95%-Konfidenzintervall: [0.6, 5.9]  
  - p-Wert: 0.24  
  - Interpretation: kein signifikanter Unterschied → Studie hätte fortgeführt werden müssen.  

- **Unstratifizierte Analyse:**  
  - Hazard Ratio: 3.1  
  - 95%-Konfidenzintervall: [1.1, 8.7]  
  - p-Wert: 0.02  
  - Interpretation: klarer Unterschied → Studie wurde abgebrochen.  

Dass zwei gängige Methoden zu so unterschiedlichen Entscheidungen führen, illustriert die praktischen Spannungen zwischen verschiedenen Herangehensweisen.

---

### Warum versagt die stratifizierte Analyse?

Der Beitrag eines Stratum zur **Partial Likelihood** im Cox-Modell ist eingeschränkt:  
- Wenn die längste Überlebenszeit in einem Stratum mit einem Todesfall endet, liefert dieses Stratum **keine Information** für die Schätzung.  
- Genau das trat in dieser Studie auf: vier Strata, deren längstes Überleben ein Todesfall war – alle in Gruppe 2.  
- Ergebnis: die stratifizierte Analyse „versteckt“ den Unterschied zwischen den Gruppen.  

---

### Kompromisslösungen und die Rolle von Bayes

Zwischen den Extremen „stratifiziert“ und „unstratifiziert“ gibt es Ansätze, die beide Sichtweisen verbinden:  
- Verwendung von **Dummy-Variablen** pro Stratum.  
- **Frailty-Modelle**, die unobservierte Heterogenität zwischen Strata berücksichtigen.  
- **Stratum-spezifische Baselines** als Zufallsziehungen aus einer Verteilung von Hazardfunktionen.  

Gerade hier zeigt sich die Stärke des bayesianischen Ansatzes:  
- Er erlaubt, Stratum-baselines **als Zufallsvariablen** zu modellieren.  
- Dadurch wird Flexibilität möglich, die in klassischen frequentistischen Verfahren kaum erreichbar ist.  

Dieses konkrete Beispiel wird später (Kapitel 4) detailliert in einer bayesianischen Analyse aufgegriffen.

---

### Vorteile der bayesianischen Inferenz

Die Fallstudie leitet über zu einer allgemeinen Betrachtung: Warum überhaupt Bayes?  
- **Flexibilität:** Auch hochgradig nichtlineare Modelle mit vielen Parametern sind handhabbar.  
- **Umgang mit Störparametern:** „Nuisance parameters“, die im Frequentismus oft problematisch sind, lassen sich natürlich integrieren.  
- **Gültigkeit bei kleinen Stichproben:** Ergebnisse hängen nicht von Grenzwerttheoremen ab.  
- **Einbindung von Vorwissen:** Expertenurteile oder frühere Studien können über Priors berücksichtigt werden.  
- **Likelihood-Prinzip:** Entscheidungen beruhen ausschließlich auf der Likelihood der beobachteten Daten, nicht auf hypothetischen Wiederholungen.  

Diese Vorteile machen die bayesianische Perspektive besonders attraktiv in komplexen realen Situationen.

---

### Zusammenfassung

Kapitel 1.4 zeigt:  
- Bayesianische und frequentistische Inferenz unterscheiden sich grundlegend in der Sicht auf Parameter und Wahrscheinlichkeit.  
- In realen Studien wie der CPCRA AIDS-Trial können diese Unterschiede zu **gegenteiligen Entscheidungen** führen.  
- Stratifizierte und unstratifizierte Modelle illustrieren die Grenzen des Frequentismus.  
- Bayesianische Methoden bieten Flexibilität, klare Interpretation und die Möglichkeit, Vorwissen einzubeziehen.  

Damit wird verständlich, warum die Bayesianische Inferenz trotz langer Kontroversen heute wieder an Bedeutung gewinnt.  
