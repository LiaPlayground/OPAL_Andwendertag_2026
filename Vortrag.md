<!--
version:  0.1.1
language: de

narrator: Deutsch Female

tags: Vortrag, OPAL, LiaScript, OER

comment:  OPAL User Day 2026 — LiaScript und seine Integration in OPAL.
          Vortragende: Sebastian Zug (TU Bergakademie Freiberg),
          Martin Lommatzsch (Geschwister-Scholl-Gymnasium Freiberg).

author:   Sebastian Zug, Martin Lommatzsch

import: https://raw.githubusercontent.com/LiaTemplates/LiveEdit-Embeddings/refs/tags/0.0.1/README.md


import: https://cdn.jsdelivr.net/gh/LiaTemplates/algebrite@master/README.md
import: https://cdn.jsdelivr.net/gh/LiaTemplates/JSXGraph@main/README.md


import: https://raw.githubusercontent.com/MINT-the-GAP/lia-annotation/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-board-mode/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-marker/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-DynFlex/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-orthography/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/NavigationREADME.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-timer/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/lia-Mathe/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/RedirecterREADME.md


import: https://raw.githubusercontent.com/MINT-the-GAP/lia-canvas-ocr/refs/heads/main/README.md
import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/KoordREADME.md


import: https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/main/imports/FreezeREADME.md

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


---

---


<section class="dynFlex" data-basis="32.5">

<div class="flex-child">

