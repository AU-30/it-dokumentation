# Windows Server

## Windows Server Rollen

Windows Server stellt verschiedene **Rollen** bereit, die jeweils einen bestimmten Dienst oder eine Funktion im Netzwerk übernehmen.
Rollen werden über den **Server-Manager** oder per PowerShell (`Install-WindowsFeature`) installiert und konfiguriert.

### Wichtige Rollen im Überblick

- **Active Directory Domain Services (AD DS):** Zentrale Verwaltung von Benutzern, Gruppen, Computern und Richtlinien in einer Domäne. AD DS ist die Grundlage für die Authentifizierung und Autorisierung im Windows-Netzwerk.
- **DNS-Server:** Löst Hostnamen in IP-Adressen auf und ist für die Funktion von Active Directory zwingend erforderlich. Wird in der Regel zusammen mit AD DS auf dem Domänencontroller betrieben.
- **DHCP-Server:** Verteilt automatisch IP-Adressen, Subnetzmasken, Gateways und DNS-Server an Clients im Netzwerk, sodass keine manuelle Konfiguration an jedem Endgerät nötig ist.
- **Dateiserver (File Services):** Stellt zentrale Dateifreigaben bereit, auf die Benutzer über das Netzwerk zugreifen können. Unterstützt Berechtigungen auf Freigabe- und NTFS-Ebene.
- **Druckserver (Print Services):** Verwaltet Drucker und Druckerwarteschlangen zentral, sodass Clients Drucker einfach über das Netzwerk nutzen können.
- **Webserver (IIS):** Hostet Websites und Webanwendungen auf Basis der Internet Information Services (IIS).
- **Hyper-V:** Ermöglicht die Virtualisierung, sodass mehrere virtuelle Maschinen auf einem physischen Server betrieben werden können.
- **Windows Deployment Services (WDS):** Ermöglicht die netzwerkbasierte Installation von Betriebssystemen auf Clients über PXE-Boot.

Jede Rolle kann unabhängig installiert werden. In kleineren Umgebungen werden häufig mehrere Rollen auf einem einzigen Server kombiniert, während in größeren Umgebungen die Rollen auf dedizierte Server verteilt werden, um Leistung und Ausfallsicherheit zu erhöhen.
