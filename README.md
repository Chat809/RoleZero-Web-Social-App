# Role0 — Frontend Web

> Aplicação web do **Role0**: facilitador de experiências coletivas. Conecta pessoas por interesses comuns para ocupar vagas em mesas e grupos, reduzindo o custo social e a ansiedade de frequentar lugares sozinho.

[![Next.js](https://img.shields.io/badge/Next.js-15-black?logo=next.js)](https://nextjs.org/)
[![Chakra UI](https://img.shields.io/badge/Chakra%20UI-2.x-319795?logo=chakra-ui)](https://chakra-ui.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?logo=typescript)](https://www.typescriptlang.org/)

---

## Índice

- [Sobre o projeto](#sobre-o-projeto)
- [Stack e requisitos](#stack-e-requisitos)
- [Começando](#começando)
- [Estrutura do projeto](#estrutura-do-projeto)
- [Identidade visual](#identidade-visual)
- [API e integrações](#api-e-integrações)
- [Requisitos acadêmicos](#requisitos-acadêmicos)
- [Licença](#licença)

---

## Sobre o projeto

O **Role0** não é um app de namoro. É um **facilitador de experiências coletivas**:

- **Problema:** custo social e ansiedade de ir sozinho a bares, shows e eventos.
- **Solução:** ocupar vagas ociosas em mesas e grupos, unindo desconhecidos por interesses comuns.
- **Diferencial:** foco no **grupo** e na **segurança**, sem a pressão do match um-a-um.

Este repositório contém o **frontend web** (Next.js + Chakra UI + TypeScript), consumindo a API do Role0.

---

## Stack e requisitos

| Tecnologia | Uso |
|------------|-----|
| **Next.js** | Framework React (App Router) |
| **Chakra UI** | Componentes e design system (sem Tailwind) |
| **TypeScript** | Tipagem estática |
| **Ecossistema JavaScript** | npm/yarn, libs compatíveis com React 18+ |

- **Node.js** 18+ recomendado.
- Interface **responsiva** (mobile-first quando aplicável).

---

## Começando

### Pré-requisitos

- Node.js 18+
- npm ou yarn

### Instalação

```bash
git clone https://github.com/Chat809/RoleZero-Web-Social-App.git
cd RoleZero-Web-Social-App
npm install
```

### Variáveis de ambiente

Crie um arquivo `.env.local` na raiz:

```env
NEXT_PUBLIC_API_URL=https://rolezero-backend-core.onrender.com
# Outras variáveis conforme necessidade (ex.: Google Maps, auth)
```

### Desenvolvimento

```bash
npm run dev
```

Acesse [http://localhost:3000](http://localhost:3000).

### Build e produção

```bash
npm run build
npm start
```

---

## Estrutura do projeto

```
RoleZero-Web-Social-App/
├── src/
│   ├── app/           # App Router (Next.js 15)
│   ├── components/    # Componentes reutilizáveis
│   ├── lib/           # Utilitários, clientes API, hooks
│   ├── theme/         # Tema Chakra (Dark Mode Triad)
│   └── types/         # Tipos TypeScript
├── public/
├── .env.local.example
├── package.json
└── README.md
```

*(A estrutura pode ser ajustada conforme a evolução do projeto.)*

---

## Identidade visual (Dark Mode Triad)

A interface usa contraste vibrante sobre fundo escuro para reduzir fadiga ocular e transmitir modernidade.

| Cor | Hex | Uso |
|-----|-----|-----|
| **Fundo** | `#0B0B0F` | Background principal |
| **Roxo elétrico** | `#3800e0` | Marca, CTAs, navegação |
| **Laranja vibrante** | `#e03800` | Urgência, eventos ao vivo, vagas acabando |
| **Verde neon** | `#00e038` | Confiança, verificados, sucesso |

O tema Chakra deve ser configurado com essa paleta.

---

## API e integrações

- **API Role0 (backend):**  
  - Base: `https://rolezero-backend-core.onrender.com`  
  - Documentação: [Swagger UI](https://rolezero-backend-core.onrender.com/swagger-ui/index.html)  
  - Repositório: [rolezero-api](https://github.com/ewkekw/rolezero-api)

- **API pública (exigência da disciplina):** integração com pelo menos uma API pública (ex.: ViaCEP, OpenWeather, Google Maps/Places para endereços e mapa).

---

## Funcionalidades (MVP)

- **Mapa de calor social:** visualização de rolês próximos com pins por categoria.
- **Sistema Host/Guest:** criação de evento, vagas e aprovação de participantes.
- **Card do rolê:** detalhes, capacidade, “Quero me juntar”.
- **Login/Autenticação:** tela de login funcional (token/session).
- **Chat de grupo:** (fase posterior) chat efêmero por evento.

---

## Requisitos acadêmicos

Este projeto atende aos requisitos mínimos da disciplina **Programação Avançada para Web** (PjBL):

| Requisito | Atendimento |
|-----------|-------------|
| **Backend** | API REST com CRUD (backend em repositório separado) |
| **Frontend** | Interface responsiva (Next.js + Chakra UI) |
| **Integração** | Chamada a API pública (ex.: geolocalização, CEP, etc.) |
| **Segurança** | Tela de login com autenticação (token/session) |
| **Nuvem** | Deploy em Vercel ou similar; banco gerenciado em nuvem (backend) |

---

## Licença

Este projeto é de uso acadêmico e do time Role0. Consulte o repositório para termos de uso e contribuição.

---

**Role0** — Menos solidão, mais rolê.