![logo](https://raw.githubusercontent.com/MINT-the-GAP/Wochenaufgabe/refs/heads/main/Zeug/Logo.png)

</div>
<div class="flex-child">

<center>

<h3> Prof. Dr. Sebastian Zug</h3> 
<small><small><small> Technische Universität Bergakademie Freiberg, Institut für Informatik </small></small></small>

<h3> und </h3> 

<h3> Martin Lommatzsch</h3>
<small><small><small> Geschwister-Scholl-Gymnasium Freiberg </small></small></small>

</center>

</div>
<div class="flex-child">


![partner_map](https://github.com/LiaPlayground/Saechsischer_Schulinformatik_Tag_2026/blob/main/pic/LiaScript_Meets_OER.png?raw=true "OER-Logo - Quelle: Jonathasmello - Eigenes Werk, CC BY 3.0, [https://commons.wikimedia.org/w/index.php?curid=18460156](https://commons.wikimedia.org/w/index.php?curid=18460156) erweitert um LiaScript Logo")
</div>

</section>

<center>

---

---

<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/0.png" width="60" height="60">  $\;\qquad\;$
<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="60" height="60">  $\;\qquad\;$
<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/2.png" width="60" height="60">  $\;\qquad\;$
<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/3.png" width="60" height="60">  $\;\qquad\;$
<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/4.png" width="60" height="60">  $\;\qquad\;$
<img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/5.png" width="60" height="60"> 

</center>



---

---




# Einleitung & Motivation

1. Warum LiaScript? - Motivation und Philosophie hinter der Beschreibungssprache 
2. Wie sieht der Einsatz in der Schule konkret aus? - Praxisbeispiel mit den Wochenaufgaben
3. Wie kommt ein LiaScript-Kurs in OPAL? - Drei Verbreitungswege, Fokus auf das native Interface

> Sie finden unseren Kurs 
>
> + unter OPAL als Beispiel die Intragration von LiaScriptinhalten [Link](https://bildungsportal.sachsen.de/opal/auth/RepositoryEntry/28960423936/CourseNode/1753151679007485003?18) und 
> + als offene OER auf GitHub [Link](https://github.com/LiaPlayground/OPAL_Andwendertag_2026)

| OPAL               | OER auf GitHub                        |
| :---------------------------------: | :-----------------------------------: |
| ![QR-Code OPAL-Kurs](qr_opal.png)   | ![QR-Code GitHub-Repository](qr_github.png) |
| 

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
        https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
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

!?[](https://raw.githubusercontent.com/LiaPlayground/OPAL_Andwendertag_2026/main/collaboration_github.mp4 "Kollaborative Entwicklungsprozesse in den LiaScript-Materialien der Arbeitsgruppe [Link]()")<!--
autoplay="true"
muted="true"
loop="true"
playsinline="true"
-->

*****************************************

</div>
</div>


# <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="60" height="60"> LiaScript im Schulalltag




<section class="dynFlex" data-basis="49">


<div class="flex-child">



{{1}}
<h2> Beobachtungen als Lehrkraft </h2> 

{{2}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/0.png" width="40" height="40">  Vergessene Fachvokabeln </h3> 


{{3}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/0.png" width="40" height="40"> Vergessene Lösungsansätze und -strategien </h3> 


{{4}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/0.png" width="40" height="40">  eingerostete Algorithmen </h3> 


</div>



<div class="flex-child">


{{6}}
![Wochenaufgaben](https://raw.githubusercontent.com/MINT-the-GAP/Wochenaufgabe/refs/heads/main/Zeug/screenshotWA.PNG)


</div>

</section>






<section class="dynFlex" data-basis="49">



<div class="flex-child">



{{5}}
<h2> Lösungsansatz </h2> 

{{5}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="40" height="40">  Bereitstellung von Wiederholungsoptionen $\;\Rightarrow\;$ Idee der Wochenaufgaben </h3> 


</div>



<div class="flex-child">


{{6}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/2.png" width="40" height="40">  wochenaufgaben.gsg-freiberg.de </h3> 


{{7}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/2.png" width="40" height="40">  Über 6800 Seiten an Aufgaben mit Musterlösungen </h3> 


{{7}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/3.png" width="40" height="40">  Repetitorium mit mehr als 1500 Seiten Erklärungen, Aufgaben und Lösungen </h3> 


</div>

</section>




## <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/2.png" width="60" height="60"> Problemanalyse




<section class="dynFlex" data-basis="49">


<div class="flex-child">



{{1}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/0.png" width="40" height="40">  PDFs bieten keine Interaktionsmöglichkeit </h3> 


{{2}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/0.png" width="40" height="40"> keine Rückmeldung für die Lernenden </h3> 

{{3}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/0.png" width="40" height="40"> keine Rückmeldung für die Lehrkräfte </h3> 


{{4}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/0.png" width="40" height="40"> Entlastet im Unterricht nicht, da "Ist das richtig?"-Meldungen bleiben </h3> 


</div>


<div class="flex-child">


{{5}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/4.png" width="40" height="40"> Es braucht interaktive digitale Aufgaben </h3> 


</div>

</section>



## <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/3.png" width="60" height="60"> Angebotsanalyse



{{1}}
<h2> Bekannte Anbieterprobleme </h2> 


<section class="dynFlex" data-basis="49">


<div class="flex-child">

{{1}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/5.png" width="40" height="40">  Proprietäre Anbieter </h3> 

{{3}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/5.png" width="40" height="40">  Es wird fast nur Anforderungsbereich 1 angeboten ("Gib an") </h3> 

{{5}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/5.png" width="40" height="40">  Beschränkung auf das Angebot durch Vorgaben des Unternehmens </h3> 

{{7}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/5.png" width="40" height="40">  Repetitiver Inhalt </h3> 

{{9}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/5.png" width="40" height="40">  Antworten müssen teilweise in einem speziellen Syntax eingegeben werden </h3> 


{{11}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/5.png" width="40" height="40">  Flipped-Classroom-Prinzip </h3> 



</div>


<div class="flex-child">

{{2}}
<h3> $\Rightarrow\;$ <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/0.png" width="40" height="40"> Bildung sollte kostenlos sein </h3> 

{{4}}
<h3> $\Rightarrow\;$ <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/0.png" width="40" height="40"> Rechenwege, Erklärungen, Zeichnungen, Vernetzungen usw. und nicht nur üben </h3> 

{{6}}
<h3> $\Rightarrow\;$ <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/0.png" width="40" height="40"> Unterricht muss auf Lerngruppen abgestimmt sein </h3> 

{{8}}
<h3> $\Rightarrow\;$ <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/0.png" width="40" height="40"> Auswendige gelernte Eingaben statt kognitiver Aktivierung </h3> 

{{10}}
<h3> $\Rightarrow\;$ <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/0.png" width="40" height="40"> Es sollte das Fach und nicht das Programm unterrichtet werden </h3> 

{{12}}
<h3> $\Rightarrow\;$ <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/0.png" width="40" height="40"> Keine Entlastung im Unterricht und Verstärkung der Herkunftsungleichheit </h3> 


</div>

</section>







## <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/4.png" width="60" height="60"> Bedarfe in der Schule {1}{und Lösungen} 


<section class="dynFlex" data-basis="49">


<div class="flex-child">

{{2}}
> <h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="40" height="40">  Bring-Your-Own-Device-Tauglichkeit </h3> 


{{3}}
<h3>LiaScript ist Open Education Resource und somit kostenlos </h3> 

{{4}}
<h3>LiaScript braucht keine Installation </h3> 

{{5}}
<h3>LiaScript ist DSGVO-konform </h3> 


</div>



<div class="flex-child">


{{6}}
> <h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="40" height="40">  Dezentrale Klassengruppen </h3> 


{{7}}
<h3>LiaScript wird dezentral im eigenen Browser realisiert </h3> 

{{8}}
<h3>Wurde ein Kurs einmal geladen, ist alles offline abrufbar </h3> 


</div>

</section>









## <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/4.png" width="60" height="60"> Bedarfe in der Schule  {0}{und Lösungen} 



<section class="dynFlex" data-basis="49">


<div class="flex-child">

{{1}}
> <h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="40" height="40"> Mathematische Schrifterkennung </h3> 

{{2}}
<h3>LiaScript erkennt über den Browser mathematische Verschriftlichung </h3> 

{{3}}
<h3>$\Rightarrow\;\;$ Es muss kein Eingabesyntax erlernt werden </h3> 

{{4}}
---

{{4}}
Bespiel: **Gib** den Bruch $\dfrac{23}{35}$ **an**.
[[  23/35  ]] @canvas
@Algebrite.check(23/35)


</div>


<div class="flex-child">

{{5}}
> <h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="40" height="40"> Eingebettes Computer-Algebra-System </h3> 

{{6}}
<h3>LiaScript verfügt über ein CAS </h3> 

{{7}}
---


{{7}}
Bespiel 2: **Gib** den Term $x^2-2x+1$ in einer beliebigen Umformung in das Lösungsfeld **ein**.
[[  x ^ 2 - 2 * x + 1  ]]
@Algebrite.check(x^2-2*x+1)


</div>

</section>










## <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/4.png" width="60" height="60"> Bedarfe in der Schule  {0}{und Lösungen} 



<section class="dynFlex" data-basis="49">


<div class="flex-child">

{{1}}
> <h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="40" height="40"> Intuitiver Umgang ohne Syntax-Schulungen </h3> 

</div>

<div class="flex-child">


{{2}}
> <h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="40" height="40"> Bildschirm als echter Ersatz für das Papier </h3> 

</div>

</section>



<section class="dynFlex" data-basis="49">


<div class="flex-child">

{{3}}
**************************
@Koordinatensystem(`xmin=-7;xmax=7;ymin=-5;ymax=5;width=800;id=A9`)

@AchsenBeschriftung(`id=A9;xlabel=$x$;ylabel=$y$`)

@Regression(`A9`)
**************************


</div>

<div class="flex-child">


{{4}}
**************************
__$a)\;\;$__ **Gib** den Funktionsterm **an**, um den Graphen darstellen zu lassen.

@PlotEingabeLatex(`A9;g;#b41f65`)
**************************




{{5}}
---


{{5}}
---

{{5}}
__$b)\;\;$__ **Zeichne** drei beliebige Punkte in das Koordinatensystem **ein** und **führe** die Regression **durch**.




</div>

</section>







## <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/4.png" width="60" height="60"> Bedarfe in der Schule  {0}{und Lösungen} 



<section class="dynFlex" data-basis="49">


<div class="flex-child">

{{1}}
> <h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="40" height="40"> Rückmeldung für den Lernenden um den individuellen Lernpfad anzupassen </h3> 

{{2}}
??[Freeze](https://liascript.github.io/nightly/?https://raw.githubusercontent.com/MINT-the-GAP/Wochenaufgabe/refs/heads/main/Zeug/VortragBPSA.md)

</div>

<div class="flex-child">



{{3}}
> <h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="40" height="40"> Statistische Analyse der Lerngruppe für die Lehrkraft um den Unterricht anzupassen </h3>



{{4}}
<!-- style="max-width:750px" -->
![Frozen](https://raw.githubusercontent.com/MINT-the-GAP/Wochenaufgabe/refs/heads/main/Zeug/frozen.png)



</div>

</section>






## <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/4.png" width="60" height="60"> Bedarfe in der Schule  {0}{und Lösungen} 


{{1}}
> <h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/1.png" width="40" height="40"> Hochwertige individualisierbare Aufgabengenerierung </h3> 


{{2}}
<h3> <img src="https://raw.githubusercontent.com/MINT-the-GAP/Aufgabensammlung/refs/heads/main/pics/grad/2.png" width="40" height="40"> Aufgabensammlung ist in der Entstehung: <a href="https://mint-the-gap.github.io/Aufgabensammlung/"> mint-the-gap.github.io/Aufgabensammlung/ </a> </h3> 


{{2}}
!?[Sammlung](https://wochenaufgaben.gsg-freiberg.de/Lia/test2.mp4)











# Einbettung in OPAL

>[!CAUTION]
> LiaScript wird im Browser gerendert und ist damit grundsätzlich ohne Lern-Managementsystem einsetzbar.

In diesem Fall lädt der Interpreter die `.md`-Datei direkt von GitHub oder einem anderen Webserver und rendert sie im Browser.

> [Quellcode dieses Vortrages](https://raw.githubusercontent.com/LiaPlayground/OPAL_Andwendertag_2026/refs/heads/main/Vortrag.md)

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
