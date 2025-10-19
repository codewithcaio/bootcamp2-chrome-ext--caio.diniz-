Tab Closer — Extensão para Google Chrome (Manifest V3)
Tab Closer é uma extensão para Google Chrome que fecha todas as abas, exceto a aba ativa, ideal para quem costuma trabalhar com várias abas abertas e deseja limpar rapidamente a janela do navegador.

Funcionalidades
Fecha todas as abas abertas, exceto a que está ativa.

Interface simples e intuitiva no popup.

Visual moderno e responsivo.

Comunicação eficiente entre popup e background (service worker).

Containerização e Testes Automatizados
Com esta entrega, a extensão pode ser empacotada em container Docker e testada automaticamente usando Playwright e integração contínua no GitHub Actions.

Como rodar localmente com Docker
Construa a imagem:

text
docker compose build
Execute os testes end-to-end:

text
docker compose run --rm e2e
(Opcional) Veja o relatório HTML dos testes:

text
npx playwright show-report
Integração Contínua (GitHub Actions)
Instala as dependências e Playwright.

Realiza o build e empacota a extensão.

Executa os testes E2E Playwright.

Publica o relatório HTML dos testes e o .zip final da extensão como artefato.

Veja os resultados diretamente na aba "Actions" do GitHub.

Instalação Manual (modo desenvolvedor)
Baixe ou clone este repositório:

text
git clone https://github.com/codewithcaio/bootcamp2-chrome-ext--caio.diniz-.git
Abra o Google Chrome e acesse:

text
chrome://extensions/
Ative o Modo desenvolvedor no canto superior direito.

Clique em Carregar sem compactação (Load unpacked).

Selecione a pasta raiz do projeto.

O ícone da extensão aparecerá na barra do navegador.

Instalação via arquivo ZIP
Baixe o arquivo .zip na página de Releases.

Extraia o .zip em uma pasta.

No Chrome acesse chrome://extensions/ e ative o modo desenvolvedor.

Clique em Carregar sem compactação e escolha a pasta extraída.

Como usar
Clique no ícone da extensão Tab Closer no Chrome.

No popup, clique em Fechar abas.

Todas as abas, exceto a atual, serão fechadas!

Uma mensagem exibirá quantas abas foram fechadas.

Estrutura do projeto
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
Tecnologias e APIs utilizadas
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

Página do Projeto
https://codewithcaio.github.io/bootcamp2-chrome-ext--caio.diniz-/

Boa codificação!
