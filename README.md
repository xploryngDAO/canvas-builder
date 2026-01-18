# Canvas App Creator

> Full-stack application for creating canvas-based apps with React frontend and Express backend

## 🚀 Quick Start

### Prerequisites

- **Node.js 18+** (recomendado: Node.js 22.17.0 ou superior)
- **pnpm** (será instalado automaticamente se não estiver disponível)

### Instalação e Execução

```bash
# Opção 1: Usando pnpm (recomendado)
pnpm run dev:full

# Opção 2: Usando npm (instala pnpm automaticamente)
npm run dev:full

# Opção 3: Usando npx se pnpm não estiver no PATH
npx pnpm run dev:full
```

**URLs de Acesso:**
- **Frontend**: http://localhost:3010
- **Backend**: http://localhost:8010

## 📁 Project Structure

```
canvas-app-creator/
├── frontend/          # React + TypeScript + Vite + TailwindCSS
│   ├── src/
│   │   ├── components/    # Reusable UI components
│   │   ├── pages/         # Application pages
│   │   ├── contexts/      # React contexts
│   │   ├── hooks/         # Custom React hooks
│   │   ├── services/      # API services
│   │   └── constants/     # Application constants
│   └── package.json
├── backend/           # Express + TypeScript + SQLite
│   ├── src/
│   │   ├── controllers/   # Route controllers
│   │   ├── services/      # Business logic
│   │   ├── repositories/  # Data access layer
│   │   ├── routes/        # API routes
│   │   ├── middleware/    # Express middleware
│   │   ├── database/      # Database configuration
│   │   └── types/         # TypeScript types
│   └── package.json
├── shared/            # Shared types and utilities
└── package.json       # Root package.json with scripts
```

## 🛠️ Development

### Prerequisites

- **Node.js 18+** (testado com Node.js 22.17.0)
- **pnpm** (recomendado) - será instalado automaticamente via npm se não estiver disponível

### Instalação do pnpm (se necessário)

```bash
# Instalar pnpm globalmente
npm install -g pnpm

# Verificar instalação
pnpm --version
```

### Available Scripts

**Scripts Principais:**
- `pnpm run dev:full` - Instala dependências e inicia frontend e backend com auto-restart
- `npm run dev:full` - Alternativa usando npm (instala pnpm automaticamente)
- `npx pnpm run dev:full` - Usando npx se pnpm não estiver no PATH
- `npm run dev:npm` - Versão que usa apenas npm (sem pnpm)

**Scripts Individuais:**
- `pnpm run dev:frontend` - Inicia apenas o servidor de desenvolvimento do frontend
- `pnpm run dev:backend` - Inicia apenas o servidor de desenvolvimento do backend
- `pnpm run install-deps` - Instala todas as dependências dos workspaces
- `pnpm run build` - Build de produção para frontend e backend
- `pnpm run start` - Inicia o servidor de produção

### Individual Development

**Frontend only:**
```bash
cd frontend
pnpm install
pnpm dev
```

**Backend only:**
```bash
cd backend
pnpm install
pnpm dev
```

## 🎨 Features

### Frontend
- ⚡ **Vite** - Fast build tool and dev server
- ⚛️ **React 18** - Modern React with hooks
- 🎨 **TailwindCSS** - Utility-first CSS framework
- 📱 **Responsive Design** - Mobile-first approach
- 🧩 **Component Library** - Reusable UI components
- 🎯 **TypeScript** - Type safety and better DX

### Backend
- 🚀 **Express.js** - Fast, unopinionated web framework
- 📊 **SQLite** - Lightweight database
- 🔒 **CORS** - Cross-origin resource sharing
- 📁 **File Upload** - Multer integration
- 🎯 **TypeScript** - Type safety
- 🔄 **Auto-restart** - Development with tsx watch

### Application Features
- 🎨 **Canvas Creation Wizard** - Step-by-step app creation
- ⚙️ **Project Settings** - Customizable default configurations
- 🎭 **Multiple Themes** - Light/Dark mode support
- 📱 **Responsive Layout** - Works on all devices
- 🔧 **Integration Support** - API and MCP server integrations
- 💾 **Local Storage** - Persistent user preferences

