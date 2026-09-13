# News-Digest-Automation

Mein bisher drittes Projekt gebaut mit n8n. Holt sich automatisch die aktuellen Nachrichten von der Tagesschau und wird zusammengefasst per Email verschickt

## Was das System macht 

Der Workflow liest den Tagesschau-RSS-Feed aus und nimmt sich die ersten drei Artikel. Jeder Artikel wird einzeln durch eine KI (Groq) geschickt und in zwei Sätzen zusammengefasst. Am Ende werden alle drei Zusammenfassungen zu einer Email zusammengefügt und automatisch verschickt.

Das war das erste Projekt das ich via Loop gebaut habe, somit eine neue wichtige Mechanik erlernt habe.

## Verwendet

- n8n
- RSS Feed Read
- Groq API (openai/gpt-oss-120b)
- Gmail API

## Zum Ausprobieren

Der Workflow (Newsletter-Zusammenfassung.json) lässt sich in eine eigene n8n-Instanz importieren. Braucht dann einen eigenen Groq API-Key und eine eigene Gmail-Verbindung

## Was noch nicht so gut ist

- Läuft nur manuell (per Klick), somit ist es kein automatischer Zeitplan
- Keine Fehlerbehandlung, falls die KI mal kein sauberes Ergebnis liefert
- Feste Anzahl von 3 Artikeln, nicht konfigurierbar

Das war mein drittes und aktuell neuestes Projekt. Ich komme langsam immer mehr rein und es fällt mir immer einfacher diese Workflows zu erstellen.
