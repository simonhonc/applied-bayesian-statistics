## Kapitel 1.5 – Diskrete Version des Bayes’ Theorem

Der Satz von Bayes lässt sich in einer besonders einfachen Form für **diskrete Ereignisse** formulieren. Er erlaubt es, Hypothesen und Beobachtungen in Beziehung zu setzen: Vorwissen wird durch neue Daten angepasst.

---

### Bayes’ Theorem im Diskreten

Seien $A_1, A_2, \dots, A_n$ eine Menge disjunkter und erschöpfender Ereignisse. Dann gilt für jedes Ereignis $A_j$:

$$
P(A_j \mid B) = \frac{P(A_j)\,P(B \mid A_j)}{\sum_i P(A_i)\,P(B \mid A_i)}.
$$

Das bedeutet: die Wahrscheinlichkeit einer Hypothese nach Beobachtung ($P(A_j \mid B)$) ist proportional zum Produkt aus **Prior** $P(A_j)$ und **Likelihood** $P(B \mid A_j)$. Die Normalisierung erfolgt durch die Summe über alle Hypothesen.

---

### Beispiel 1.3 – Schachturnier

Stell dir vor, du spielst in einem Schachturnier. Dein nächster Gegner ist entweder Jun oder Martha, je nach Ergebnis anderer Spiele.  

- Gegen Jun hast du eine Gewinnchance von ½.  
- Gegen Martha nur ¼.  
- Mit Wahrscheinlichkeit ½ wirst du gegen Jun spielen.  

Frage: *Wie groß ist die Wahrscheinlichkeit, dass du das nächste Spiel gewinnst?*

Man kombiniert hier die verschiedenen Möglichkeiten:  
$$
P(\text{Gewinn}) = P(\text{Jun}) \cdot P(\text{Gewinn|Jun}) + P(\text{Martha}) \cdot P(\text{Gewinn|Martha}).
$$

Das ergibt:
$$
P(\text{Gewinn}) = \tfrac{1}{2}\cdot\tfrac{1}{2} + \tfrac{1}{2}\cdot\tfrac{1}{4} = \tfrac{3}{8}.
$$

Nun kommt die zweite Frage: *Angenommen, du hast tatsächlich gewonnen – wie wahrscheinlich ist es, dass dein Gegner Jun war?*  
Hier dreht sich die Richtung um: man möchte von der Beobachtung auf die zugrunde liegende Hypothese schließen. Genau das leistet der Satz von Bayes.

---

### Beispiel 1.4 – Diagnostisches Testen

Ein neues HIV-Heimtest-Kit wird vorgestellt:  
- **Sensitivität**: 95 % (der Test erkennt 95 % der tatsächlich Infizierten).  
- **Spezifität**: 98 % (der Test ist bei 98 % der Gesunden negativ).  
- **Prävalenz**: 1 von 1000 Personen ist infiziert.  

Frage: *Wenn der Test bei einer Person positiv ausfällt – wie wahrscheinlich ist es, dass die Person tatsächlich HIV-positiv ist?*

Sei  
- $A =$ „Person ist HIV-positiv“,  
- $\bar{A} =$ „Person ist HIV-negativ“,  
- $B =$ „Test ist positiv“.  

Mit Bayes ergibt sich:
$$
P(A \mid B) = \frac{P(A)\,P(B \mid A)}{P(A)\,P(B \mid A) + P(\bar{A})\,P(B \mid \bar{A})}.
$$

Da die Prävalenz extrem gering ist, überwiegen die falsch-positiven Ergebnisse, trotz hoher Sensitivität und Spezifität. Nur ein kleiner Teil der positiven Tests sind tatsächlich Infizierte.  

Dieses Resultat überrascht viele. 1991 nutzte die Kolumnistin Marilyn vos Savant genau dieses Beispiel. Sie gab die richtige Antwort – doch viele Mathematiker widersprachen ihr zunächst fälschlicherweise. Das illustriert, wie kontraintuitiv Bayes’sche Schlüsse oft sind.

---

### Beispiel 1.5 – Das Monty-Hall-Problem

Ein weiteres berühmtes Rätsel: In der Show *Let’s Make a Deal* gibt es drei Türen – hinter zweien Ziegen, hinter einer ein Auto.  

- Du wählst eine Tür (z. B. Tür 2).  
- Der Moderator Monty Hall öffnet eine andere Tür mit einer Ziege (z. B. Tür 1).  
- Nun darfst du wechseln oder bei deiner ursprünglichen Wahl bleiben.  

Frage: *Was soll man tun?*

Intuitiv glauben viele, die Chancen stünden 50:50. Mit Bayes sieht man: Wenn man **wechselt**, beträgt die Gewinnwahrscheinlichkeit 2/3; wenn man bleibt, nur 1/3. Auch dies ist ein Beispiel, wie Bayes die richtige Intuition liefert.

---

### Allgemeine Formulierung

All diese Beispiele lassen sich unter einem Dach darstellen:  

Seien $H_1, H_2, \dots, H_n$ Hypothesen und $D$ beobachtete Daten. Dann gilt:

$$
P(H_i \mid D) = \frac{P(H_i)\,P(D \mid H_i)}{\sum_j P(H_j)\,P(D \mid H_j)}.
$$

- $P(D \mid H_i)$: **Likelihood** – wie gut erklärt die Hypothese die Daten?  
- $P(H_i)$: **Prior** – wie plausibel ist die Hypothese im Vorfeld?  
- $P(H_i \mid D)$: **Posterior** – aktualisierte Wahrscheinlichkeit nach Einbezug der Daten.  

---

### Beispiel 1.6 – Die Bedeutung plausibler Priors

Man stelle sich vor: Beim Blick aus dem Fenster sieht man etwas Großes, Verzweigtes, mit grünen Blättern. Warum denkt man sofort: „Das ist ein Baum“?

- Hypothese $H_1$: es ist ein Baum.  
- Hypothese $H_2$: es ist ein Mensch.  
- Hypothese $H_3$: es ist etwas anderes, z. B. eine Pappattrappe.  

Die Likelihoods sind ähnlich:  
- $P(D|H_1)$ nahe 1,  
- $P(D|H_2)$ nahe 0,  
- $P(D|H_3)$ ebenfalls nahe 1.  

Doch entscheidend sind die **Priors**:  
- $P(H_1)$ hoch (Bäume sind häufig).  
- $P(H_2)$ hoch (Menschen auch).  
- $P(H_3)$ sehr niedrig (Pappbäume im Garten sind extrem selten).  

Bayes kombiniert beides: die Information aus den Daten (Likelihoods) und das Vorwissen (Priors). Nur so entsteht ein plausibles Gesamtbild. Die Posterior-Wahrscheinlichkeiten sind proportional zu Prior × Likelihood – eine präzise mathematische Form dessen, was Menschen intuitiv beim Erkennen tun.

---

### Zusammenfassung

Kapitel 1.5 zeigt die **diskrete Form des Satzes von Bayes** in Theorie und Praxis:  

- **Formel:** Posterior = Prior × Likelihood / Normalisierung.  
- **Beispiele:**  
  - Schachspiel: von Sieg auf Gegner schließen.  
  - Diagnostische Tests: geringe Prävalenz kann scheinbar sichere Tests entwerten.  
  - Monty Hall: Intuition kann trügen, Bayes liefert die richtige Strategie.  
  - Baum-Beispiel: Plausibilität (Prior) ist ebenso wichtig wie die Beobachtung selbst.  

Der Satz von Bayes erklärt damit, wie man aus Vorwissen und Beobachtungen zu einem kohärenten, quantitativen Urteil gelangt.
