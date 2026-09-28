
## Project structure

`Visualização de trocas/`: Diagrama UML e Documentação de casos de uso

`app/`: aplicação web (React + TypeScript, feito usando Vite)

| Path | Purpose |
|---|---|
| `index.html` | Página HTML que o app React carrega|
| `public/` | Arquivos estáticos (não-importados) |
| `src/main.tsx` | Onde o app começa; renderiza `App` em `index.html` |
| `src/App.tsx` | Componente root; faz o setup das páginas |
| `src/index.css` | Estilos .css globais |
| `src/models/` | Tipos TypeScript para cada classe no UML, um arquivo por classe: Jogador, Troca, Carta, Notificacao |
| `src/services/` | Lógica das fucionalidades (criarTroca, consultarDisponibilidade... -> trocaService.ts, criarCadastro, efetuarLogin... -> jogadorService.ts...), um arquivo classeService.ts por classe |
| `src/pages/` | Páginas (login, trocas, histórico, etc.) |
| `src/components/` | UI reutilizável (card, notificação...), um arquivo de componente PascalCase.tsx, exemplos: CartaCard.tsx (com nome, tipo, se está disponível...), NotificaçãoItem.tsx (uma notificação genérica)...; Páginas são compostas por componentes, e componentes não possuem lógica, são apenas UI |
| `src/hooks/` | Lógica React compartilhada |
| `src/assets/` | Imagens e ícones importados pelo código |
| `package.json` | Dependências e scripts (`npm run dev`, `npm run build`) |
| `tsconfig*.json` | Configurações do TypeScript |
| `vite.config.ts` | Configurações do Vite (dev server/build) |
| `.oxlintrc.json` | Configurações do Linter (code checker) |

## Como rodar

    cd app
    npm install
    npm run dev

Abrir http://localhost:5173 no browser de escolha