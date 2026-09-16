# 🪰🧠 Mosca Cerebral Países

Plataforma web educativa e experimental inspirada em conectomas de **Drosophila** (mosca-da-fruta).

A primeira versão foi projetada para funcionar **sem backend**: sem Supabase, Firebase ou servidor próprio. A aplicação roda no navegador e pode ser hospedada como site estático no Cloudflare.

## O que já existe

- 🧠 **Explorar** — visualizador interativo de uma rede neural demonstrativa.
- ⚡ **Simulador** — aplique estímulos como luz, cheiro, toque e perigo e acompanhe a propagação.
- 🪰 **Vida** — uma mosca virtual procura alimento e evita ameaças em um mundo 2D.
- 🧪 **Laboratório** — ligue/desligue grupos neurais e compare respostas.
- 🧬 **Evolução** — simulação simples de populações com parâmetros herdáveis.
- 🧱 **Construtor** — monte pequenos circuitos de sensor → processamento → ação.
- 🎓 **Escola** — conteúdo curto e quiz.
- 💾 **Progresso local** — salvo no próprio navegador.
- 📱 **PWA** — pode ser instalada e funcionar offline depois do primeiro carregamento.

## Importante sobre os dados

O conjunto incluído em `data/flybrain-demo.json` é **demonstrativo/sintético**. Ele não deve ser apresentado como uma reprodução do conectoma científico completo da Drosophila. A arquitetura foi deixada preparada para, no futuro, receber subconjuntos de dados científicos devidamente processados e documentados.

## Tecnologias

- HTML5
- CSS3
- JavaScript moderno (ES Modules)
- Canvas 2D
- LocalStorage
- Service Worker / Web App Manifest

Não há dependências externas nem etapa de build.

## Rodar localmente

Por causa do Service Worker e do carregamento do JSON, use um servidor HTTP simples em vez de abrir o `index.html` diretamente.

Com Python:

```bash
python -m http.server 8080
```

Depois abra `http://localhost:8080`.

## Publicar no Cloudflare

No Cloudflare, conecte este repositório do GitHub e use uma publicação de site estático:

- **Framework preset:** None
- **Build command:** deixe vazio
- **Build output directory:** `/` (raiz do repositório)

Se a interface do Cloudflare exigir um diretório de saída, use um fluxo de Static Assets que publique a raiz do projeto, ou copie os arquivos para um diretório como `public/` antes do deploy.

## Estrutura

```text
/
├── index.html
├── styles.css
├── app.js
├── manifest.webmanifest
├── sw.js
├── icon.svg
└── data/
    └── flybrain-demo.json
```

## Próximas evoluções planejadas

- Importação de subconjuntos reais de conectoma, mantendo metadados e fonte.
- Visualização 3D.
- Web Workers para simulações maiores.
- WebGPU opcional para cálculos paralelos.
- Exportar/importar experimentos em arquivo.
- Multiplayer local sem conta.
- Backend opcional no futuro para ranking, sincronização e multiplayer online.

## Licença

Código do projeto: MIT. Dados científicos adicionados futuramente podem ter licenças próprias e deverão ser documentados separadamente.
