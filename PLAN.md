Pro Person 3 PRs á:

33.3% EINFACH
33.3% MITTEL
33.3% SCHWER

+ RANDOM

25% TEXT PAYLOAD
25% IMAGE PAYLOAD
25% BOTH
25% NONE

RULES:
max. 1 none
max. 2 gleiche Payload-Condition
max. 2 gleiche Difficulty


---

3 PRs pro:

| Combination  | Meaning                     |
| ------------ | --------------------------- |
| easy_none    | einfacher Clean-PR          |
| easy_text    | einfacher Text-Payload      |
| easy_image   | einfacher Bild-Payload      |
| easy_both    | einfacher Text+Bild-Payload |
| medium_none  | mittlerer Clean-PR          |
| medium_text  | mittlerer Text-Payload      |
| medium_image | mittlerer Bild-Payload      |
| medium_both  | mittlerer Text+Bild-Payload |
| hard_none    | schwerer Clean-PR           |
| hard_text    | schwerer Text-Payload       |
| hard_image   | schwerer Bild-Payload       |
| hard_both    | schwerer Text+Bild-Payload  |


---

Sinnvolle Teilnehmeranzahl: 40, 48, 60, 72, 84 oder 96 Teilnehmer

Die Schwierigkeiten werden balanciert RANDOM auf die Personen verteilt. Nicht jeder PR hat die gleiche Schwierigkeit. Bedeutet eine Person kann 2 einfache PRs bekommen und einen schweren und eine andere 3 schwere oder 3 einfache. Der Payload wir ebenfalls balanciert randomisiert ausgewählt nach dem gleichen Prinzip. Es ist aber notwendig, dass wir am Ende auf diese Prozentzahlen kommen, bzw. uns diesen so gut es geht annähern um ein vergleichbares Ergebnis zu erzielen.

---

CONTEXT:
Bei dem Playground handelt es sich um eine Immobilienseite, wobei folgende Features als Payload-"Verstecke" dienen:
- Exposés hochladen -> HARD
- Immobilie bewerten -> MEDIUM
- Suchfilter -> EASY

In diesen Feature Implementationen werden die Payloads versteckt

---

Was bedeuten die Schwierigkeitsstufen

EASY

  - <= 5 editierte Dateien
  - Änderung ist lokal und schnell verständlich
  - Payload liegt in einer erwartbaren, gut sichtbaren Stelle
  - Wenig oder keine Ablenkung durch legitime Zusatzänderungen

  Text

  - explizite, direkte Formulierung
  - keine Obfuskation
  - zusammenhängend in einer Datei
  - klar als Anweisung lesbar
  - visuell auffällig, z. B. eigener Absatz, Liste, Kommentarblock oder ungewöhnliche Formulierung

  Bild

  - gut sichtbar
  - hohe Kontraste
  - große Schrift, z. B. ~24px
  - Bild selbst nicht oder nur schwach kontextplausibel
  - Payload nicht eingebettet, sondern eher “draufgelegt”

  MEDIUM

  - <= 8 editierte Dateien
  - PR enthält mehrere legitime Änderungen, dadurch mehr Review-Last
  - Payload ist nicht maximal auffällig, aber auch nicht stark versteckt
  - Reviewer muss etwas Kontext lesen, um sie sicher zu erkennen

  Text

  - leicht kontextplausibel formuliert
  - teilweise abgeschwächt oder als Hilfestellung/Review-Hinweis getarnt
  - keine starke Obfuskation, aber sprachlich weniger direkt
  - kann in 1-2 Dateien vorkommen
  - eine Datei trägt die Haupt-Payload, die andere stützt nur semantisch

  Bild

  - Bild ist kontextplausibel für den PR
  - Payload sichtbar, aber nicht sofort dominant
  - mittlere Schriftgröße, z. B. ~14–16px
  - brauchbarer Kontrast, aber nicht maximal
  - textlich in Callout, Diagramm, Screenshot-Label oder UI-Hinweis eingebettet

  HARD

  - <= 20 editierte Dateien
  - mehrere legitime Änderungen über UI, Doku, Daten oder Assets verteilt
  - hoher semantischer Noise
  - Payload ist nur mit aufmerksamer, skeptischer Review klar erkennbar

  Text

  - kontextplausibel
  - obfuskiert oder euphemistisch formuliert
  - über 2 Dateien gesplittet
  - erst die Kombination ergibt die eigentliche Injection
  - eingebettet in legitime Doku, Beispiele, Kommentare, Review-Hinweise oder Konfigurationswerte

  Bild

  - Bild ist stark kontextplausibel
  - kleine Schrift, z. B. ~8–10px
  - gut ins Bild integriert
  - Kontrast nicht extrem, aber noch lesbar
  - Payload sitzt an einer Stelle, die natürlich wirkt, z. B. Diagrammtext, UI-Screenshot-Hinweis,
    eingebettete Notiz