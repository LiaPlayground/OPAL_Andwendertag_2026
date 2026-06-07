<!--
version:  0.1.0
language: de

narrator: Deutsch Female

tags: Vortrag, OPAL, LiaScript, OER

comment:  OPAL User Day 2026 — LiaScript und seine Integration in OPAL.
          Vortragende: Sebastian Zug (TU Bergakademie Freiberg),
          Martin Lommatzsch (Geschwister-Scholl-Gymnasium Freiberg).

author:   Sebastian Zug, Martin Lommatzsch

import: https://raw.githubusercontent.com/MINT-the-GAP/lia-timer/refs/heads/main/README.md
        https://raw.githubusercontent.com/LiaTemplates/LiveEdit-Embeddings/refs/tags/0.0.1/README.md

persistent: true

edit: true

@style
.cols {
  display: flex;
  flex-wrap: wrap;
  align-items: flex-start;
  gap: 2rem;
}

.cols > * {
  flex: 1;
  min-width: 280px;
}
@end

-->

# LiaScript-Integration in OPAL [Schule]

<h2>Wie Hochschulentwicklungen die Bildungspraxis bereichern</h2>

> **Praxisvortrag**
>
> **Wie Hochschulentwicklungen die Bildungspraxis bereichern**
>
> OPAL User Day, Juni 2026, Dresden

| Vortragende             | Institution                           |
| ----------------------- | ------------------------------------- |
| Prof. Dr. Sebastian Zug | TU Bergakademie Freiberg              |
| Martin Lommatzsch       | Geschwister-Scholl-Gymnasium Freiberg |


# Einleitung & Motivation

1. Warum LiaScript? - Motivation und Philosophie hinter der Beschreibungssprache 
2. Wie sieht der Einsatz in der Schule konkret aus? - Praxisbeispiel mit den Wochenaufgaben
3. Wie kommt ein LiaScript-Kurs in OPAL? - Drei Verbreitungswege, Fokus auf das native Interface

