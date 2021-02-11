# Begriffsdefinitionen

## Allgemein

**Tenant:** Die oberste Ordnungsinstanz, welche mehrere Nutzer\*innen zusammenfasst und somit als digitale Repräsentation von einer Organisation, einem Team, etiner Abteilung, etc. dient.

**Stelle:** Eine Offene Position in Ihrere Organisation.

**Anforderungsprofil:** Ein Satz an Kriterien (=Anforderungskriterien) einer Stelle auf welche ein\*eine Kanditat\*in untersucht werden soll.

## Formulare

Ein Formular ist eindeutig einer _Stelle_ zugeordnet und ist aus einer der folgenden drei Kategorien:\
**Formularkategorie:** _Bewerbung_, _Screening_, _Assessment_

**Bewerbungsformular:** Ein Formular über welches sich Bewerber\*innen für eine Stelle bewerben. Eine _Stelle_ hat genau ein _Bewerbungsformular_.\
**Screeningformular:** Ein Formular über welches Bewertungen zu Bewerbungsunterlagen abgegeben werden. Eine _Stelle_ hat genau ein _Screeningformular_.\
**Assessmentformular:** Ein Formular über welches Bewertungen zu Übungungen eines Assessment Centers abgegeben werden. Eine _Stelle_ hat ein oder mehere _Assessmentformulare_.

**Formularfeld:** Ein einzelnes Feld eines Formulars. **Achtung:** Nicht nur Eingabefelder sondern auch statische Felder wie zum Beispiel ein _Section Header_ werden als _Formularfeld_ bezeichnet.

**Formularfeld-Absicht:** Eine aus drei Möglichkeiten der Auswertung: _count distinct_, _aggregate_, _sum up_\
**count distinct:** In der Auswertung wird gezählt wie oft jeder mögliche Wert vorkommt. (z.B. Ich will diesen\*diese Bewerber\*in besprechen)\
**aggregate:** In der Auswertung werden die Werte aller Formulareintragsfelder, welche dieses Formularfeld referenzieren aneinander gereiht. (z.B. Anmerkungen)\
**sum up:** In der Auswertung werden die Werte alle Formulareintragsfelder, welche dieses Formularfeld referenzieren summiert und/oder deren Durchschnitt berechnet.

## Formulareintrag

**Formulareintrag:** Füllen Sie ein Formular aus und senden es ab, so wird die Zusammenfassung aller Eingabewerte als _Formulareintrag_ bezeichnet.\
**Formulareintragsfeld:** Ein einzelnes Feld aus einem _Formulareintrag_. Ein _Formulareintragsfeld_ ist eindeutig einem _Formularfeld_ zugeordnet.

## Auswertung

Der Zentrale Begriff der Auswertung ist der _Score_. Er tritt auf verschiedenen Ebenen auf und spiegelt entweder eine Summe oder einen Durchschnitt wieder. Um zu erkennen auf was er sich bezieht wird er mit einem entsprechenden Präfix versehen:

### Ranking

**Formulareintrag-Score:** Man betrachte die Felder (=_Formulareintragsfelder_) von einem Formulareintrag und zwar nur die, deren referenziertes _Formularfeld_ die _Formularfeld-Absicht_ "_sum up_" trägt. Berechnet man die Summe der Werten dieser _Formulareintragsfelder_ ensteht der _Formulareintrag-Score_.

**Formular-Score:** Man betrachte alle _Formulareintrag-Score_, welche sich auf ein bestimmtes Formular beziehen. Davon betrachte man nur jene Einträge, die sich auf einen\*eine bestimmten\*bestimmten Bewerber\*in beziehen. Bildet man nun den Durchschnitt aller dieser Einträge erhält man den _Formular-Score_. (="Wie wurde ein\*eine Bewerber\*in durchschnittlich mit einem bestimmten Formular bewertet")

**Formularkategorie-Score:** Man betrachte alle Formulare einer Kategorie (Screening, Assessment) sowie einen\*eine bestimmen\*bestimmte Bewerber\*in. Der Durchschnitt aller _Formular-Scores_ von diesem\*dieser Bewerber\*in wird _Formularkategorie-Score_ genannt. (="Wir wurde ein\*eine Kandida\*in in einer Kategorie bewertet")

### Bewerber\*innengutachten

Ein Gutachten bezieht sich auf einen\*eine Bewerber\*in sowie eine _Formularkategorie_ und gibt einen Überblick über die allgemeine Bewertung des\*der Bewerber\*in.
Im folgenden werden wichtige Begriffe erläutert:

