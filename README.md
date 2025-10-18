Tab Closer — Extensão para Google Chrome (Manifest V3)

Tab Closer é uma extensão para Google Chrome que fecha todas as abas abertas, exceto a aba ativa. Ideal para quem costuma trabalhar com várias abas e quer limpar rapidamente a janela do navegador.

Funcionalidades

Fecha todas as abas abertas, exceto a que está ativa.

Interface simples e intuitiva no popup.

Visual moderno e responsivo.

Comunicação eficiente entre popup e background (service worker).

Instalação Manual (modo desenvolvedor)

Baixe ou clone este repositório:

git clone https://github.com/codewithcaio/bootcamp2-chrome-ext--caio.diniz-.git


Abra o Chrome e acesse:

chrome://extensions/


Ative o Modo desenvolvedor no canto superior direito.

Clique em Carregar sem compactação (Load unpacked) e selecione a pasta raiz do projeto.

O ícone da extensão aparecerá na barra de ferramentas.

Instalação via arquivo ZIP

Baixe o arquivo mais recente na página de Releases
.

Extraia o .zip em uma pasta da sua máquina.

No Chrome, acesse chrome://extensions/ e ative o modo desenvolvedor.

Clique em Carregar sem compactação e selecione a pasta extraída.

O ícone da extensão aparecerá na barra do navegador.

Como usar

Clique no ícone Tab Closer na barra de ferramentas do Chrome.

No popup, clique no botão Fechar abas.

Todas as abas, exceto a atual, serão fechadas instantaneamente.

Uma mensagem exibirá quantas abas foram fechadas.

Estrutura do projeto
my-chrome-extension/
├─ src/
│  ├─ popup/
│  │  ├─ popup.html
│  │  ├─ popup.js
│  │  └─ popup.css
│  ├─ background/
│  │  └─ service-worker.js
├─ icons/
│  ├─ icon16.png
│  ├─ icon32.png
│  ├─ icon48.png
│  └─ icon128.png
├─ docs/
│  └─ index.html
├─ dist/                 # Build da extensão
├─ tests/
│  └─ extension.spec.ts  # Teste E2E Playwright
├─ scripts/
│  └─ build-extension.mjs
├─ manifest.json
├─ package.json
├─ README.md
├─ LICENSE

Tecnologias e APIs utilizadas

Google Chrome Extensions (Manifest V3)

HTML, CSS e JavaScript (popup e background scripts)

API Chrome Tabs para gerenciamento de abas

Playwright para testes E2E

Docker + Docker Compose para containerização e testes replicáveis

GitHub Actions para CI/CD

Testes Automatizados (E2E)

O teste automatizado verifica a funcionalidade de fechar abas via popup. Ele:

Abre múltiplas abas normais (example.com/1, /2, /3)

Detecta o ID da extensão no contexto do Chromium

Abre o popup e clica no botão #close-tabs

Verifica que apenas a aba do popup permanece aberta

Rodando localmente
npm install
npm run build
npx playwright test tests/extension.spec.ts
npx playwright show-report   # opcional, para abrir relatório HTML


Localmente, o teste roda visível; em CI, roda headless.

Rodando via CI / GitHub Actions

Workflow configurado em .github/workflows/ci.yml

Executa build, testes E2E e publica artefatos:

dist/extension.zip

playwright-report (HTML)

Critérios de sucesso dos testes

Apenas a aba do popup permanece aberta após o clique.

URLs restantes logadas no console:

URLs restantes depois do clique: [ 'chrome-extension://<extensionId>/src/popup/popup.html' ]


Teste executa sem erros, tanto local quanto no CI.

Licença

MIT License — veja o arquivo LICENSE para detalhes.

Autor

Caio Diniz
GitHub
 | LinkedIn

Página do projeto (GitHub Pages)

https://codewithcaio.github.io/bootcamp2-chrome-ext--caio.diniz-/

Boa codificação!
