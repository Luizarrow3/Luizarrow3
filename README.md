# OLÁ SOU O (LUIZ DEV👋)
 



# título:
   "ESTOU EM MEU PROCESSO DE ESTUDO HTML,CSS,FRONT-END".
 for deploying static content to GitHub Pages
name: Deploy static content to Pages
   "ESTOU EM MEU PROCESSO DE ESTUDO HTML,CSS,FRONT-END".
para implantar conteúdo estático nas páginas do GitHub
nome: Implantar conteúdo estático nas páginas

eco "# Luizahhor" >> README.md
iniciar git
git adicionar README.md
git commit -m "primeiro commit"
git branch -M principal
git remoto adicionar origem https://github.com/Luizarrow3/Luizahhor.git
git push -u origem principal
  # Executa em pushes direcionados ao branch padrão
  empurrar:
    ramos: [ "principal" ]

  # Permite que você execute este fluxo de trabalho manualmente na guia Ações
  fluxo de trabalho_despacho:

# Define permissões do GITHUB_TOKEN para permitir a implantação no GitHub Pages
permissões:
  conteúdo: ler
  páginas: escrever
  id-token: escrever

# Permitir apenas uma implantação simultânea, ignorando as execuções enfileiradas entre a execução em andamento e a mais recente na fila.
# No entanto, NÃO cancele execuções em andamento, pois queremos permitir que essas implantações de produção sejam concluídas.
simultaneidade:
  grupo: "páginas"
  cancelamento em andamento: falso

empregos:
  # Tarefa de implantação única, pois estamos apenas implantando
  implantar:
    ambiente:
      nome: github-pages
      URL: ${{ etapas.implantação.saídas.página_url }}
    em execução: ubuntu-latest
    passos:
      - nome: Checkout
        usos: ações/checkout@v4
      - nome: Configurar páginas
        usos: ações/configure-pages@v5
      - nome: Carregar artefato
        usos: ações/upload-pages-artifact@v3
        com:
          # Carregar repositório inteiro
          caminho: '.'
      - nome: Implantar nas páginas do GitHub
        id: implantação
        usos: ações/páginas-de-implantação@v4


echo "# Luizahhor" >> README.md 
git init 
git add README.md 
git commit -m "primeiro commit" 
git branch -M main 
git remote add origin https://github.com/Luizarrow3/Luizahhor.git
 git push -u origin main
  # Runs on pushes targeting the default branch
  push:
    branches: ["main"]

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

# Sets permissions of the GITHUB_TOKEN to allow deployment to GitHub Pages
permissions:
  contents: read
  pages: write
  id-token: write

# Allow only one concurrent deployment, skipping runs queued between the run in-progress and latest queued.
# However, do NOT cancel in-progress runs as we want to allow these production deployments to complete.
concurrency:
  group: "pages"
  cancel-in-progress: false

jobs:
  # Single deploy job since we're just deploying
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Setup Pages
        uses: actions/configure-pages@v5
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          # Upload entire repository
          path: '.'
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
  

