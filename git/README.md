# **COMANDOS DO GIT** #

### 1. :sparkles: Ciclo de Vida ### 

![Ciclo de vida do Git](/assets/images/git_ciclo.vida.png "Ciclo de Vida do Git")

  1. **Untracked** ( não marcado ) 

      São arquivos que ainda não foram adicionados ao Git, ou seja ainda não tem nenhuma versãoda existencia do arquivo no repositório.


  2. **UnModified** 

      Arquivos que foram adicionados mas ainda não foram modificados e por estarem nesta situação estão prontos para irem para a fase de staged ou seja podem ser adicionados ao repositório.
    
  3. **Modified** 

      Arquivos que foram modificados e devem ser adicionados para o Staged para poderem ser commitados
    
  4. **Staged**

      Área preparada pra a versão, após ter sido feito o commit, o status volta para unModified.

### 2. :gear: Configuração ###
 
1. **Usuário** 

  ~~~
  git config --global user.email "(seu email github)" 
  git config --global user.name "(seu usuario github)"
  ~~~

2. **Desabilitar a paginação no git** 

    ~~~
    git config --global core.pager cat
    git config --global man.viewer catman
    git config --global man.catman.cmd 'man -P "col -b"'
    ~~~

3. **Definir o Visual Studio Code como editor padrão.**
    ~~~
    git config --global core.editor 'code --wait'
    ~~~

4. **Teste para saber se as configurações funcionaram.**
    ~~~
    git config --global -e
    ~~~

5. **Comando listar configurações**

    ~~~
    git config --list
    ~~~

>**:eyes:**  *Existem muitas outras configurações no git, entretanto essas foram as primeiras que trabalhei.*

### 3. :rocket: Básicos ###

1. **Mostrar o status do git** 

    ~~~	
    git status
    ~~~

    > importante para saber qual fase do ciclo o repositório está no momento.

    2. **Adicionar arquivo ao Git** 
        
        ~~~		
        git add nomedoarquivo.extensao
        ~~~

        2.1 Adicionando no versionador

          ~~~ 
          git add Readme.md 
          ~~~

          2.2 Adicionando recursivamente
          
          >

          >É possível adicionar todos os arquivos pendentes usando o .(ponto) de forma recursiva, todos os arquivos em todos os diretórios.
                  
          ~~~
          git add .
          ~~~

    3. **Adicionar arquivo ao Git** 

        *Comando para criar um snapshot do arquivo. **git Commit***
        ~~~        
        git commit nomedoarquivo.extensao -m "mensagem do commit"
        ~~~

        >obs: o -m é para dizer para o git que tu vais passar uma mensagem no commit
        >>git commit Readme.md -am "mnensagem do commit" 

        obs: adicionar todos os arquivos modificados
        ~~~
        git commit . -am "esse comando já adiciona no stage e já faz o commit recursivamente"
        ~~~

    4. **Visualizar commits feitos** 

        ~~~
        git log	
        git log --decorate
        git log --graph
        ~~~
        4.1 **Listar a quantidade de commits por pessoas**

        ~~~
        git shortlog 
        ~~~

        4.2 **Forma gráfica**
        
        ~~~
        git log --author="nome do author"
        ~~~
    
        4.3 **Mostrar commit por hash do commit**
        
        ~~~
        git show **o id da branch**      
        ~~~
        >*o **id** do branch pode conseguir com git log*
        
        
        4.4 **Mostrar diferenças entre dois commit**
        
        ~~~
        git diff     
        ~~~
  
	  5. **Remover um arquivo do Staged** 

          ~~~
          git reset HEAD Readme.md
          ~~~
	
	

* Retornar  uma mudança no arquivo quando ainda estão em estado de ediçao
	
	git checkout Readme.md
	
	
* Reset mudanças
	é necessário escolher a hash apartir de qual commit quer iniciar o processo
	
	--soft
		volta as modificaçoes com os arquivos em staged
		git reset --soft 3f4c927ebe04df737455c245a292abea86655481
	--mixed
		volta as modificaçoes com os arquivos com o status de modified
		git reset --mixed 3f4c927ebe04df737455c245a292abea86655481
	--hard
		volta todas as modificaçoes
	
	8fd709234250a1aac05b61ba10ccc3414d39c920
* Criar branch
 
	git checkout -b testing
	
* Excluir branch
	git branch -D testing

* Unir Branches

	Merge - 
	git
	Rebase - 
			
	
* Git stash
	Quando um arquivo ainda não está pronto para subir para o commit posso usar
	o comando stash para aguardar até estar pronto, e isso não vai atrapalhar o fluxo 		dos outros arquivos.
	
	git stash
	
	Depois de terminar o arquivo
	
	git stash apply - para aplicar 
	git stash list - para listar os stash
	git stash clear  - para limpar tudo que estiver em stash

* Criar Alias
	git config --global alias.s status - cria um alias para o comando status bastando 		apenas digitar git s
* Criar Tags
	git tag -a 1.0.0 -m "Primeira Versao"
		

	
	
	
	