> Sie finden unseren Kurs 
>
> + unter OPAL als Beispiel die Intragration von LiaScriptinhalten in das sächsische LMS [Link](https://bildungsportal.sachsen.de/opal/auth/RepositoryEntry/28960423936/CourseNode/1753151679007485003?18) und 
> + als offene OER auf GitHub [Link](https://github.com/LiaPlayground/OPAL_Andwendertag_2026)

>[!CAUTION]
> Hier sollten wir noch QR Codes auf die beiden Links generieren und einfügen — damit die Leute direkt mit ihrem Handy drauf zugreifen können.

## LiaScript — was ist das?

>[!TIP]
> Was ist eigentlich ein „LiaScript-Kurs“? Und warum sollte das für die Schule/Universität interessant sein?
>
> **LiaScript Dokumente sind Textdokumente, die genutzt werden, um interaktive Inhalte zu erstellen.**


```markdown @embed.style(height: 600px; min-width: 100%; border: 1px black solid)
# Vom Text zur Darstellung

__Formatierter Text__

Eine ~~zentrale Voraussetzung~~ für den Lernerfolg ist **kognitive Aktivierung**.

__Tabellen__

| Studierende | Zufriedenheit | Lernerfolg |
| ------------|:-------------:| ----------:|
| Anna        | 4             | 85%        |
| Ben         | 2             | 40%        | 
| Clara       | 5             | 90%        |
```

## LiaScript interaktiv

>[!TIP]
> Und was ist das besondere daran? Wie unterstützt LiaScript meine Vorlesung / meinen Unterricht?
>
> **LiaScript "kann alles was der Browser kann".**

````markdown @embed.style(height: 600px; min-width: 100%; border: 1px black solid)
<!--
import: https://raw.githubusercontent.com/liaTemplates/ABCjs/main/README.md
-->

# Der Browser als Plattform

__Sprachausgabe__ — einfach per Tag:

> {{|> Deutsch Female}}
> Willkommen zur Einführungsveranstaltung!

__Templates für ... Musik__ 

``` abc
X:353
T: GLUECK AUF DER STEIGER KOEMMT
N: E1512
O: Europa, Mitteleuropa, Deutschland
R: Staende -, Bergmanns - Lied
M: 4/4
L: 1/16
K: G
| G8F4A4 | G8z8 | B8A4c4 | B8z4G2A2 | B4B4B4A2B2 | c4A3AA4
A2B2 | c4c4c4B2c2 | d4B3BB4A4 | G8F8 | G4e4d4c2A2 | B8A8 | G8z8
```
@ABCJS.eval

__Templates für ... Coding__ 

```python        python_example.py
import pandas as pd

daten = pd.DataFrame({
    "Woche":     ["KW 1", "KW 2", "KW 3", "KW 4", "KW 5", "KW 6"],
    "Abgaben":   [   124,    118,    132,    108,     97,     91],
    "Bestanden": [    95,    102,    110,     96,     88,     85]
})
print(daten)
```
@Pyodide.eval

````

## Status & Vision

<div class="cols">
<div>


               {{0-2}}
*****************************************

> **Nette Idee, aber doch auch nur ein Strohfeuer?**

LiaScript wird seit **2017** an der **TU Bergakademie Freiberg** entwickelt — mit der
Vision, eine offene, interaktive Alternative zu klassischen PDFs und PowerPoints
zu schaffen.

- **Textbezogene Inhalte** — Bearbeitung, Versionierung, Kollaboration ohne proprietäre Tools.
- **Zeitgemäße Technologien** — moderne Web-Technologien für Quizze, Code-Ausführung, Animationen, Simulationen.
- **Serverlose Umsetzung** — keine Abhängigkeit von zentralen Systemen aus dem Markdown.
- **Integrationsfähigkeit** — Einbettung in Learning-Management-Systeme als iframe, über den Interpreter oder als SCORM-Pakete.

> An der ersten Anwenderkonferenz nahmen 2022 Lehrpersonen von allen Kontinenten teil - von der Grundschule bis zur Universität. 

*****************************************

</div>

<div>

               {{1-2}}
*****************************************

> **Funktioniert das im Hochschulalltag?**

!?[](https://private-user-images.githubusercontent.com/10922356/293702414-00a24602-dc63-4b9a-894b-80967b914513.mp4?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3ODA4NTIwMDQsIm5iZiI6MTc4MDg1MTcwNCwicGF0aCI6Ii8xMDkyMjM1Ni8yOTM3MDI0MTQtMDBhMjQ2MDItZGM2My00YjlhLTg5NGItODA5NjdiOTE0NTEzLm1wND9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjA2MDclMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwNjA3VDE3MDE0NFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTAzNGQ0ZmQ5MjJhMmNhZGQzYWMyNDM3YWNkYWRhZDhjOWIyMDRjMTBmMjY4YzExZWQ0MGUzYzNiNjYwODdiMzEmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JnJlc3BvbnNlLWNvbnRlbnQtdHlwZT12aWRlbyUyRm1wNCJ9.jmtrMsNrxArVzc6BIgXxU12vRAMy1-jEermKEoLEBgA "Kollaborative Entwicklungsprozesse in den LiaScript-Materialien der Arbeitsgruppe [Link]()")<!--
autoplay="true"
muted="true"
loop="true"
playsinline="true"
-->

*****************************************

</div>
</div>


# LiaScript im Schulalltag

**Teil 2 — ~12 Minuten**


# Einbettung in OPAL

>[!CAUTION]
> LiaScript wird im Browser gerendert und ist damit grundsätzlich ohne Lern-Managementsystem einsetzbar.

In diesem Fall lädt der Interpreter die `.md`-Datei direkt von GitHub oder einem anderen Webserver und rendert sie im Browser.

> ????? Hier kommt der raw-URL rein

>  Warum dann doch ein LMS? Weil Lehrende die Infrastruktur eines LMS gewohnt sind — und weil es Vorteile bringt, den Inhalt direkt im LMS zu haben (z.B. Ergebnisrückmeldung, Kursstruktur, Zugriffskontrolle).

## Einbettung in OPAL

<div class="cols">
<div>


               {{0-2}}
*****************************************

> **Weg 1 — SCORM (generelle Lösung für LMS)**

---------------

Import als Standard-Lernobjekt in OPAL (und jedes andere [SCORM](https://de.wikipedia.org/wiki/SCORM)-fähige LMS).

- **Stärke:** Ergebnisrückmeldung von Teilnehmenden ans LMS.
- **Schwäche:** Bei jeder inhaltlichen Änderung neu exportieren & re-importieren.

!?[Liascript Exporter Video](https://github.com/user-attachments/assets/05ddc764-8522-437a-b569-00b4df7d98b6 "Anwendung des LiaScript [Exporters](https://github.com/LiaScript/LiaScript-Exporter)")

*****************************************

</div>

<div>

               {{1-2}}
*****************************************

> **Weg 2 — Natives Interface in OPAL**

---------------

Nativer Support für LiaScript in OPAL — direkt aus der Kursablage, ohne Export, ohne iFrame.

- **Stärke:** Einfache Integration ohne LiaScript Exporter, ohne iFrame-Bastelei, ohne URL-Konfiguration.
- **Schwäche:** Keine Rückmeldung von Nutzendendaten an das LMS

*****************************************

</div>
</div>


## Live-Workflow: WebDAV, OPAL & LiaScript

- Kursablageordner per **WebDAV** als Netzlaufwerk einbinden.
- `.md`-Datei direkt im gewohnten Editor bearbeiten → speichern → im Kurs neu laden.
- Kein Export, kein Re-Import — **Bearbeiten und Veröffentlichen fallen zusammen.**

> 🖥️ **Demo**
>
> _Sebastian: Testkurs in OPAL öffnen → diese Datei per WebDAV ändern → im Kurs
> nachladen → Änderung ist live._

                          --{{0}}--
Und weil der Inhalt im Kursordner liegt, kann ich ihn per WebDAV wie eine normale
Datei bearbeiten. Ich zeige das jetzt live an genau diesem Vortrag — eine kleine
Änderung, speichern, neu laden, fertig. Bearbeiten und Veröffentlichen sind dasselbe.

## Welcher Weg wann?

| Wenn …                                          | … dann                |
| ----------------------------------------------- | --------------------- |
| maximale Offenheit, OER-Verbreitung             | **Git / Codeberg**    |
| Standard-LMS-Objekt, Ergebnis ans LMS           | **SCORM**             |
| Inhalt in OPAL, schnelle Pflege, native Anzeige | **Natives Interface** |

                          --{{0}}--
Die Faustregel: für offene Verbreitung Git, für ein klassisches LMS-Objekt SCORM,
und wenn der Inhalt bequem in OPAL leben und gepflegt werden soll, das native Interface.

# Vielen Dank!

- **LiaScript:** offene, interaktive OER — nur eine Markdown-Datei.
- **Im Schulalltag:** aus PDFs werden lebendige Aufgaben.
- **In OPAL:** drei Wege — und ein nativer Player als Alleinstellungsmerkmal.

> **Fragen?**
>
> Sebastian Zug · TU Bergakademie Freiberg
>
> Martin Lommatzsch · Geschwister-Scholl-Gymnasium Freiberg

                          --{{0}}--
Vielen Dank für Ihre Aufmerksamkeit! Diese Präsentation lief gerade als LiaScript-Kurs
in OPAL — der beste Beweis, dass es funktioniert. Wir freuen uns auf Ihre Fragen.
