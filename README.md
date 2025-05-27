📌 Concepts clés
AMI (Amazon Machine Image) : modèle système utilisé pour lancer l’instance.

Instance type : configuration matérielle de l’instance (ex : t2.micro).

Key Pair : paire de clés pour accéder à l’instance via SSH.

Security Groups : pare-feu virtuel contrôlant le trafic entrant/sortant.

IAM Policy & Role : gestion des permissions et association à l’instance EC2.

🧪 Étapes principales de l’exercice
🔐 1. Création de la politique IAM
Une politique permettant d’utiliser iam:ListGroups est définie.

Elle autorise l’instance à interroger la liste des groupes IAM.

👥 2. Sélection de la permission ListGroups
Permet à l’instance de récupérer tous les groupes IAM via l’API.

🎭 3. Association de la politique à un rôle IAM
⚙️ 4. Création d’un rôle IAM spécifique pour EC2
Le rôle est lié au service EC2 pour lui accorder les permissions IAM.

🔗 5. Vérification de la création du rôle EC2
🔒 6. Création du groupe de sécurité
Port 22 (SSH) ouvert pour l’accès distant.

Port 80 (HTTP) ouvert pour l’accès web.

🖥️ 7. Création de l’instance EC2
Type : t2.micro, système Ubuntu (ou Amazon Linux selon le contexte).

Rôle IAM et groupe de sécurité sont associés à l’instance.

🌐 8. Récupération de l’adresse IP publique
✅ 9. Accès à la page web générée par le script "User Data"
La page HTML affiche dynamiquement les groupes IAM disponibles.


1 - Avant de creer l'instance il est important de creer une politique et l'associé à l'instance ----

<img width="937" alt="image" src="https://github.com/user-attachments/assets/87c16f0b-1009-4911-a0d6-9051df18c3b7" />

2 - selectionnez liste groupe pour permettre de lister l'ensemble des groupe IAM

<img width="953" alt="image" src="https://github.com/user-attachments/assets/fd191739-cb7a-48f3-b2f7-4b61b42815e4" />

3 - la politique etant crée il faut l'associé à un role 

<img width="956" alt="image" src="https://github.com/user-attachments/assets/c4973a52-0c99-4284-bf72-a7e4d17bbe6e" />

4 -  creer un role tout en selectionnant le service EC2

<img width="949" alt="image" src="https://github.com/user-attachments/assets/8234a1cf-5023-4df5-b529-40b3f0722ba4" />

5- EC2 role crée 

<img width="952" alt="image" src="https://github.com/user-attachments/assets/44ca6902-3c18-4109-9a12-866a932af311" />

6 - creation du groupe securité pour notre EC2 afin de controler les flux entrant et sortant 

<img width="954" alt="image" src="https://github.com/user-attachments/assets/7460a509-b45b-4ca0-aff1-e22145ba129d" />

7 - creation de l'instance EC2 ---

<img width="958" alt="image" src="https://github.com/user-attachments/assets/5165532b-cfbb-45c8-a255-269d2092199f" />

8 -- copié l'adresse IP publique de votre instance EC2

<img width="959" alt="image" src="https://github.com/user-attachments/assets/b54b2691-d8f8-4785-a249-adc75f806621" />

9 -- votre page web est déjà accessible 

<img width="859" alt="image" src="https://github.com/user-attachments/assets/8ba64c38-9e35-43a1-a125-7b78067def0d" />






