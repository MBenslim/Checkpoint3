
Partie 1 : Gestion des utilisateurs

L'utilisateur Kelly Rhameur a quitté l'entreprise.
Elle est remplacée par Lionel Lemarchand

Q.1.1.1 Créer l'utilisateur Lionel Lemarchand avec les même attribut de société que Kelly Rhameur.

![VirtualBox_Checkpoint3-SRVWIN01_20_06_2025_09_53_36](https://github.com/user-attachments/assets/d4955aad-fc99-456b-a9a6-71c91628a9a8)


Q.1.1.2 Créer une OU DeactivatedUsers et déplace le compte désactivé de Kelly Rhameur dedans.

![VirtualBox_Checkpoint3-SRVWIN01_20_06_2025_10_00_35](https://github.com/user-attachments/assets/0f238e64-6d5e-4adf-9dfe-9f079789c622)


Q.1.1.3 Modifier le groupe de l'OU dans laquelle était Kelly Rhameur en conséquence.

![VirtualBox_Checkpoint3-SRVWIN01_20_06_2025_10_04_47](https://github.com/user-attachments/assets/d95a71dc-05a7-4ede-82dc-72b10e9ad3a5)


Q.1.1.4 Créer le dossier Individuel du nouvel utilisateur et archive celui de Kelly Rhameur en le suffixant par -ARCHIVE.
pas fait

Partie 2 : Restriction utilisateurs

Q.1.2.1 Faire en sorte que l'utilisateur Gabriel Ghul ne puisse se connecter que du lundi au vendredi, de 7h à 17h.

![VirtualBox_Checkpoint3-SRVWIN01_20_06_2025_10_14_06](https://github.com/user-attachments/assets/647c6acf-8ea3-41f0-9a21-eb06faf94722)

Q.1.2.2 De même, bloquer sa connexion au seul ordinateur CLIENT01.

![VirtualBox_Checkpoint3-SRVWIN01_20_06_2025_10_18_06](https://github.com/user-attachments/assets/02cdd2d6-3887-45ed-a762-b88c18dcca15)

Q.1.2.3 Mettre en place une stratégie de mot de passe pour durcir les comptes des utilisateurs de l'OU LabUsers.

![VirtualBox_Checkpoint3-SRVWIN01_20_06_2025_10_27_59](https://github.com/user-attachments/assets/719deb60-1884-43c7-ad4a-6124e7ac2fff)


Partie 3 : Lecteurs réseaux

Q.1.3.1 Créer une GPO Drive-Mount qui monte les lecteurs E: et F: sur les clients.

![VirtualBox_Checkpoint3-SRVWIN01_20_06_2025_10_44_21](https://github.com/user-attachments/assets/e06dba15-8bd0-4d15-b100-8964f7b5b248)
