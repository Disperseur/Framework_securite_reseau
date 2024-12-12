# Notes sécurité des réseaux


# Pour voir son ip: 
``$sudo ifconfig``

# Pour scanner les appareils actifs sur le réseau:
``$sudo fping -s -g ip_deb ip_fin --alive -q``

# Pour scanner un appareil:
``$sudo nmap -sS ip_appareil``

# Pour scanner les différents services d'un appareil

## Telnet

``$telnet <ip_addr> <port>``\
puis hit Esc et Enter
-> affiche la banniere

## netcat (nc)
``$nc <ip_addr> <port>``\
``$GET /index.html``

## nmap (best)
``$nmap -sV -script=banner <ip_addr>``

# Pour obtenir un accès 

## hydra(bruteforce)
``hydra -L /usernames.txt -P /passwords.txt <ip_app> ftp -V`` (ftp)
``hydra -L usernames.txt -P passwords.txt <ip_app> ssh -V`` (SSH)

## Netcat 

``nc <ip_app> <port>``

## Metasploit 

``use <exploit>``           -choix de l'exploit à utiliser
``---``                     -commande particulière à l'exploit utiliser
``set RHOSTS $TARGET_IP``   -il faut donner l'ip ciblé
``---``                     -commande particulière à l'exploit utilisé
``exploit``                 - execution de l'exploit 





