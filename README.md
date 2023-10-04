# Resumos das aulas do Git/GitHub

**Repositório para armazenar anotações e links de fontes para estudo.**

## 📚 LINKS ÚTEIS
- [Documentação Git](https://git.scm.com/doc)
- [Documentação GitHub](https://docs.github.com/)
- [Documentação Markdown](https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

## 💻 Resumo das aulas

- **Aula 01** - Como criar um repositório remoto:
    **1.** Crie um novo repotirósio: 
    
            mkdir + nome do repositório.

    **2.** Inicie seu repositório: 
            
            git init.

    **3.** Conectando a um repositório GitHub Remoto:
            
            git .remote add origin + "Link URL repositório GitHub".

- **Aula 02** Salvando alterações no repositório local:

    **1.** Alterar algum arquivo previamente salvo.

    **2.** Adicionar o arquivo salvo a área de preparação:
    
             git add git add nome-do-arquivo.extensão.

    **3.** Salvar as alterações realizadas dentro do arquivo: 
    
            git commit -m "Mensagem desejada".


- **Aula 03** Desfazendo alterações no repositório local:

    **1.** Removendo um repositorio git de uma pasta indesejada: 
    
            rm -rf .git** comando para remover      forçadamente.

    **2.** Recuperando arquivos: 
    
            git restore + nome do.

    **3.** Como alterar a mensagem do último commit:
    
            git commit --amend -m 'Nova mensagem'.

    **4.** Desfazendo um commit: **git reset --(tipo do commit) + código hash**.
            
            soft: move a branch para um commit anterior, porém, mantem as alterações posteriores.
            mixed: move a branch para um commit anterior e remove as alterações desse commit e dos commits posteriores da área de preparação.
            hard: move a branch para um commit anterior e descarta todas as alterações dos commits posteriores.

    **5.** Retirando arquivos da área de preparação:
    
             git reset + nome do arquivo (resumos/aula-01.md).

    **6.** Restaurando após remoção: 
    
            git restore --staged + nome do arquivo (resumos/aula-01.md).
    
- **Aula 04** Enviando a baixando alterações:

    **1.** Abra o VSCode

    **2.** Vá na abba de Source Control

    **3.** Clique em "Commit & Push", caso deseje comentar, apenas insira um comentário na caixa de mensagens.
        
        Para realizar alterações dentro do terminal basta utilizar 'git push' ou 'git push origin nome da branch desejada'

    **4.** Para atualizar o repositório local com as alterações feitas no repositório remoto é só utilizar o comando:

        git pull

- **Aula 05** Trabalhando com branches:
    
    **1.** Mudando de uma branch atual para nova dentro da mesma branch (criando uma branch dentro da outra)

        git checkout -b nome da branch desejada
        git checkout nome da branch principal - 'para retornar a branch original'

    **2.** Mesclando as branchs
        
        git merge nome da branch para mesclar

   **Aula 06** Trabalhando com branches:

    **1.** Buscando informações do repositório remoto, mas sem alterar o repositorio local

        git fetch nome do repositorio e branch
   
    **2.** Baixando arquivos da branch remota sem mesclar com a local.
    
        git merge origin/main

    **3.** Clonando um repositório com várias branchs, caso não ocorra a identificação da branch o comando irá clonar apenas a principal
        
        git clone URL repositorio --branch desejada --single-branch

## 📋 Comandos Úteis
- **cat**: Exibe o conteúdo de configuração de um arquivo.
- **git remote -v**: Exibe os repositórios vinculados.
- **git status**: Exibe o 'Status' da árvore de trabalho ou da sua preparação.
- **touch -nome do arquivo-.-extensão**: Cria um arquivo vázio com o nome e extensão especificadas.
- **git log**: Exibe os logs do diretório.
- **git add nome-do-arquivo.extensão**: Adiciona o arquivo especificado que foi modificado a área de preparação.
- **git add .**: Adiciona todos os arquivos a área de preparação.
- **git commit -m "Mensagem desejada"**: Salva as alterações feitas dentro do repositório.
- **git log**: Exibe todos os commits realizados.
- **echo arquivo-desejado/ > .gitignore**: Insere o arquivo desejado dentro do gitignore para que suas alterações não sejam salvas durante o commit.
- **echo > .gitignore**: Limpa a lista de arquivos ignorados.
- **git reflog**: mostra um histórico mais detalhado dos commits realizados
- **echo '#nome do arquivo' > nome do arquivo**: cria um novo commit dentro do arquivo
- **git branch -v**: lista o último commit de cada branch
- **git branch -d nome da branch**: deleta a branch desejada
- **git branch**: retorna todas as branchs do repositório
- **git fetch**: busca valores do repositório remoto, mas não os mistura com os valores do repositório local.
- **git diff main origin/main**: lista as diferenças entre os arquivos do repositorio local e do repositório remoto