## 🏗️ Architecture

### Frontend Architecture
- **Component-based** - Modular and reusable components
- **Context API** - State management for global data
- **Custom Hooks** - Reusable logic extraction
- **Service Layer** - API communication abstraction

## 🧭 Fluxo de Navegação

- `Home` (`/`) - Página inicial com acesso rápido ao fluxo de criação.
- `Projects` (`/projects`) - Lista e gerenciamento de projetos e versões.
- `Create App` (`/create` ou `/create-app`) - Wizard completo de criação e configuração.
- `Compilation` (`/compilation`) - Consolida geração de código e feedback do terminal.
- `IDE` (`/ide` e `/ide/:projectId/:versionId`) - Edição, visualização e gerenciamento de arquivos gerados.
- `Settings` (`/settings`) - Preferências e integrações (IA, APIs, etc.).

## 📄 Páginas

- `HomePage` - Introdução e CTA para iniciar o wizard.
- `ProjectsPage` - Lista de projetos, versões, abertura no IDE, exclusão e duplicação.
- `CreateAppPage` - Wizard interativo com IA e validações contextuais.
- `CompilationPage` - Terminal de build e logs de geração.
- `IDEPage` - Ambiente de desenvolvimento com abas (preview, editor, etc.).
- `SettingsPage` - Configurações globais de projeto e serviços.

## 🧙 Wizard de Criação

O wizard organiza a criação em etapas claras com IA auxiliar e validações:

- Etapa 1: `Informações Básicas` — nome e descrição do app.
- Etapa 2: `Aprimoramento de Descrição` — IA melhora a descrição e sugere ajustes.
- Etapa 3: `Escolha de Configuração` — padrão, personalizar ou IA criativa.
- Etapa 4: `Tipo de Aplicação` — ex.: `web-spa`, `pwa`, `ecommerce`, `dashboard`.
- Etapa 5: `Stack Frontend + Framework CSS` — escolha de `react`, `vue`, `nextjs` e `tailwind`, `bootstrap`, etc.
- Etapa 6: `Tema de Cores + Fonte` — seleção de temas e tipografia.
- Etapa 7: `Estilo de Layout` — `modern`, `minimal`, `material`, `flat`, etc.
- Etapa 8: `Navegação` — estrutura de navegação e padrões de UX.
- Etapa 9: `Estrutura de Menu` — header/footer, sidebar, hamburger, dashboard.
- Etapa 10: `Funcionalidades` — ativar `autenticação`, `banco de dados`, `pagamentos`.
- Etapa 11: `Integrações` — mapeamento de integrações conforme contexto e descrição.
- Etapa 12: `Mapeamento de Recursos` — IA organiza páginas, recursos, fluxos e menus.
- Etapa 13: `Geração de Banco de Dados` — criação/visualização de schema e entidades.
- Etapa 14: `Revisão das Configurações` — resumo e aprovação final.

### Validações e Restrições

- Sistema de restrições do wizard alinha escolhas com a categoria de aplicação.
- Regras de combinação para `frontend`, `css`, `layout`, `menu`, `navigation`, `themes`.
- Métricas por tipo (ex.: limite de bundle, metas de performance e Lighthouse).

### IA e Aprovações

- `Aprimoramento de Descrição` e `Prompt Enhance` refinam pedidos para geração robusta.
- `App Mapping` cria estrutura aprovada: páginas, recursos, fluxos, navegação e elementos.
- Seções de aprovação auxiliam validação e ajuste antes da compilação.

## 🧰 IDE e Abas

A IDE centraliza edição, preview e gestão de artefatos gerados com múltiplas abas:

