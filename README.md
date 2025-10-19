
# Tab Closer — Extensão para Google Chrome (Manifest V3)

Tab Closer é uma extensão para Google Chrome que fecha todas as abas, exceto a aba ativa, ideal para quem costuma trabalhar com várias abas abertas e deseja limpar rapidamente a janela do navegador.

***

## Funcionalidades

- Fecha todas as abas abertas, exceto a que está ativa.
- Interface simples e intuitiva no popup.
- Visual moderno e responsivo.
- Comunicação eficiente entre popup e background (service worker).

***

## Instalação Manual (modo desenvolvedor)

1. Baixe ou clone este repositório na sua máquina:
   ```
   git clone https://github.com/codewithcaio/bootcamp2-chrome-ext--caio.diniz-.git
   ```
2. Abra o Google Chrome e acesse:
   ```
   chrome://extensions/
   ```
3. Ative o **Modo desenvolvedor** no canto superior direito.
4. Clique em **Carregar sem compactação** (Load unpacked).
5. Selecione a pasta raiz do projeto onde o código está.
6. O ícone da extensão aparecerá na barra de ferramentas do navegador.

***

## Instalação via arquivo ZIP

1. Baixe o arquivo `.zip` mais recente na [página de Releases](https://github.com/codewithcaio/bootcamp2-chrome-ext--caio.diniz-/releases).
2. Extraia o `.zip` em uma pasta da sua máquina.
3. No Chrome, acesse `chrome://extensions/` e ative o modo desenvolvedor.
4. Clique em **Carregar sem compactação** e selecione a pasta extraída.

***

## Como usar

- Clique no ícone da extensão Tab Closer na barra do Chrome.
- Na janela popup, clique no botão **Fechar abas**.
- Todas as abas, exceto a atual, serão fechadas!
- Uma mensagem exibirá quantas abas foram fechadas.

***

## Como rodar localmente com NPM

1. Instale as dependências:
   ```
   npm install
   ```
2. Gere o build da extensão:
   ```
   npm run build
   ```
3. Execute os testes end-to-end com Playwright:
   ```
   npm run test:e2e
   ```
4. (Opcional) Veja o relatório HTML dos testes:
   ```
   npx playwright show-report
   ```

***

## Containerização e Testes Automatizados (Opcional)

Se desejar rodar tudo dentro de container Docker:

1. Construa a imagem:
   ```
   docker compose build
   ```
2. Execute os testes end-to-end:
   ```
   docker compose run --rm e2e
   ```

***

## Integração Contínua (GitHub Actions)

- Instala dependências e Playwright.
- Realiza o build e empacota a extensão.
- Executa os testes E2E Playwright.
- Publica o relatório HTML dos testes e o arquivo .zip final da extensão como artefato.

Veja os resultados na aba “Actions” do projeto.

***

## Estrutura do Projeto

```
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
```

***

## Tecnologias e APIs utilizadas

- Google Chrome Extensions (Manifest V3)
- HTML, CSS, JavaScript
- API Chrome Tabs
- Playwright (E2E)
- Docker & Docker Compose
- GitHub Actions

***

## Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

***

## Autor

Caio Diniz  
[GitHub](https://github.com/codewithcaio) | [LinkedIn](https://www.linkedin.com/in/codewithcaio)

***

## Página do Projeto

https://codewithcaio.github.io/bootcamp2-chrome-ext--caio.diniz-/

***

*Boa codificação!*

[4](https://github.com/simov/markdown-viewer)
[5](https://stackoverflow.com/questions/5922882/what-file-uses-md-extension-and-how-should-i-edit-them)
[6](https://developer.chrome.com/docs/extensions/samples)
[7](https://www.reddit.com/r/Markdown/comments/1ksk0d9/webpage_to_markdown_chrome_extension/)
[8](https://code.visualstudio.com/docs/languages/markdown)
[9](https://cloud.google.com/shell/docs/cloud-shell-tutorials/markdown-extensions)
