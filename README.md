# Desafio: Modelo de Domínio e ORM - Sistema de Eventos

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![H2 Database](https://img.shields.io/badge/H2_Database-003B57?style=for-the-badge&logo=h2&logoColor=white)

## sobre o projeto

Este projeto é a resolução de um desafio de **Modelagem de Domínio e ORM** (Object-Relational Mapping). O objetivo foi criar uma API Rest utilizando **Java e Spring Boot** para gerenciar as informações de um evento acadêmico, focando na estruturação correta das entidades e seus relacionamentos no banco de dados.

O sistema gerencia:
- **Atividades**: Palestras, cursos, oficinas (com nome, descrição e preço).
- **Blocos de Horário**: Dias e horários em que as atividades ocorrem.
- **Participantes**: Pessoas cadastradas no evento.

O projeto inclui o **Seeding** (povoamento) básico do banco de dados para testes imediatos.

## 📂 Modelo Conceitual

O domínio da aplicação foi modelado respeitando as seguintes regras de negócio:
1. Uma **Atividade** pode ter um ou mais **Blocos** de horário.
2. Um **Participante** pode se inscrever em várias **Atividades**.
3. Uma **Atividade** pode ter vários **Participantes**.

Isso resultou nos seguintes relacionamentos principais:
- **Atividade -> Bloco**: *Um para Muitos (1..N)*
- **Atividade <-> Participante**: *Muitos para Muitos (N..N)*, gerando a tabela de associação `tb_participante_atividade`.

## 🛠 Tecnologias Utilizadas

- **Java 17+**
- **Spring Boot**
- **Spring Data JPA** (Hibernate)
- **H2 Database** (Banco de dados em memória)
- **Maven**

## 🚀 Como executar o projeto

### Pré-requisitos
- Java 17 ou superior instalado.

### Passo a passo
1. Clone o repositório:
```bash
git clone https://github.com/Wsalvarengadev/desafio_ORM
