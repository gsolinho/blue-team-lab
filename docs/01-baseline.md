# Proyecto laboratorio Blue Team Día 1

## Qué es el lab y qué monté:
- Instalé dos Debian 13 en VMWare Workstation, en red host-only para hacer practicas de Blue Team registrando log, posibles ataques, IPS...

## Topología:
| Máquina | Rol | Host-only | NAT | Notas |
|---|---|---|---|---|
| `eden` | Tu PC (analista) | 172.16.165.1 | — | Aquí está el repo |
| `srv-web` | Servidor a defender | `172.16.165.10` (`ens37`) | `ens33` (dinámica) | Debian 13, SSH, Nginx |
| `atacante` | Atacante | `172.16.165.20` | sí, para instalar | Debian 13 mínima |

## Qué servicios tengo en el srv-web hasta ahora:
- SSH en el puerto 22
- Nginx en el puerto 80

## Problemas que tuve hasta ahora:
- No instalé el GRUB la primera vez, sin bootloader no arranca, necesidad de reinstalar.
- sources.list solo tenia cdrom, faltaba por añadir los repos de Debian
- Diferencias entre "su" y "su -"
- Intentar leer el log de Nginx sin sin ser root
