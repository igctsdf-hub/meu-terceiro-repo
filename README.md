# Configuração do Repositório: meu-terceiro-repo

Este projeto tem como objetivo demonstrar a criação de um repositório público no GitHub usando a GitHub CLI, sua clonagem local e a publicação de um README por meio de um commit inicial no branch principal `main`.

## Configuração

- **Repositório público:** https://github.com/igctsdf-hub/meu-terceiro-repo
- **Conta:** `igctsdf-hub`
- **Pasta local:** `C:\Users\Admin\Documents\Agente_Exercicios\agente-cria-pr\meu-terceiro-repo`
- **Branch principal:** `main`
- **Ferramentas:** Git, GitHub CLI (`gh`) e PowerShell.

## Comandos Git e CLI

Os comandos abaixo documentam a sequência de configuração. A autenticação e a criação foram executadas no diretório pai; os demais comandos Git foram executados na pasta clonada.

1. **Verificar a autenticação no GitHub**

   ```powershell
   gh auth status
   ```

   Confere a conta autenticada, o protocolo Git e as permissões disponíveis na GitHub CLI.

2. **Criar e clonar o repositório público**

   ```powershell
   gh repo create igctsdf-hub/meu-terceiro-repo --public --clone
   ```

   Cria o repositório público na conta indicada e o clona na subpasta `meu-terceiro-repo` do diretório atual, configurando o remoto `origin`.

3. **Definir o nome do branch principal**

   ```powershell
   git branch -M main
   ```

   Define o nome do branch local como `main`.

4. **Adicionar a documentação à área de preparação**

   ```powershell
   git add README.md
   ```

   Prepara o README para inclusão no primeiro commit.

5. **Criar o commit inicial**

   ```powershell
   git commit -m "docs: documenta configuração inicial do repositório"
   ```

   Registra a documentação no histórico Git com uma mensagem descritiva.

6. **Enviar o branch principal ao GitHub**

   ```powershell
   git push -u origin main
   ```

   Publica o commit no branch `main` do remoto `origin` e configura seu acompanhamento para os próximos envios e atualizações.

7. **Verificar o estado local**

   ```powershell
   git status --short --branch
   ```

   Exibe o branch, seu acompanhamento remoto e eventuais alterações locais pendentes.

8. **Confirmar a configuração no GitHub**

   ```powershell
   gh repo view igctsdf-hub/meu-terceiro-repo --json nameWithOwner,url,visibility,defaultBranchRef
   ```

   Consulta o nome completo, a URL, a visibilidade e o branch padrão do repositório publicado.

## Inspeção local e criação do arquivo

Antes da criação, `Get-Location` confirmou o diretório atual. Os comandos PowerShell `Get-ChildItem -Force -LiteralPath . -Name`, `Get-ChildItem -LiteralPath .. -Filter AGENTS.md -Force` e `Get-ChildItem -LiteralPath . -Filter AGENTS.md -Force` verificaram o conteúdo local e a presença de instruções em `AGENTS.md`.

Este `README.md` foi criado diretamente no diretório clonado com uma ferramenta de edição de arquivos, antes de sua inclusão no commit inicial.
