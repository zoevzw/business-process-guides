# Vom operativen Problem zur verständlichen IT-Anforderung

## 1. Warum „Das CRM muss besser werden“ keine umsetzbare Anforderung ist

Ein Änderungswunsch wird erst dann konkret, wenn Ausgangssituation, betroffene Rollen, benötigte Informationen und gewünschtes Verhalten zusammenpassen. Die Aufgabe der fachlichen Schnittstelle ist es, diese Informationen zu ordnen und offene Entscheidungen sichtbar zu machen.

## 2. Fünf Fragen vor jeder technischen Lösung

1. **Was passiert heute?** Einen konkreten Vorgang mit nachvollziehbaren Schritten beschreiben.
2. **Welche Auswirkung hat das?** Zusatzaufwand, unklare Verantwortung oder widersprüchliche Information benennen.
3. **Was ist fachlich geklärt?** Bestätigte Fakten, Annahmen und offene Entscheidungen trennen.
4. **Was soll künftig passieren?** Gewünschtes Verhalten aus Sicht der jeweiligen Rolle beschreiben.
5. **Woran erkennen wir die passende Umsetzung?** Beobachtbare Abnahmekriterien definieren.

## 3. Informationen aus verschiedenen Quellen zusammenführen

| Quelle | Was dort stehen kann | Was dadurch noch nicht geklärt ist |
| --- | --- | --- |
| Rückmeldung des Fachbereichs | Leistung wurde erbracht | Ob Umfang und Betrag der Bestellung entsprechen |
| CRM | Vorgang hat den Status „abgeschlossen“ | Welche fachliche Bedeutung dieser Status hat |
| Finanzsystem | Rechnung ist eingegangen | Ob Leistung und Rechnung bereits geprüft sind |
| Projektkommunikation | Es wurde über eine Änderung gesprochen | Ob eine zuständige Person die Änderung verbindlich freigegeben hat |

Widersprüche werden nicht stillschweigend aufgelöst. Sie werden als Klärungspunkt mit Quelle, verantwortlicher Person und benötigter Entscheidung dokumentiert.

## 4. Durchgängiges, frei erfundenes Beispiel

### Ist-Situation

Eine Retail-Koordinatorin setzt einen Vorgang nach Abschluss einer Dienstleistung im CRM auf „abgeschlossen“. In der Monatsübersicht wird derselbe Status als vollständiger finanzieller Abschluss interpretiert. Eine noch ungeklärte Rechnungsdifferenz bleibt unsichtbar.

### Fachliche Klärung

„Leistung erbracht“ und „Rechnung geklärt“ beschreiben unterschiedliche Sachverhalte. Das Team benötigt eine gemeinsame Definition. Ob und wann eine Zahlung erfolgen darf, bleibt Gegenstand des separat festgelegten Finanzprozesses.

### Ziel

Die Monatsübersicht zeigt den fachlichen Leistungsstatus und den Stand der Rechnungsprüfung getrennt. Offene Differenzen bleiben sichtbar und einer zuständigen Rolle zugeordnet.

### Anforderung REQ-DEMO-01

Für jeden betroffenen Vorgang werden der Leistungsstatus und der Rechnungsprüfstatus getrennt dargestellt. Eine Übersicht darf einen Vorgang nicht allein aufgrund des Leistungsstatus als vollständig finanziell geklärt ausweisen.

### Abnahmekriterien

- **Szenario A:** Leistung erbracht, Rechnung noch nicht eingegangen. Die Übersicht zeigt beide Sachverhalte; sie behauptet keinen vollständigen finanziellen Abschluss.
- **Szenario B:** Leistung erbracht, Rechnung mit ungeklärter Differenz vorhanden. Die Differenz und ihre zuständige Klärungsrolle sind erkennbar.
- **Szenario C:** Rechnung und Leistung fachlich geklärt. Die Darstellung folgt der gemeinsam definierten Statuslogik; Zahlungs- und Buchungsstatus werden dadurch nicht automatisch geändert.
- **Szenario D:** Bestehender Datensatz enthält nur den alten Status. Die Migration folgt einer abgestimmten Zuordnung oder kennzeichnet den Klärungsbedarf; sie erfindet keine fehlenden Informationen.

### Vor der Umsetzung noch zu entscheiden

- Wer darf die jeweiligen Status ändern?
- Welche Werte stammen aus dem CRM, welche gegebenenfalls aus einem anderen System?
- Welche Historie muss für die Beteiligten nachvollziehbar bleiben?
- Wer entscheidet über Ausnahmefälle?
- Welche Daten dürfen die einzelnen Rollen sehen?

## 5. Übergabe an die IT

Eine gute Übergabe enthält Problem, Ziel, betroffene Rollen, Informationen, Geschäftsregeln, Beispiele, offene Entscheidungen und Abnahmekriterien. Technische Architektur und Implementierungsdetails werden gemeinsam mit den zuständigen Fachkräften festgelegt.

Die Umsetzung sollte anschließend anhand des abgestimmten Beispiels fachlich überprüft werden. Für dieses Demonstrationsdokument wurde keine reale Systemumsetzung durchgeführt.

## 6. Fachlicher Mehrwert

Die Dokumentation hilft dabei, an verschiedenen Stellen vorhandenes Wissen zusammenzuführen. Sie reduziert vermeidbare Rückfragen und macht sichtbar, ob eine technische Änderung, eine fachliche Entscheidung oder eine klarere Zuständigkeit benötigt wird. Der tatsächliche Nutzen muss im jeweiligen Projekt überprüft werden.

Vorlagen: [IT-Anforderung](templates/it-requirement.md) und [Klärungslog](templates/decision-log.md).
