# **COMANDOS DO GIT** #


<p align="center">
  <a href="#1-sparkles-ciclo-de-vida">Ciclo de Vida</a> &#xa0; | &#xa0; 
  <a href="#2-gear-configuração">Configuração</a> &#xa0; | &#xa0;
  <a href="#3-rocket-básicos">Básico</a> &#xa0; | &#xa0;
  <a href="#white_check_mark-requirements">Requirements</a> &#xa0; | &#xa0; 
  <a href="https://github.com/RicardoSantosSantana" target="_blank">Author</a>
</p>



### 1. :sparkles: Ciclo de Vida ### 

  >
  
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
    >
    ~~~
    git config --global user.email "(seu email github)" 
    git config --global user.name "(seu usuario github)"
    ~~~

2. **Desabilitar a paginação no git** 
    >
    ~~~
    git config --global core.pager cat
    git config --global man.viewer catman
    git config --global man.catman.cmd 'man -P "col -b"'
    ~~~

3. **Definir o Visual Studio Code como editor padrão.**
    >
    ~~~
    git config --global core.editor 'code --wait'
    ~~~

4. **Teste para saber se as configurações funcionaram.**
    >
    ~~~
    git config --global -e
    ~~~

5. **Comando listar configurações**

    ~~~
    git config --list
    ~~~

    >**:eyes:**  *Existem muitas outras configurações no git, entretanto essas foram as primeiras que trabalhei.*

6. **Token no cache do git**
    >
    **Adicionar**
    >
    ~~~
    git config --global credential.helper cache
    ~~~
    __Remover__
    ~~~    
    
    git config --global --unset credential.helper
    ~~~

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
  
  6. **Retornar  uma mudança no arquivo quando ainda estão em estado de ediçao** 

        ~~~
        git checkout Readme.md
        ~~~

  7. **Reset mudanças** 
        
        
        * **soft** - volta as modificaçoes com os arquivos em staged          
          
          >`git reset --soft "hash do commit"`
                  

        * **mixed** - volta as modificaçoes com os arquivos com o status de modified        
          >`git reset --mixed "hash do commit"`
        
        * **hard** - volta todas as modificaçoes
            >`git reset --hard "hash do commit"` 
        
  8. **Manipular Branch** 
      >

        * **Criar** 
          ~~~
          git checkout -b minhaBranch
          ~~~

        * **Excluir**
          ~~~
          git checkout -D minhaBranch
          ~~~
        
        * **Acessar**
          ~~~
          git checkout minhaBranch
          ~~~
        
        * **Unir Branches**

          Merge - 
          Rebase - 
    
      >
  9. **Git Stash** 
        >   
        Quando um arquivo ainda não está pronto para subir para o commit é possível usar o comando stash para aguardar até estar pronto, e isso não vai atrapalhar o fluxo dos outros arquivos.
        >
        ~~~
        git stash    
        ~~~

        > É importante lembrar que ele vai colocar em stash todos os arquivos de sua branch que estão status de modified.
  
        ~~~
        git stash apply - para aplicar 
        git stash list - para listar os stash
        git stash clear  - para limpar tudo que estiver em stash
        ~~~
  >
  10. **Criar Alias** 
        
        >

        > Cria um alias para o comando status bastando 		apenas digitar git s

        ~~~
        git config --global alias.s status 
        ~~~
  >
  11. **Criar Tags** 
      >
      ~~~
      git tag -a 1.0.0 -m "Primeira Versao"
      ~~~
 

<a href="https://github.com/RicardoSantosSantana">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=RicardoSantosSantana&theme=dracula&show_icons=true" />
</a>
