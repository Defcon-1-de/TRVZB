Dieser Home‑Assistant‑Blueprint steuert Heizkörper‑Thermostate wie das Sonoff TRVZB vollständig über Home Assistant und ersetzt damit die herstellerseitige Automatik.

Funktionen im Überblick:

Komfort‑Betrieb mit Delta‑Hysterese: Die Heizung wird eingeschaltet, wenn die Differenz zwischen eingestellter Komfort‑Temperatur und aktueller Raumtemperatur einen einstellbaren Schwellwert überschreitet, und wieder abgeschaltet, sobald die Komfort‑Temperatur erreicht ist.
​
Absenkbetrieb außerhalb der Heizzeiten: Über einen Zeitplan (Schedule‑Helper) wird zwischen Komfort‑Temperatur und frei definierbarer Absenktemperatur gewechselt, damit Räume nicht unnötig auskühlen, aber Energie gespart wird.
​
Fenster‑Erkennung mit höchster Priorität: Wenn ein konfigurierter Fenstersensor „offen“ meldet, wird das Thermostat auf eine separate Fenster‑Abschalttemperatur (bis 0 °C) gesetzt und bleibt dort, solange das Fenster offen ist – unabhängig von Heizzeiten oder Absenkbetrieb.
​
Optionaler externer Temperatursensor: Statt der internen TRV‑Messung kann ein beliebiger externer Sensor als Regelgröße verwendet werden, was vor allem bei ungünstig platzierten Thermostaten sinnvoll ist.
​
Optionaler Override‑Schalter: Ein Override‑Entity (z.B. input_boolean oder Schalter) erlaubt es, die automatische Regelung temporär zu deaktivieren, ohne dass Fenster‑Schutzmechanismen dabei außer Kraft gesetzt werden.
​
Optionaler Speicher für letztes Komfort‑Setpoint: Über einen input_number‑Helper kann das zuletzt gesetzte Komfort‑Setpoint persistiert und nach Override oder Fenster‑Öffnung wiederhergestellt werden, auch nach einem Neustart von Home Assistant.
​
Der Blueprint ist so aufgebaut, dass alle erweiterten Funktionen (externer Sensor, Zeitplan, Override, Speicher‑Helper) optional sind und bei Bedarf direkt aus dem Entity‑Selector der Blueprint‑Konfiguration heraus angelegt werden können.
​
