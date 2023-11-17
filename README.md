# DevSecOps - Desafio Final
A seguir será apresentado a arquitetura desenvolvida, bem como a explicação dela. Demais recursos podem ser encontrados na apresentação.

![arquitetura](https://github.com/AnaMaria27/DevSecOps-DesafioFinal/assets/33530061/afc8c210-7a79-49a0-9447-b90b6322bddc)

- VPC: Criamos uma VPC para isolar nossos recursos.

- Subnets: Dividimos a VPC em várias sub-redes. Temos duas sub-redes públicas e quatro sub-redes privadas.

- NAT Gateway: Instalamos um NAT Gateway em cada uma das sub-redes públicas para fornecer acesso à Internet para as instâncias privadas.

- EC2 Instances: Implantamos nossos servidores de aplicativos (EC2 Instances) em sub-redes privadas. Essas instâncias são provisionadas e gerenciadas por um Auto Scaling Group, garantindo um escalonamento adequado em resposta à carga variável.

- ELB: Implementamos um Elastic Load Balancer para distribuir o tráfego entre as instâncias EC2 em nosso Auto Scaling Group.

- RDS: Usamos o Amazon RDS para fornecer um banco de dados gerenciado. Neste caso, o MySQL.

- EKS: Para execução de contêineres, utilizamos o Amazon EKS, um serviço gerenciado baseado no Kubernetes.

- AWS Backup: Configuramos o AWS Backup para fazer backup dos volumes EBS do EC2 Instances e do RDS.

- AWS CloudWatch: Monitoramos nossa arquitetura usando o AWS CloudWatch, que nos permite rastrear métricas e definir alertas.

- AWS IAM: Garantimos a segurança do acesso aos recursos da AWS usando o AWS Identity and Access Management (IAM).

- Availability Zones: Utilizamos diferentes zonas de disponibilidade (AZs) para garantir alta disponibilidade e resiliência em caso de falhas na infraestrutura da AWS.
