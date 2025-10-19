Tab Closer — Extensão para Google Chrome (Manifest V3)
Tab Closer é uma extensão para Google Chrome que fecha todas as abas, exceto a aba ativa, ideal para quem costuma trabalhar com várias abas abertas e deseja limpar rapidamente a janela do navegador.

Funcionalidades
Fecha todas as abas abertas, exceto a que está ativa.

Interface simples e intuitiva no popup.

Visual moderno e responsivo.

Comunicação eficiente entre popup e background (service worker).

Containerização & Testes Automatizados
Esta entrega inclui empacotamento da extensão, testes automáticos E2E com Playwright usando Docker e integração contínua via GitHub Actions.

Instalação Manual (modo desenvolvedor)
Baixe ou clone este repositório na sua máquina:

text
git clone https://github.com/codewithcaio/bootcamp2-chrome-ext--caio.diniz-.git
Abra o Google Chrome e acesse:

text
chrome://extensions/
Ative o Modo desenvolvedor no canto superior direito.

Clique em Carregar sem compactação (Load unpacked).

Selecione a pasta raiz do projeto onde o código está.

O ícone da extensão aparecerá na barra de ferramentas do navegador.

Instalação via arquivo ZIP
Baixe o arquivo mais recente da extensão na página de Releases.

Extraia o arquivo .zip em uma pasta da sua máquina.

No Chrome, acesse chrome://extensions/ e ative o modo desenvolvedor.

Clique em Carregar sem compactação e selecione a pasta extraída.

O ícone da extensão aparecerá na barra do navegador.

Como usar
Clique no ícone da extensão Tab Closer na barra de ferramentas do Chrome.

Na janela popup que abrir, clique no botão Fechar abas.

Todas as abas, exceto a atual, serão fechadas instantaneamente.

Uma mensagem exibirá quantas abas foram fechadas.

Como Rodar Testes E2E com Docker
Construa a imagem do container:

text
docker compose build
Execute os testes end-to-end dentro do container:

text
docker compose run --rm e2e
(Opcional) Visualize o relatório HTML dos testes Playwright:

text
npx playwright show-report
Integração Contínua (GitHub Actions)
O workflow automatiza:

Instalação de dependências.

Build da extensão (dist/extension.zip).

Execução dos testes E2E Playwright.

Publicação do relatório e do pacote .zip como artefatos.

Veja resultados na aba Actions do projeto.

Estrutura do Projeto
text
my-chrome-extension/
├─ src/
│  ├─ popup/
│  ├─ content/
│  └─ background/
├─ icons/
├─ tests/
│  ├─ extension.spec.ts
│  └─ playwright.config.ts
├─ dist/
├─ Dockerfile
├─ docker-compose.yml
├─ package.json
├─ scripts/
│  └─ build-extension.mjs
├─ .github/
│  └─ workflows/
│     └─ ci.yml
├─ manifest.json
└─ README.md
Tecnologias e APIs Utilizadas
Google Chrome Extensions (Manifest V3)

HTML, CSS, JavaScript

API Chrome Tabs

Playwright (E2E)

Docker & Docker Compose

GitHub Actions

Licença
Este projeto está licenciado sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

Autor
Caio Diniz
GitHub | LinkedIn

Página do Projeto (GitHub Pages)
A landing page da extensão está disponível em:
https://codewithcaio.github.io/bootcamp2-chrome-ext--caio.diniz-/

Boa codificação!
