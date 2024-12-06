+++
date = 2024-12-02
draft = true
tags = ['Diagramm', 'LF4']
title = "Anwendungsfalldiagramm / Use Case Diagramm"
+++
## UML – Anwendungsfalldiagramm / Use Case Diagramm

Das Anwendungsfall Diagramm ist auch als Use Case Diagramm bekannt und beschreibt welche Aktionen von Akteuren ausgeführt werden können.

![](Getränkeautomat.webp)

In diesem einfachen Beispiel gibt es nur die nötigen Elemente:

- **Akteur**: ``Kunde`` (Strichmännchen)
- **Use Case**: Aktion, die ausgeführt werden können. Hier im Beispiel: ``kaufe Getränk`` (Ellipse)
- **Assoziation**: Beteiligung zwischen ``Akteur`` und ``Use Case`` (Durchgezogene Linie ohne Pfeile).
- **System**: ``Automat``

Das Ziel ist es darzustellen welcher Akteur welche Aktionen ausführen kann. Die Relevanten Akteure ergeben sich aus der Aufgabenstellung – z.B. wenn in dieser kein Inhaber erwähnt wird, welcher den Automaten auf *kostenlos* stellen kann oder den Servicetechniker bestellen kann werden die auch nicht ins Diagramm aufgenommen.

Das Diagramm beschreibt die Aktionen aus der Sicht des Nutzers, der ein Ziel hat. „Knopf 1 drücken“ wäre eine Aktion, die der Nutzer machen kann – diese soll aber nicht im Use Case Diagramm aufgenommen werden, da der Nutzer das Ziel hat ein Getränkt zu kaufen – nicht Knöpfe zu drücken oder Fehlermeldungen zu lesen. **Es geht nicht um die programmiertechnische Umsetzung**. Auch „Geld einwerfen“ und „Wechselgeld ausgeben“ sollten nicht aufgenommen werden, da diese nicht die Ziele des Nutzers sind.

## weitere Symbole

Im folgenden Beispiel Use Case Diagramm benutze ich alle Relevanten Symbole um diese zu erklären. An einem Beispiel erklärt es sich besser, als die Symbole erst theoretisch durchzugehen.

![](Kaffeeautomat.webp)

- Include-Beziehung:  
  Milchkaffee zu kaufen beinhaltet immer die Ausgabe von Milch.  
  (gestrichelter Pfeil in Richtung des automatisch nächsten Use Case mit der Beschriftung «include»)
- Generalisierung:  
  - Der Mitarbeiter kann wie ein Kunde agieren. Zusätzlich kann er mehr. 
  - Milchkaffee wird wie jeder Kaffee gekauft. Zusätzliche Funktionen spezialisieren es.  
    (Durchgezogener Pfeil mit weißer Pfeilspitze)
- Extend-Beziehung:  
  eine optionale Erweiterung. In der Regel an eine Bedingung geknüpft.  
  (gestrichelter Pfeil in Richtung des erweiterten Use Cases mit der Beschriftung «extend»)  
  Am Use Case kann es Extension Points / Erweiterungspunkte geben.  
  (Horizontale Linie in der Use Case Ellipse mit der Beschriftung ``extension points:`` und der Auflistung der möglichen extends z.B. ``Milch leer``)

### Unterschied zwischen Extension Point und extend mit Bedingung

**Für die Abschlussprüfungen wird es keinen Unterschied machen**, ob man einen Use Case mit Extension Point und «extend» Use Case, oder einen Use Case per «extend» und Bedingung benutzt. Also im Beispiel könnte man nur den Use Case ``Milch ausgeben`` per «extend» ``Fehlermeldung`` erweitern und die Notiz ``Bedingung: Milch leer`` benutzen.

Extension Points können einen spezifischen Status im System darstellen. Der Unterschied wäre also, dass im Beispiel die Fehlermeldung kommt, wenn der Kaffeeautomat versucht Milch auszugeben. Dies ist ein genauer Status. Der Mitarbeiter hingegen kann seine Karte benutzen egal in welchem Menü er sich gerade befindet. Zumindest gibt das Diagramm keinen Aufschluss, zu welchem genauen Zeitpunkt es nur möglich ist.

## Herangehensweise an eine Aufgabenstellung

1. Den Kasten für das System zeichnen und Beschriften. Z.B. ``Kaffeeautomat``. Das ist i.d.R. schon 1 Punkt in der Abschlussarbeit.
2. Außerhalb des Systems die Akteure zeichnen und Beschriften. Z.B. ``Kunde`` und ``Mitarbeiter``.
3. Die direkten Aktionen die eine Person ausführen kann in Ellipsen aufzeichnen und mit den entsprechenden Personen verbinden.  
  Falls ein Akteur alle Aktionen eines anderen Akteurs ausführen kann wird stattdessen ein Pfeil vom „mächtigeren“ Akteur zum eher generischen Akteur gezeichnet (**Generalisierung**).
4. Weitere Aktionen in der Aufgabenstellung suchen. Alles was an **Bedingungen** geknüpft ist **muss** eine **«extend»** Beziehung sein. Schritte die **nacheinander passieren müssen** werden sind **«include»** Beziehungen. „Login“ ist ein häufiger Use Case, der in einer «include» Beziehung verbunden ist.
5. Falls du in deinem gezeichneten Diagram Punkte findest, die mehrmals auftauchen, solltest du überprüfen, ob es sich nicht per «include» mehrmals mit anderen Use Cases verbinden lässt. Ein Use Case sollte nur ein mal auftauchen.

Im Zweifelsfall richtet man sich nach der Aufgabenstellung. Falls diese ausdrücklich sagt, du sollst etwas erweitern, dann zeichnest du das so auf.

## Übungsaufgaben

{{< tabs title="Aufgabe" >}}
{{% tab title="Webshop" %}}
![](Webshop-Aufgabe.jpg)
{{% /tab %}}
{{% tab title="Ferienhäuser" %}}
![](Ferienhäuser-Aufgabe.jpg)
{{% /tab %}}
{{% tab title="Statistik" %}}
![](Statistik-Aufgabe.jpg)
{{% /tab %}}
{{% tab title="Solaranlagenverkauf" %}}
![](Solaranlagenverkauf-Aufgabe.jpg)
{{% /tab %}}
{{< /tabs >}}

## Lösungen

{{% expand title="Lösung Webshop"%}}![](Webshop-Lösung.jpg){{% /expand %}}

{{% expand title="Lösung Ferienhäuser"%}}![](Ferienhäuser-Lösung.jpg){{% /expand %}}

{{% expand title="Lösung Statistik"%}}![](Statistik-Lösung.jpg){{% /expand %}}

{{% expand title="Lösung Solaranlagenverkauf"%}}![](Solaranlagenverkauf-Lösung.jpg){{% /expand %}}