- `Preview` — visualização responsiva (desktop/tablet/mobile), zoom e modo de inspeção.
- `Canvas` — fluxo visual do canvas e composição de elementos.
- `Files` — árvore de arquivos gerados com seleção e edição.
- `Editor` — Monaco Editor com recursos avançados (minimap, folding, formatação, atalhos).
- `Agentes` — agentes de código (geração, refatoração, debug e teste).
- `Dados` — visão de dados, schema e entidades (quando habilitado).
- `Memoria` — contexto de trabalho e histórico para auxiliar a IA.
- `Integrações` — gerenciamento de integrações de serviços.
- `Notas` — notas e documentação auxiliar do projeto.
- `Documentacao` — referência e artefatos gerados de documentação.
- `Tarefas` — acompanhamento de atividades e roadmap.
- `Dashboard` — visão geral de status do projeto.
- `Roadmap` — planejamento e marcos.
- `Diagramas` — diagramas técnicos e de fluxo.

### Funcionalidades de Destaque na IDE

- Inspeção de elementos no `Preview` com overlay e captura de metadados.
- Edição com Monaco carregado sob demanda (`lazy`) para performance.
- Atualização automática de arquivos e salvamento em banco local (SQLite).
- Download de projeto gerado em ZIP com README.


### Backend Architecture
- **Layered Architecture** - Controllers, Services, Repositories
- **Database Layer** - SQLite with better-sqlite3
- **Middleware** - CORS, file upload, error handling
- **Type Safety** - Shared types between frontend and backend

## 🔧 Configuration

### Environment Variables

**Backend (.env):**
```env
PORT=8010
NODE_ENV=development
DATABASE_PATH=./database.db
```

### Port Configuration
- Frontend: **3010** (configured in vite.config.ts)
- Backend: **8010** (configured in .env and index.ts)

## 📦 Dependencies

### Frontend
- React 18 + React DOM
- React Router DOM
- TailwindCSS + PostCSS
- Lucide React (icons)
- Zustand (state management)
- Vite + TypeScript

### Backend
- Express.js
- better-sqlite3
- CORS + Multer
- dotenv + uuid
- TypeScript + tsx

## 🚀 Deployment

### Build for Production

```bash
# Opção 1: Scripts raiz (recomendado)
npm run build:npm   # build frontend + backend
npm run start:npm   # inicia backend em produção

# Opção 2: Workspaces (pnpm)
cd frontend && pnpm build
cd ../backend && pnpm build
cd ../backend && pnpm start
```

### Docker Support (Coming Soon)
- Multi-stage Docker build
- Production-ready containers
- Docker Compose for full stack

## 🔧 Troubleshooting

### Problema: "pnpm não é reconhecido como comando"

**Solução 1:** Instalar pnpm globalmente
```bash
npm install -g pnpm
```

**Solução 2:** Usar npx para executar pnpm
```bash
npx pnpm run dev:full
```

**Solução 3:** Usar npm diretamente
```bash
npm run dev:full
```

### Problema: Portas já em uso

Se as portas 3010 ou 8010 estiverem em uso:

**Frontend (porta 3010):**
- O Vite automaticamente tentará a próxima porta disponível (3011, 3012, etc.)

**Backend (porta 8010):**
- Modifique o arquivo `backend/.env` ou `backend/src/index.ts`
- Altere a variável `PORT` para uma porta diferente

### Problema: Dependências não instaladas

```bash
# Limpar cache e reinstalar
pnpm store prune
pnpm install

# Ou usando npm
npm cache clean --force
npm run install-deps
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- React team for the amazing framework
- Vite team for the blazing fast build tool
- TailwindCSS for the utility-first CSS framework
- Express.js community for the robust backend framework

---

Made with ❤️ by [xploryngDAO](https://github.com/xploryngDAO)
## ⚡ Performance e Build

- Code splitting configurado em `frontend/vite.config.ts` via `manualChunks` (separa `react`, `monaco`, `icons`, `sql`, etc.).
- Monaco Editor é carregado sob demanda com `React.lazy`/`Suspense` nas abas de Editor.
- Bundle inicial reduzido e chunks gerados: `react`, `monaco`, `icons`, `sql` em arquivos separados.
- Ajuste de `chunkSizeWarningLimit` para 2000 no build, reduzindo avisos de tamanho.

### Verificações

```bash
# Frontend
cd frontend
npm run check  # typecheck (tsc --noEmit)
npm run lint   # lint (pode exigir correções manuais)
```
