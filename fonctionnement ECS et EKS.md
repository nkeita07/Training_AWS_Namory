AWS propose plusieurs alternatives aux instances EC2 pour héberger des applications web ou des API, notamment basées sur la conteneurisation ou le serverless :

1. Conteneurisation
Docker permet de créer des conteneurs légers au lieu de machines virtuelles.

Amazon ECS (Elastic Container Service) orchestre ces conteneurs :

Mode EC2 : vous gérez vous-même les instances.

Mode Fargate : AWS gère l'infrastructure (recommandé).

Amazon ECR stocke vos images Docker.

Pour l’ECS, on définit des "task definitions" et on attribue des rôles IAM pour autoriser les actions.

2. Amazon EKS (Elastic Kubernetes Service)
Basé sur Kubernetes, compatible avec d’autres clouds (GCP, Azure).

Déploiement possible avec :

Nœuds EC2 autogérés

Groupes de nœuds gérés

Fargate

Supporte plusieurs systèmes de stockage (EBS, EFS, etc.).

3. AWS Elastic Beanstalk
Solution simple et gratuite pour déployer une application web sans gérer l’infrastructure.

Automatisé via CloudFormation.

4. AWS App Runner
Service encore plus simple pour déployer une application conteneurisée sans connaissance technique sur l’infra.

5. Solutions Serverless
AWS Lambda : exécute du code uniquement à la demande (jusqu’à 15 minutes).

Avantages : pas de gestion de serveur, coût à l’utilisation, supporte plusieurs langages.

AWS Step Functions : orchestre des fonctions Lambda sous forme de flux visuels.

En résumé :
ECS/EKS pour gérer des conteneurs.

Fargate/Lambda pour du serverless sans gestion d’infrastructure.

Elastic Beanstalk/App Runner pour des applications web simples.

Choisissez selon vos besoins en simplicité, contrôle ou portabilité.
