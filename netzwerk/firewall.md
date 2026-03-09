# Firewall

## Grundlagen einer Firewall

Eine Firewall ist ein Sicherheitssystem, das den ein- und ausgehenden Netzwerkverkehr anhand definierter Regeln überwacht und kontrolliert.
Ihr Hauptzweck ist es, ein vertrauenswürdiges internes Netzwerk vor unautorisierten Zugriffen aus externen Netzwerken (z. B. dem Internet) zu schützen.

### Funktionsweise

Firewalls arbeiten mit **Regeln (Rules)**, die festlegen, welcher Datenverkehr erlaubt oder blockiert wird.
Diese Regeln basieren typischerweise auf Kriterien wie Quell- und Ziel-IP-Adresse, Portnummer und verwendetem Protokoll (TCP, UDP, ICMP).
Dabei gilt in der Regel das Prinzip **„Deny All"** – alles wird zunächst blockiert, und nur explizit freigegebener Verkehr wird durchgelassen.

### Arten von Firewalls

- **Paketfilter-Firewall:** Prüft jedes einzelne Datenpaket anhand von Header-Informationen (IP, Port, Protokoll) und entscheidet, ob es weitergeleitet oder verworfen wird.
- **Stateful Inspection Firewall:** Merkt sich den Zustand aktiver Verbindungen und kann dadurch zusammengehörige Pakete erkennen. Antwortpakete einer erlaubten Verbindung werden automatisch zugelassen.
- **Application Layer Firewall (Proxy):** Arbeitet auf Anwendungsebene und kann den Inhalt des Datenverkehrs analysieren (z. B. HTTP, FTP). Bietet tiefere Kontrolle, ist aber aufwändiger.
- **Next-Generation Firewall (NGFW):** Kombiniert klassische Firewall-Funktionen mit zusätzlichen Sicherheitsfeatures wie Intrusion Prevention (IPS), Deep Packet Inspection und Anwendungserkennung.

Firewalls können als **Hardware-Appliance** (z. B. am Netzwerk-Perimeter) oder als **Software-Firewall** (z. B. Windows Defender Firewall auf einem einzelnen Host) betrieben werden.
