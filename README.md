# Raum-Classifier
In diesem Repository finden Sie einen Raum-Classifier, der mit dem StanfordNER kompatibel ist, sowie dazugehörige Trainingsdaten. 

Die Datei "Raum320000_18-21_ner-model" ist ein Raum-Classifier mit sieben Unterkategorien, die mit dem StanfordNER kompatibel sind. Die Datei "Raum320000_18-21_ner-model_ohneMetaphern" entält den gleichen Classifier mit sechs Raum-Kategorien (Metaphern sind hier weggelassen). Die Kategorien sind:
Ort
Relation
relationeles Verb
Raumhinweis
Raumbeschreibung
Raumthema
Raummetapher

Die Datei "Raum320000_18-21_ner-model_ohneMetaphern" ist die empfohlene Version zur Anwendung. 

Beide Classifier können wie folgt verwendet werden:

1. Laden Sie sich die Classifier herunter
2. Laden Sie sich das Named-Entity-Recognition-Tool StanfordNER herunter
3. Öffnen Sie den Stanford-Named-Entity-Recognizer wie auf der Seite der Stanford NLP Group beschrieben
4. Laden Sie über "Classifier" > "Load CRF from file" den Raum-Classifier in das Tool
5. Wählen Sie über "File" > "Open File" ein  Dokument, in dem Raumausdrücke annotiert werden sollen
6. Klicken Sie auf "Run"

Die annotierten Daten können über "File" > "Save tagged file as" gespeichert und weiter verwendet werden. 

Die Annotationskategorien des Raum-Classifiers erreichen unterschiedliche Erkennungsquoten. Eine detaillierte Übersicht der Gesamterkennunggenauigkeit (F1-Score) der einzelnen Kategorien finden Sie im Unterordner "Modell Testreihen". Im Unterordner "Testreihen mit 7 Kategorien" sind im Dokument "7 Kategorien NER-Test Übersicht.xlsx" ausführliche Tests des gesamten Traningsprozesses dokumentiert. Getestet wurde mit acht Testtexten aus vier Jahrhunderten. Durchschnittswerte finden sich im Tabellenblatt "einige Durchschnittswerte". Die abschließenden Tests der finalen Classifier finden sich in den Zeilen 20 und 21. Werte für die einzelnen Testtexte aus den Jahrhunderten 18-21 sind in den anderen Tabellenblättern verzeichnet.

Die annotierten Testtexte können - so weit das urheberrechtlich möglich ist, aus dem Unterordner "annotierte Testtexte" heruntergeldane werden. Hierin finden Sie sechs annotierte Texte in Tabellenform aus den Jahrhunderten 18-20 (die nicht gemeinfreien Texte aus dem 21. Jahrhundert können hier nicht zugänglich gemacht werden).

Außerdem in diesem Repository zu finden sind:
- die Dokumentation von Tests eines ersten, nicht implementierten Modells (Ordner "Vorabtests - nicht implementierte Varianten")
- Anzahl der Annotationen im Trainingskorpus (im Ordner "Testreihen mit 7 Kategorien")

Imformationen und Daten zum Trainig des Raum-Classifiers finden sich im Ordner "Training CRF-Classifier". Hierin ist eine Auflistung der Texte im Trainingskorpus enthalten. Aus jedem der aufgelisteten Texte wurden 4.000 Tokens direkt vom Anfang entnommen und ins Trainingskorpus integriert. Das Trainingskorpus besteht insgesamt aus 320.000 Tokens aus 80 Romanen aus vier Jahrhunderten (18-21). Annotierte Trainingsdaten im Tabellenformat TSV (kompatibel mit dem StanfordNER-Tool) finden sich im Unterordner "Trainingsdaten". Die Trainingsdaten aus dem 20. und 21. Jahrhundert enthalten urheberrechtlich geschütztes Material und können darum nicht öffentlich zugänglich gemacht werden. Die Trainingsdaten aus dem 18. und 19. Jahrhundert können jahrhundertweise heruntergeladen werden. Sowohl die Variante mit als auch die ohne Metaphern steht zur Nachnutzung zur Verfügung. Das Trainingskorpus umfasst 80.000 Tokens / Jahrhundert. Informationen zu den im Raum-Classifier implementierten Features können in der Properties-Datei "Raum.prop" eingesehen werden.
