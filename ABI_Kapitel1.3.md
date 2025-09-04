## Kapitel 1.3 – Historical Overview

Die Geschichte der Statistik erinnert an eine kleine Evolutionsgeschichte: aus frühen, oft spekulativen Ideen entwickelte sich eine Praxis, die über Jahrhunderte ihr Gesicht mehrfach veränderte. Der Weg von Bayes über Laplace und Fisher bis in die moderne Statistik zeigt, wie eng methodische Innovationen mit philosophischen Grundhaltungen verbunden sind.

---

### Von Wahrscheinlichkeit zu *inverser Wahrscheinlichkeit*

Die klassische Frage lautet: *Wie wahrscheinlich sind bestimmte Daten, wenn man einen Parameter θ kennt?*  
Die inverse Wahrscheinlichkeit kehrt diese Richtung um: *Wie plausibel ist θ, wenn man bestimmte Daten beobachtet hat?*  

Ein einfaches Beispiel: man beobachtet x Erfolge in n unabhängigen Bernoulli-Versuchen. Klassisch interessiert  

$$
P(X = x \mid \theta).
$$  

Die inverse Sicht fragt stattdessen nach  

$$
P(\theta \mid X = x).
$$  

Damit wird der Parameter selbst Gegenstand einer Wahrscheinlichkeitsaussage – genau das, was später den Kern der bayesianischen Inferenz bildet.

---

### Thomas Bayes (1702–1761)

Thomas Bayes, geboren 1702 in London, war presbyterianischer Geistlicher und Mathematiker. Er war Sohn eines der ersten sechs Nonkonformisten-Prediger Englands, vermutlich Schüler von Abraham de Moivre, und verteidigte Newtons Ideen gegen die Kritik von Bischof Berkeley.  

Bayes interessierte sich intensiv für Mathematik und Wahrscheinlichkeit. Zu Lebzeiten veröffentlichte er nur zwei Arbeiten:  
- *Divine Providence and Government is the Happiness of His Creatures* (1731),  
- *An Introduction to the Doctrine of Fluxions, and a Defense of the Analyst* (1736).  

1742 wurde er zum Fellow der Royal Society gewählt. Sein berühmtestes Werk erschien jedoch erst nach seinem Tod 1761: das *Essay Towards Solving a Problem in the Doctrine of Chances* (1763), eingereicht von Richard Price. Darin wird die zentrale Aufgabe formuliert:

> „Given the number of times in which an unknown event has happened and failed:  
> Required the chance that the probability of its happening in a single trial  
> lies somewhere between any two degrees of probability that can be named.“

Damit wurde erstmals systematisch versucht, von Beobachtungen auf die Wahrscheinlichkeit selbst zu schließen – der erste Schritt zur modernen Bayesianischen Statistik. Bayes’ Grab („Bayes’ vault“) findet man in Bunhill Fields, London.

---

### Laplace und das 19. Jahrhundert

Pierre-Simon Laplace (1749–1827) griff Bayes’ Gedanken auf und entwickelte sie zu einem mächtigen Instrument weiter. Er verfeinerte die inverse probability, würdigte Bayes ausdrücklich (u. a. in seiner Monographie von 1812) und setzte die Methode in Astronomie, Demographie und anderen Wissenschaften ein.  

Auch Kritiker meldeten sich: George Boole stellte 1854 in seinen *Laws of Thought* die inverse probability infrage. Trotzdem blieb sie bis ins frühe 20. Jahrhundert die **dominierende Statistik-Methode**. Sie war Bestandteil universitärer Curricula, schlicht auch deshalb, weil es keine ausgereifte Alternative gab.

---

### Das 20. Jahrhundert: Fisher und die Frequentisten

Im 20. Jahrhundert trat Ronald A. Fisher (1890–1962) auf den Plan. Er war ein lebenslanger Kritiker der inversen Wahrscheinlichkeit und gilt als eine Schlüsselfigur ihres Niedergangs.  

