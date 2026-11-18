# 🧩 Microservices Node.js — gRPC, REST & GraphQL

> Architecture microservices avec deux services (**Films** et **Séries TV**) qui communiquent en **gRPC**, exposés par une **API Gateway** qui propose à la fois **REST** et **GraphQL**.

![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-244c5a?logo=google&logoColor=white)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?logo=graphql&logoColor=white)
![Apollo](https://img.shields.io/badge/Apollo%20Server-311C87?logo=apollographql&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?logo=express&logoColor=white)

## 🏗️ Architecture

```
            Client (REST ou GraphQL)
                     │
              ┌──────▼──────┐
              │ API Gateway │  Express (REST) + Apollo Server (GraphQL)
              └──┬───────┬──┘
           gRPC  │       │  gRPC
      ┌──────────▼─┐   ┌─▼──────────────┐
      │ Movie      │   │ TV Show        │
      │ service    │   │ service        │
      └────────────┘   └────────────────┘
```

| Fichier | Rôle |
|---|---|
| `movie.proto`, `tvShow.proto` | Contrats gRPC (Protocol Buffers) |
| `movieMicroservice.js`, `tvShowMicroservice.js` | Serveurs gRPC |
| `apiGateway.js` | Point d'entrée unique : routes REST + endpoint GraphQL |
| `schema.gql`, `resolvers.js` | Schéma et résolveurs GraphQL |

## 🚀 Lancer le projet

```bash
npm install
node movieMicroservice.js
node tvShowMicroservice.js
node apiGateway.js
```

## 📚 Ce que j'ai appris

- Définir des contrats de service avec Protocol Buffers
- Faire communiquer des services en gRPC
- Exposer la même donnée en REST et en GraphQL derrière une API Gateway

---

👩‍💻 **Mayssa Dhahri** — Élève-ingénieure en Génie Logiciel · [LinkedIn](https://www.linkedin.com/in/mayssa-dhahri)
