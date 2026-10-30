# Direccionamiento

Transcrito de la captura de la topología; conviene verificarlo contra las configuraciones de cada equipo.

## Enlaces punto a punto
| Enlace | Subred | Extremos |
|---|---|---|
| R1 g0/0 – ESW1 f0/0 | 172.16.4.0/30 | .1 – .2 |
| R1 g1/0 – ESW2 f1/0 | 172.16.4.4/30 | .5 – .6 |
| R1 g2/0 – ESW3 f0/0 | 172.16.4.8/30 | .9 – .10 |
| ESW1 f1/5 – ESW2 f1/3 | 172.16.4.12/30 | .13 – .14 |
| R1 g4/0 – R-DMZ f0/0 | 172.16.4.16/30 | .17 – .18 |

## VLAN y zonas
| VLAN / zona | Subred | Gateway |
|---|---|---|
| 10 Marketing | 172.16.0.0/24 | 172.16.0.1 |
| 20 Invitados | 172.16.1.0/25 | 172.16.1.1 |
| 30 Contabilidad | 172.16.1.128/25 | 172.16.1.129 |
| 40 Gestión TI | 172.16.2.0/26 | 172.16.2.1 |
| 50 Gerencia | 172.16.2.64/27 | 172.16.2.65 |
| DMZ | 172.16.2.96/28 | 172.16.2.97 |
| 80 Gestión | 172.16.2.112/28 | 172.16.2.113 |
| 90 Nativa/trunk | sin IP | no aplica |

## Hosts destacados
- DMZ-Server: 172.16.2.100
- Estación de gestión MGT (VLAN 80): 172.16.2.114
- Servidor interno: 172.16.2.41 (gateway 172.16.2.2)