In seinem Aufsatz von 1922 führte Fisher drei grundlegende Konzepte ein:  
1. **Maximum Likelihood** – Schätzung von Parametern über den Wert, der die Daten am plausibelsten macht.  
2. **Suffizienz** – die Idee, dass man Daten durch eine Statistik zusammenfassen kann, ohne Information über θ zu verlieren.  
3. **Effizienz** – Maßstab für die Güte eines Schätzers: optimale Präzision bei minimaler Varianz.  

Diese Konzepte prägten eine ganze Generation von Statistikern. Jerzy Neyman und Egon Pearson entwickelten darauf aufbauend Signifikanztests und Konfidenzintervalle. Damit setzte sich der frequentistische Ansatz durch und wurde im 20. Jahrhundert zum Standard in Wissenschaft und Praxis.

---

### Jeffreys, de Finetti und das Wiederaufleben der Bayes-Idee

Ganz verstummt war die inverse probability aber nie. John Maynard Keynes, Émile Borel und Frank Ramsey sahen Wahrscheinlichkeit als Grad von Überzeugung. Harold Jeffreys griff in den 1930er Jahren die Diskussion auf, verteidigte die inverse probability in einer berühmten Auseinandersetzung mit Fisher und veröffentlichte 1939 *Theory of Probability*. Dieses Werk ist bis heute ein Grundpfeiler der objektiven Bayesianischen Statistik.  

Parallel entwickelte Bruno de Finetti in Italien eine subjektive Fundierung: Für ihn waren Wahrscheinlichkeiten nichts anderes als persönliche Überzeugungen. Er begründete das mit strengen Konsistenzargumenten und führte das Konzept der **Austauschbarkeit (exchangeability)** ein – bis heute eine zentrale Idee für bayesianische Modelle.

Nach dem Zweiten Weltkrieg folgte die „Neo-Bayesian Revival“-Bewegung mit Leonard Savage, I. J. Good und Dennis Lindley. Sie bauten eine moderne bayesianische Schule auf, die sich explizit gegen den dominierenden Frequentismus positionierte.

---

### Moderne: Rechenleistung und MCMC

Den entscheidenden Schub bekam die Bayesianische Statistik durch den technischen Fortschritt. Ab den 1950er Jahren erlaubten Computer erstmals, komplexe Posterior-Verteilungen numerisch zu berechnen. Mit der Entwicklung von **Markov Chain Monte Carlo (MCMC)** in den 1990er Jahren wurde die Bayes-Statistik praktisch breit anwendbar – in Medizin, Ökonomie, Genetik, Klimaforschung und Informatik.  

---

### Synthese von Bayes und No-Bayes

Obwohl die Debatte „Bayes versus Frequentist“ lange polarisiert wurde, gibt es inzwischen Versuche, die Stärken beider Ansätze zu verbinden. Auf unterschiedlichen Skalen und in verschiedenen Problemstellungen lassen sich bayesianische und frequentistische Methoden kombinieren. Ein Beispiel ist Bradley Efrons Aufsatz *Bayesians, frequentists, and scientists* (2005), in dem Möglichkeiten einer solchen Synthese ausgelotet werden.  

Solche Ansätze spielen im Gesamtbild zwar nur eine Nebenrolle, zeigen aber, dass die Lager nicht unvereinbar sind und dass eine praktische Statistik beide Philosophien nutzen kann.

---

### Zusammenfassung

Die Entwicklung der Bayesianischen Statistik verlief in Wellen:  
- Bayes legte den Grundstein, Laplace machte die inverse probability groß.  
- Im 19. Jahrhundert war sie Standard, bis Fisher und die Frequentisten das Paradigma umstellten.  
- Jeffreys und de Finetti hielten die Ideen lebendig und gaben ihnen neue Fundamente.  
- Mit Computer und MCMC wurde die Bayes-Statistik im späten 20. Jahrhundert praktisch unersetzlich.  
- Heute ergänzt ein gelegentliches „sowohl-als-auch“ die Debatte, indem Bayes- und Frequentist-Ideen gezielt verbunden werden.

Dieses Kapitel liefert damit nicht nur eine Chronik, sondern erklärt, **warum** die heutigen Methoden genau so aussehen – und **wo** es sinnvoll ist, bayesianische und frequentistische Ideen **gemeinsam** zu nutzen.
