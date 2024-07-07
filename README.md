# K-Means-Clustering

**Anleitung zum ausführen des Notebooks:**
1. Klicken Sie auf das MyBinder Batch ↓
2. Warten Sie bis sich das Notebook geöffnet hat (bis zu 15min)
3. Das Notebook wird direkt aufgerufen und kann durch verwenden des Play-Button schrittweise ausgeführt werden

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/MichaelFranLu/Logistic-Regression/master?labpath=3-Logistische_Regression_Projekt-Loesung.ipynb)

**Update:**
Ausführen in Google Colab ebenfalls möglich & performatnter:
1. Klicken Sie auf den Google Colab Batch ↓
2. Warten Sie bis sich das Notebook geöffnet hat (maximal 10sek)
3. Das Notebook wird direkt aufgerufen und kann durch verwenden des Play-Button schrittweise ausgeführt werden

<a target="_blank" href="https://colab.research.google.com/github/MichaelFranLu/K-Means-Clustering/blob/main/3-K_Means_Clustering_Projekt-Loesung.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>




**Dokumentation - K-Means-Clustering**

In diesem Projekt wird der K Means Clustering Algorithmus angewendet, um US-Universitäten in private und öffentliche Einrichtungen zu kategorisieren. Obwohl die tatsächliche Zuordnung der Universitäten bekannt ist, wird sie ignoriert, um den Algorithmus als Unsupervised Learning Methode zu nutzen. Die Leistung des Algorithmus wird anhand der Zuteilung bewertet, wobei die Confusion Matrix und der Classification Report nur theoretische Auswertungen darstellen.
- Private: Dummy Varaible mit "Yes" für private und "No" für öffentliche Einrichtungen
- Apps: Anzahl an erhaltenen Bewerbungen
- Accept: Anzahl an angenommenen Bewerbungen
- Enroll: Anzahl neu eingeschriebener Studenten
- Top10perc: Prozent der neuen Studenten der Top 10% einer High School Klasse
- Top25perc: Prozent der neuen Studenten der Top 25% einer High School Klasse
- F.Undergrad: Anzahl an Vollzeitstudenten
- P.Undergrad: Anzahl an Teilzeitstudenten
- Outstate: Gebühr für Studenten, die aus einem anderen Staat kommen
- Room.Board: Kosten für Räume und Mitarbeiter
- Books: Geschätze Kosten für Bücher
- Personal: Geschätzte persönliche Ausgaben
- PhD: Prozent der Fakultäten mit Ph.D.'s
- Terminal: Prozent der Fakultäten mit Terminal Degree
- S.F.Ratio: Rate der Studenten pro Fakultät
- perc.alumni: Prozent der Alumni die spenden
- Expend: Verwaltungskosten pro Student
- Grad.Rate: Abschlussrate


**Benötigte Libraries instalieren**
- pandas
- numpy
- matplotlib
- seaborn

**Daten einlesen "College_Data.csv"**


**Explorative Datensanalyse**

In diesem Teil wird die explorative Datenanalyse unter Verwendung der Seaborn-Bibliothek ausgeführt. Es werden unterschiedliche Diagramme generiert, um Zusammenhänge und Muster zu entdecken:
- Scatterplot-Erstellung: “Grad.Rate” vs. “Room.Board”, eingefärbt nach “Private”
- Scatterplot-Erstellung: “F.Undergrad” vs. “Outstate”, eingefärbt nach “Private”
- Histogramm-Erstellung: Darstellung der “Out of State Tuition” (“Outstate”), geteilt nach “Private”
- Histogramm-Erstellung: Darstellung der “Grad.Rate”, geteilt nach “Private”
- Identifikation: Universität mit einer Abschlussrate von mehr als 100%
- Datenbereinigung: Setzen der Abschlussrate (“Grad.Rate”) auf 100 für die identifizierte Universität


**K Means Cluster**

Ein K-Means-Clustering-Modell mit 2 Clustern wird erstellt und auf die Daten angewendet.

**Vorhersagen und Auswertung**
Die Ergebnisse zeigen, dass das Modell eine Genauigkeit von 22% hat, was darauf hindeutet, dass es Raum für Verbesserungen gibt. Insbesondere scheint das Modell Schwierigkeiten zu haben, private Universitäten korrekt zu klassifizieren
