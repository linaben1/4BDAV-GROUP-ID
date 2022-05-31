# 4BDAV-GROUP-GROUP2

## Configuration de la VM

La première chose qui a été faite est la configuration de la VM. Pour ça on a procédé comme suit :

-Téléchargement plus extraction depuis VirtualBox

-Mise en français via les paramètres

Depuis le terminal on a fait :

-Connexion en tant qu'administrateur :

    [oracle@localhost ~]$ sqlplus

    SQL*Plus: Release 19.0.0.0.0 - Production on Tue May 31 08:56:09 2022
    Version 19.3.0.0.0

    Copyright (c) 1982, 2019, Oracle.  All rights reserved.

    Enter user-name: system
    Enter password: oracle
    Last Successful login time: Tue May 31 2022 07:46:31 -04:00

    Connected to:
    Oracle Database 19c Enterprise Edition Release 19.0.0.0.0 - Production
    Version 19.3.0.0.0

-Création d'un compte personnel et affectation des droits :

    SQL> CREATE USER <name> IDENTIFIED BY <password>;

    User created.

    SQL> GRANT CONNECT, RESOURCE to sylfried;

    Grant succeeded.

    SQL> GRANT CONNECT, RESOURCE to sylfried;

    Grant succeeded.

    SQL> GRANT UNLIMITED TABLESPACES TO <user>;

    Grant succeeded.

-Déconnexion puis connexion au nouveau compte créé :

    SQL> __exit__
    Disconnected from Oracle Database 19c Enterprise Edition Release 19.0.0.0.0 - Production
    Version 19.3.0.0.0
    [oracle@localhost ~]$ sqlplus

    SQL*Plus: Release 19.0.0.0.0 - Production on Tue May 31 07:47:10 2022
    Version 19.3.0.0.0

    Copyright (c) 1982, 2019, Oracle.  All rights reserved.

    Enter user-name: <user>
    Enter password: <password>
    Last Successful login time: Tue May 31 2022 05:51:08 -04:00

    Connected to:
    Oracle Database 19c Enterprise Edition Release 19.0.0.0.0 - Production
    Version 19.3.0.0.0

Et nous voilà connecté avec un compte personnel qui a les droits nécessaires pour créer, modifier, voir ou supprimer des tables.
