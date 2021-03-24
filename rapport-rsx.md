################# Rapport TP 3 RSX2 ##########################


1 – ROUTAGE STATIQUE :
----------------------

1) - La commande ip route ne renvoie aucune table de routage pour les 3 routeurs car les interfaces des routeurs ne sont pas configurées.
  - Activer et configurer les interfaces des 3 routeurs
    - Routeur 1:
    ```
R1:~# ifconfig eth0 211.230.193.1/26
R1:~# ifconfig eth1 211.230.193.129/26
R1:~# ip route add 211.230.193.64/26 via 211.230.193.2
R1:~# ip route add 211.230.193.192/26 via 211.230.193.130
    ```
    - Routeur 2:
    ```
R2:~# ifconfig eth0 211.230.193.2/26
R2:~# ifconfig eth1 211.230.193.65/26
R2:~# ip route add 211.230.193.128/26 via 211.230.193.1
R2:~# ip route add 211.230.193.192/26 via 211.230.193.1

    ```
    - Routeur 3:
    ```
R3:~# ifconfig eth0 211.230.193.130/26
R3:~# ifconfig eth1 211.230.193.193/26
R3:~# ip route add 211.230.193.0/26 via 211.230.193.129
R3:~# ip route add 211.230.193.64/26 via 211.230.193.129

    ```
- En affichant les tables de routage à nouveau, celles-ci ne sont pas vides car l’interface a été configurée et l’adresse IP de la machine a été ajoutée à l’interface eth0.
– Les adresses ajoutées sont des adresses réseau(network address)

2)




2 – TRACEROUTE:
---------------
1- R2:~# traceroute 211.230.193.193



ip address del address dev eth0/eth1
