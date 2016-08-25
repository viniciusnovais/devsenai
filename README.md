# devsenai
Repositorio da equipe - EasyCarros


Então pessoal vou deixar aqui um tutorial para facilitar para quem nunca usou versionamento .git.

Primeiro passo : gerar uma chave SSH

  Por qual motivo usamos chaves SSH? 
    simples para não precisarmos colocar usuario e senha toda vez que fomos subir um arquivo, imagina só que em um dia você suba,
    30 vezes no git você vai precisar colocar usuario e senha 30 vezes, com a chave ssh não precisa disso.
    
    Então para criar a chave SSH sigam os passos abaixo :
    
    1 - Abram o git bash (normalmente clicando com o botão direito do mouse em qualquer lugar pode ser a área de trabalho mesmo..);
    
    2 - digitem o seguinte comando : ssh-keygen -t rsa -b 4096 -C "your_email@example.com" , Troquem o email de exemplo pelo email 
    que vocês usaram para se cadastrar no git.
    
    3 - Quando a seguinte mensagem aparecer "Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]"
    pressionem a tecla ENTER
    
    4 - Quando as seguintes mensagens aparecerem "Enter passphrase (empty for no passphrase): [Type a passphrase]
                                                  Enter same passphrase again: [Type passphrase again]"
        Apertem a tecla ENTER
        
    5 - Digitem o seguinte comando : eval "$(ssh-agent -s)"
    
    6 - Por fim digitem o seguinte comando : ssh-add ~/.ssh/id_rsa
    
    Pronto chave SSH gerada!
    

Segundo Passo : cadastrar sua chave SSH no projeto 

  1 - Digitem o seguinte comando : clip < ~/.ssh/id_rsa.pub , com esse comando ele automaticamente copia sua chave SSH
  
  2 - Depois na pagina do projeto é so ir na aba Settings e lá vai ter Deploy Keys ai é so colocar a chave la e dar um nome para ela ex : joaoSSH 
      obs : não se esqueçam de marcar a caixinha que aparece embaixo para vocês poderem subir arquivos se não vocês só vão ter direito de leitura.
      
Terceiro passo :  Clonar o repositorio

    1 - Digitem o comando : git clone + o endereço do repositorio que você pega clicando no botão verde escrito clone (peguem a versão SSH e não HTTP) o git vai baixar o repositorio onde ele estiver então por exemplo se voce abrir o git na C: vai ficar C:/devsenai e assim por diante.
    
Quarto passo : Subindo arquivos para o repositorio
   
   1 - toda vez que vocês modificarem um arquivo ou adicionarem novas pastas ou arquivos digitem o seguinte comando : gi add .
      feito isso ele ira ler tudo que esta diferente e ja vai ficar "setado" o que ele vai subir.
      
  2 - Digitem o comando : git commit -m "comentario" , coloquem o que vocês mudaram no comentario , isso é mto importante por que se por acaso subir algo com bug ja sabe qual foi o arquivo modificado ! , 
  obs : comentario sempre "entre aspas duplas"
  
  3 - Por fim digitem git push -u origin master , feito isso ele subira todos os arquivos modificados e novos no diretorio.
  
Quinto passo : baixando att do repositorio

  1 - Digitem o comando git pull origin master , feio isso ele baixara todos os arquivos que tenham sido modificados ou pastas novas.
  
Bom é isso ai!
