# IP-Konzept

## IPv4 Grundlagen

Eine IPv4-Adresse ist eine 32-Bit-Adresse, die ein Gerät in einem Netzwerk eindeutig identifiziert.
Sie wird in der sogenannten Dezimal-Punkt-Notation dargestellt, bestehend aus vier Oktetten, die jeweils durch einen Punkt getrennt sind (z. B. 192.168.1.10).
Jedes Oktett kann einen Wert von 0 bis 255 annehmen.

Eine IPv4-Adresse setzt sich aus zwei Teilen zusammen: dem **Netzanteil** und dem **Hostanteil**.
Der Netzanteil identifiziert das Netzwerk, in dem sich das Gerät befindet, während der Hostanteil das einzelne Gerät innerhalb dieses Netzwerks bestimmt.
Die Aufteilung zwischen Netz- und Hostanteil wird durch die **Subnetzmaske** festgelegt (z. B. 255.255.255.0 bzw. /24 in CIDR-Notation).

Es gibt verschiedene Adressklassen (A, B, C), die sich in der Größe des Netz- und Hostanteils unterscheiden.
Zusätzlich existieren private Adressbereiche, die nur innerhalb lokaler Netzwerke verwendet werden und nicht im Internet geroutet werden:

| Klasse | Privater Adressbereich         | Subnetzmaske    | CIDR  |
|--------|-------------------------------|-----------------|-------|
| A      | 10.0.0.0 – 10.255.255.255     | 255.0.0.0       | /8    |
| B      | 172.16.0.0 – 172.31.255.255   | 255.240.0.0     | /12   |
| C      | 192.168.0.0 – 192.168.255.255 | 255.255.0.0     | /16   |

Besondere Adressen sind die **Netzadresse** (Hostanteil = 0, z. B. 192.168.1.0/24) und die **Broadcast-Adresse** (Hostanteil = alle Bits auf 1, z. B. 192.168.1.255/24). Diese beiden Adressen können nicht an Hosts vergeben werden.
