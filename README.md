# Challenge FórumHub - Alura

Este é o desafio final do módulo de **Especialização em Java** da Alura. O projeto consiste em uma **API REST** para um fórum de discussões, desenvolvida com Spring Boot, utilizando autenticação via **JWT (JSON Web Token)** e persistência de dados com MySQL.

---

## Tecnologias Utilizadas

* **Java 21**
* **Spring Boot 3.3.0**
* **Spring Security** (Autenticação e Autorização)
* **JWT** (Auth0)
* **Spring Data JPA**
* **Flyway** (Migrações de Banco de Dados)
* **MySQL** (Banco de dados relacional)
* **Lombok** (Produtividade no código)
* **Maven** (Gerenciamento de dependências)

---

## Funcionalidades (CRUD)

A API permite realizar as seguintes operações nos tópicos do fórum:

* **Listagem de Tópicos:** Retorna uma lista paginada e ordenada por data de criação.
* **Detalhamento:** Busca um tópico específico pelo seu ID.
* **Cadastro:** Criação de novos tópicos (protegido por token).
* **Atualização:** Edição de título e mensagem de um tópico existente (protegido por token).
* **Exclusão:** Remoção de tópicos do banco de dados (protegido por token).

---

## Segurança e Autenticação

O sistema utiliza segurança **Stateless**. Para acessar os endpoints de criação, edição e exclusão, é necessário:

1. Realizar login no endpoint `/login`.
2. Obter o **Token JWT**.
3. Enviar o token no cabeçalho das próximas requisições:
* **Key:** `Authorization`
* **Value:** `Bearer <seu_token_aqui>`
