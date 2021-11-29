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
    
    github: USERNAME

    git config --global user.name ""
	  git config --global user.email "mirianbernardes@gmail.com"