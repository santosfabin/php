# PHP

- Introdução
    1. Vamos utilizar:
        1. VScode
            1. Extensões:
                - PHP Intelephense
                    - Caso esteja com problemas:
                        - procure pelo erro ‘php.validate.executablePath’ dentro do VSCode
                        - em "php.validate.executablePath": ""  preencha essas ultimas “” com o link local que esta o arquivo executável do laragon, exemplo: C:/laragon/bin/php/php-8.1.3-Win32-vs16-x64/php.exe
                - Material Icon Theme
        2. Laragon
            1. baixar a versão mais nova do PHP 7 e 8 Thread Safe
            [https://windows.php.net/download/](https://windows.php.net/download/)
            2. caso de algum erro no apache quando der inicio, basta clicar com o botao direito na tela iniciar do laragon;
            ir no Apache;
            dir: conf;
            abrir o		mod_php.conf	com um bloco de notas;
            tirar o numero q esta em	LoadModule php8_module;
            3. caso de outro erro, baixe a versão x64 do	VC15 & VS16
    2. ao clicar em	start all	no laragon, ele vai criar uma pagina web localhost
        1. para abrir o local dos arquivos, basta clicar em	Root
        la se pode editar os arquivos

---

- INDEX
    - O index é o nome que se da ao arquivo no qual se apresentará primeiro
        - ou seja, é fundamental ter no mínimo e máximo um arquivo chamado **index,** pois sem ele o programa q iniciará a execução de seu site não entenderá qual arquivo deverá ser aberto, causando assim um erro, então SEMPRE coloco UM index
        - caso tenha 2 index, um sendo index.php e o outro sendo index.html, o programa executador que escolherá sua preferência
    - Caso queira mudar isso no Laragon
        - Mouse2 dentro da tela do Laragon
        - Apache
        - httpd.conf
        
        ---
        
        - ou em:
            - C:\laragon\bin\apache\httpd-2.4.47-win64-VS16\conf
        
        ---
        
        - vá para a linha 286
        - então altere a ordem que desejar
            - se é primeiro o .html ou o .php

---

- 

---

- Referencias
    1. [https://www.youtube.com/watch?v=jVUeF7cZdFE&list=PLXik_5Br-zO9wODVI0j58VuZXkITMf7gZ&index=2](https://www.youtube.com/watch?v=jVUeF7cZdFE&list=PLXik_5Br-zO9wODVI0j58VuZXkITMf7gZ&index=2)
    2. [https://windows.php.net/download/](https://windows.php.net/download/)
    3. [https://code.visualstudio.com/](https://code.visualstudio.com/)