#### Formularkategorie

**Formularkategorie-Score:** Siehe [Ranking](#ranking)

**OverallAvg-Formularkategorie-Score:** Man betrachte den _Formularkategorie-Score_ jedes\*jeder einzelnen Bewerber\*in. Der Durschnitt von all diesen wird _AverallAvg-Formularkategorie-Score_ genannt. (="Wie wurden Bewerber\*innen durchschnittlich in dieser Kategorie bewertet")

**OverallStdDev-Formularkategorie-Score:** Man betrachte den _Formularkategorie-Score_ jedes\*jeder einzelnen Bewerber\*in. Die Standardabweichung von diesem Datensatz wird _StdDev-Formularkategorie-Score_ genannt. (="Wie stark schwanken die Bewertungen in dieser Kategorie")

**OverallMax-Formularkategorie-Score:** Man betrachte den _Formularkategorie-Score_ jedes\*jeder einzelnen Bewerber\*in. Der maximal Wert wird _OverallMax-Formularkategorie-Score_ genannt. (="Was ist die höchste Bewertung in dieser Kategorie")\
**OverallMin-Formularkategorie-Score:** Man betrachte den _Formularkategorie-Score_ jedes\*jeder einzelnen Bewerber\*in. Der minimale Wert wird _OverallMin-Formularkategorie-Score_ genannt. (="Was ist die niedrigste Bewertung in dieser Kategorie")

**PossibleMax-Formularkategorie-Score:** Der größtmögliche _Formularkategorie-Score_. Sollte für einen\*eine Bewerber\*in ein oder mehrere Formulare dieser Kategorie nicht ausgefüllt werden, liegt der mögliche Maximalwerte dennoch bei der Summe _aller_ _PossibleMax-Formular-Scores_.\
**PossibleMin-Formularkategorie-Score:** Der kleinstmögliche _Formularkategorie-Score_.

#### Formular

**Formular-Score:** Siehe [Ranking](#ranking)

**StdDev-Formular-Score:** Man betrachte ein bestimmtes Formular und berechne alle [_Formulareintrags-Scores_](#ranking) für einen\*eine Kanditat\*in. Die Standardabweichung von diesem Datensatz wird _StdDev-Formular-Score_ genannt. (="Wie stark schwanken die Bewertungen in dieser Übung")

**OverallAvg-Formular-Score:** Man betrachte ein bestimmtes Formular und berechne den _Formular-Score_ für alle Kanditat\*innen. Der Durchschnitt dieser _Forumlar-Scores_ wird _OverallAvg-Formular-Score_. (="Wie wurden Bewerber\*innen durschnittlich mit diesem Formular bewertet.")

**OverallAvgStdDev-Formular-Score:** Man berechne den _StdDev-Formular-Score_ für alle Kanditat\*innen. Der Durchschnitt von diesem Datensatz wird _OverallAvgStdDev-Formular-Score_ genannt. (="Wie stark schwanken durchschnittlich die Bewertungen in dieser Übung.")

**OverallStdDev-Formular-Score:** Man berechne alle _Formular-Scores_ einer Kategorie. Die Standardabweichung von diesem Datensatz wird _OverallStdDev-Formular-Score_ genannt. (="Wie stark schwanken die Bewertungen in dieser Übung insgesamt")

**OverallMax-Formular-Score:** Man betrachte den _Formular-Score_ jedes\*jeder einzelnen Bewerber\*in. Der maximal Wert wird _OverallMax-Formular-Score_ genannt. (="Was ist die höchste Bewertung in dieser Übung")\
**OverallMin-Formular-Score:** Man betrachte den Formular-Score\* jedes\*jeder einzelnen Bewerber\*in. Der minimale Wert wird _OverallMin-Formular-Score_ genannt. (="Was ist die niedrigste Bewertung in dieser Übung")

**PossibleMax-Formular-Score:** Der größtmögliche _Formular-Score_.\
**PossibleMin-Formular-Score:** Der kleinstmögliche _Formular-Score_.

#### Formularfeld

**Formularfeld-Score:** Man betrachte die Werte aller _Formulareintragsfelder_ zu einer bestimmten Bewerber\*in sowie zu einem bestimmten Feld. Berechnet man davon den Durchschnitt erhält man den _Formularfeld-Score_. (="Wie wurde dieser\*diese Kanditat\*in bei diesem Feld bewertet")

**StdDev-Formularfeld-Score:** Man betrachte die Werte aller _Formulareintragsfelder_ zu einer bestimmten Bewerber\*in sowie zu einem bestimmten Feld. Berechnet man davon die Standardabweichung erhält man den _StdDev-Formularfeld-Score_. (="Wie stark schwanken die Bewertungen in dieser Frage für diesen\*diese Bewerber\*in")

**OverallAvg-Formularfeld-Score:** Man betracht ein Formularfeld und berechne den _Formularfeld-Score_ für alle Bewerber\*innen. Der Durchscnitt dieser Werte wird _OverallAvg-Formularfeld-Score_ genannt. (="Wie wurden Kanditat\*innen durschnittlich bei diesem Feld bewertet")

**OverallAvgStdDev-Formularfeld-Score:** Man berechne den _StdDev-Formularfeld-Score_ für alle Kanditat\*innen für ein Feld. Der Durchschnitt von diesem Datensatz wird _OverallAvgStdDev-Formularfeld-Score_ genannt. (="Wie stark schwanken durchschnittlich die Bewertungen in dieser Frage")

**OverallStdDev-Formularfeld-Score:** Man betrachte die Werte aller _Formulareintragsfelder_ zu einem bestimmten Feld. Berechnet man davon die Standardabweichung erhält man den _OverallStdDev-Formularfeld-Score_. (="Wie stark schwanken die Bewertungen in diesem Feld")

**OverallMax-Formularfeld-Score:** Man betrachte den _Formularfeld-Score_ jedes\*jeder einzelnen Bewerber\*in eines bestimmenten Feldes. Der maximal Wert wird _OverallMax-Formularfeld-Score_ genannt. (="Was ist die höchste Bewertung in dieser Frage")\
**OverallMin-Formularfeld-Score:** Man betrachte den _Formularfeld-Score_ jedes\*jeder einzelnen Bewerber\*in eines bestimmenten Feldes. Der minimale Wert wird _OverallMin-Formularfeld-Score_ genannt. (="Was ist die kleinste Bewertung in dieser Frage")

**PossibleMax-Formularfeld-Score:** Der größtmögliche _Formularfeld-Score_.\
**PossibleMin-Formularfeld-Score:** Der kleinstmögliche _Formularfeld-Score_.

#### Anforderungskriterien

**Anforderungskriterium-Score:** Man betrachte alle Formularfelder, die auf ein bestimmtes Anforderungskriterium abziehlen und sich auf einen\*eine bestimmeten\*bestimmte Bewerber\*in. Berechnet man nun den Durchschnitt der dazugehörigen _Formulareintragsfeld-Scores_ erhält man den _Anforderungskriterium-Score_. (="Wie wurden ein\*eine Bewerber\*in in diesem Kriterium berwertet")

**OverallAvg-Anforderungskriterium-Score:** Man betrachte ein Anforderungskriterium und berechne sich den _Anforderungskriterium-Score_ für alle für alle Bewerber\*innen. Der Durchschnitt dieser Werte wird
_Avg-Anforderungskriterium-Score_ geannt. (="Wie wurden Bewerber\*innen durchschnittlich in diesem Kriterium berwertet")

**OverallStdDev-Anforderungskriterium-Score:** Man betrachte ein Anforderungskriterium und berechne sich den _Anforderungskriterium-Score_ für alle für alle Bewerber\*innen. Die Standardabweichung dieser Werte wird _StdDev-Anforderungskriterium-Score_ geannt. (="Wie stark schwanken die Bewertungen in diesem Kriterium")

**OverallMax-Anforderungskriterium-Score:** Man betrachte den _Anforderungskriterium-Score_ jedes\*jeder einzelnen Bewerber\*in eines bestimmenten Kriteriums. Der maximal Wert wird _OverallMax-Anforderungskriterium-Score_ genannt. (="Was ist die höchste Bewertung in diesem Kriterium")\
**OverallMin-Anforderungskriterium-Score:** Man betrachte den _Anforderungskriterium-Score_ jedes\*jeder einzelnen Bewerber\*in eines bestimmenten Kriteriums. Der minimale Wert wird _OverallMin-Anforderungskriterium-Score_ genannt. (="Was ist die kleinste Bewertung in diesem Kriterium")

**PossibleMax-Anforderungskriterium-Score:** Der größtmögliche _Anforderungskriterium-Score_.\
**PossibleMin-Anforderungskriterium-Score:** Der kleinstmögliche _Anforderungskriterium-Score_.
