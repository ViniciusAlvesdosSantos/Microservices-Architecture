# Microservices com Spring Cloud e Spring Boot

Visão geral
-----------
Projeto de referência para aprender e praticar microservices com Java: Spring Boot 3 e JDK 21. O objetivo é guiar do zero até o deploy em containers Docker, cobrindo arquitetura, comunicação síncrona/assíncrona e infraestrutura (discovery, gateway, mensageria e auth).

O que este projeto cobre
1. Módulos Spring Cloud / Spring Boot
2. Arquitetura completa de microservices
3. Service Discovery
4. API Gateway
5. Balanceamento de carga
6. Comunicação síncrona (OpenFeign) e assíncrona (RabbitMQ)
7. Authorization Server (Keycloak)
8. Build e execução com Docker (imagens e containers)
9. Réplicas e escalabilidade básica

Tecnologias
1. Java 21 (JDK 21)
2. Spring Boot 3
3. Spring Cloud (Discovery, OpenFeign, Gateway)
4. RabbitMQ
5. Keycloak
6. Docker / Docker Compose
7. Maven

Pré-requisitos
1. Conhecimento em Java e orientação a objetos
2. Noções básicas de Spring Boot
3. Ferramentas instaladas: JDK 21, Maven, Docker, Docker Compose, (opcional) Keycloak
4. Noções de REST APIs e bancos de dados

Como executar (resumo)
1. Compilar com Maven:
    - `mvn clean package -DskipTests`
2. Construir imagens Docker (exemplo por módulo):
    - `docker build -t myservice:latest -f Dockerfile .`
3. Subir ambiente com Docker Compose (se houver `docker-compose.yml`):
    - `docker compose up -d`
4. Acessar serviços via API Gateway e configurar Keycloak conforme instruções do módulo `auth-server`.

Estrutura sugerida do repositório
1. `discovery-server` - Service Discovery (Eureka/Consul)
2. `api-gateway` - Gateway (Spring Cloud Gateway)
3. `auth-server` - Keycloak / Authorization
4. `service-<nome>` - Microservices (ex.: catalog, orders, customers)
5. `rabbitmq` - configuração / docker-compose para RabbitMQ
6. `docker` - scripts e Dockerfiles compartilhados

O que você aprenderá
1. Projetar e implementar arquitetura de microservices
2. Comunicação entre serviços (síncrona e assíncrona)
3. Configuração de mensageria com RabbitMQ
4. Autenticação/autorização com Keycloak
5. Criar imagens Docker e gerenciar containers

Contribuição
1. Abrir issues para bugs ou sugestões
2. Criar pull requests com descrições claras e testes quando aplicável

Licença
1. Verifique o arquivo `LICENSE` no repositório (ou adicione a licença desejada).

Notas finais
1. Todo o código e configurações utilizados nas aulas estão disponibilizados no repositório.
2. Consulte as anotações das aulas para links de download das ferramentas e versões utilizadas.
