# PHP FULL

- Glossário
    
    fd == ao clicar em f12 e ir em network/rede/ou_algo_do_tipo é possível ver as requisições feito ao servidor
    
    —F == importante
    

---

- Introdução
    - Arpanet = (pai da internet)
        - conexão de computadores
        - troca de dados
        - independente de aplicações WEB
    - WEB
        - serviço que usa a internet pra existir
        - HYPER TEXTO
    - HTTP
        - Hypertext Transfer Protocol
    - Paradigma é um padrão uma conduta, uma forma de fazer alguma coisa
        - o PHP suporta tanto o paradigma procedural quanto o paradigma de orientação a objeto

---

- Instalação do XAMPP
    - link
        
        [https://www.apachefriends.org/pt_br/index.html](https://www.apachefriends.org/pt_br/index.html)
        
        - é um pacote que vai instalar basicamente o MySQL, PHP e o Apache
    - Nisso é necessário deixar para instalar essas opções:
        - Apache
        - MySQL
        - PHP
        - phpMyAdmin

---

- ?.php
    - Para ver qual script será executado para início de página basta:
        - Clique em Config na parte do Apache
        - e procure ou use o Ctrl + f para buscar por “DirectoryIndex”
        - lá terá uma lista de preferência em ordem sobre qual arquivo ele irá procurar, caso não seja especificado
    - Lá você pode mudar/adicionar prioridades
        - por exemplo, você pode adicionar um script principal para iniciar
        

---

- Como usar
    - Ele o index ou outra página deverá ser .php
        - caso contrário ele não reconhecerá o php enserido
    - Não há limites de php inseridos
    - Sintaxe da abertura de comando
        
        ```php
        <html>
        	<body>
        		<?php
        			codigo;
        		?>
        	</body>
        </html>
        ```
        
        - ou
        
        ```php
        <?php
        	codigo;
        ?>
        <html>
        	<body>
        		<?php
        			codigo;
        		?>
        		<?php
        			codigo;
        		?>
        	</body>
        </html>
        ```
        
        - ou quando for apenas php
        
        ```php
        <?php
        	codigo;
        ```
        
        - ou em alguns casos+ em apresentação de texto
            
            ```php
            <?= escrita ?>
            ```
            
            - podendo ser apresentado dentro de um html, como por exemplo
            
            ```php
            <html>
            	<body>
            		<div class=<?= escrita ?>>
            		</div>
            		</div>
            	</body>
            </html>
            ```
            

---

- Apresentar texto
    - Existem dois comandos
        - print
            - em sua essência ele é uma função
        - echo
        - Sintaxes
            
            ```php
            echo "PHP";
            print "PHP";
            ```
            
            ```php
            echo 'PHP';
            print 'PHP';
            ```
            
            ```php
            echo ("PHP");
            print ("PHP");
            ```
            
    - Exemplo
        
        ```php
        <!DOCTYPE html>
        <html lang="pt-br">
            <head>
                <meta charset="UTF-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Document</title>
            </head>
            <body>
                <?php echo 'teste 1' ?>
                <br>
        
                <?php print "teste 2" ?>
                <br>
                <?php echo print "teste 2" ?>
        
                <?= 'teste 3' ?>
            </body>
        
        </html>
        ```
        
    
    ---
    
    - Ele consegue usar elementos html dentro do echo/print
        
        ```php
        <!DOCTYPE html>
        <html lang="pt-br">
            <head>
                <meta charset="UTF-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Document</title>
            </head>
            <body>
                <?php echo 'teste 1<br>' ?>
        
                <?php print "teste 2<br>" ?>
        
                <?= 'teste 3<hr>' ?>
            </body>
        
        </html>
        ```
        

---

- Comentário
    - Comentário de UMA linha
        
        ```php
        // comentario 
        # comentario
        ```
        
    - Comentário com MAIS de uma linha
        
        ```php
        /*
        comentario 
        comentario
        */
        ```
        
    - shift + alt + A
        - ao selecionar várias linhas e fizer esse comando, ele comentará as linhas selecionadas
    - Comentário inválido
        
        ```php
        <!DOCTYPE html>
        <html lang="pt-br">
            <head>
                <meta charset="UTF-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Document</title>
            </head>
            <body>
                <?php
                    /*asfasf
                    asfasf*/
        
                    // asdas
        
                    #coasfonba
                ?>
                // comentario invalido (pois esta na parte do html nao do php)
            </body>
        
        </html>
        ```
        
        - ele TEM que estar dentro do <?php ?> para ser comentado

---

- Variáveis
    - O que é
        - É um “espaço” onde se pode guardar algum dado/informação
            - sendo ele número, texto, etc
        - Elas servem para diversas coisas, uma delas é ser usada para operação, ou como um resultado
        - Pode-se se definir um valor de um tipo e depois ser mudada automaticamente para outro tipo
    
    ---
    
    - Iniciando variável
        - Elas devem ser iniciada com um $ na frente, seguida de um identificador (nome)
        - As variáveis SÃO sensitive case
            - ou seja, uma letra maiúscula é diferente da minúscula
        - Sintaxe
            - é necessário ao fim de cada “operação” um ;
                
                ```php
                $variavel;
                $var1;
                $var_um;
                $varUm;
                $_um;
                $_1;
                ```
                
            - iniciando com um valor
                
                ```php
                $variavel = 100;
                ```
                
            - mudando seu valor
                
                ```php
                $variavel = 100;
                
                // operacao
                
                $variavel = 'fimteste';
                ```
                
        - Sintaxe INCORRETA
            
            ```php
            $1var = 0;
            $!var = 0;
            $variavel(1) = 0;
            $variavel um = 0;
            $variavel-um = 0;
            ```
            
    
    ---
    
    - Testando
        
        ```php
        <!DOCTYPE html>
        <html lang="pt-br">
            <head>
                <meta chanset="utf-8">
                <meta name="viewport" content="width=device-width, initial scale=1.0">
                <title>Teste PHP</title>
            </head>
            <body>
        
                <?php
                    $nome = 'Fabiano Santos';
                    $idade = 29;
                    $peso = 82.5;
                    $fumante = true; //(true = 1) ou (false = vazio)
                ?>
                <h1>Ficha</h1>
                <br>
                <p>Nome: <?php echo $nome ?></p>
                <p>Idade: <?= $idade ?></p>
                <p>Peso: <?= $peso ?></p>
                <p>Fumante: <?= $fumante ?></p>
                
            </body>
        </html>
        ```
        
    
    ---
    
    - Alterando variáveis
        
        ```php
        <!DOCTYPE html>
        <html lang="pt-br">
            <head>
                <meta chanset="utf-8">
                <meta name="viewport" content="width=device-width, initial scale=1.0">
                <title>Teste PHP</title>
            </head>
            <body>
        
                <?php
                    $nome = 'Fabiano Santos';
                    $idade = 29;
                    $peso = 82.5;
                    $fumante = true; //(true = 1) ou (false = vazio)
                    
                    #... logica / operacao
        
                    $idade = 30;
                ?>
                <h1>Ficha</h1>
                <br>
                <p>Nome: <?php echo $nome ?></p>
                <p>Idade: <?= $idade ?></p>
                <p>Peso: <?= $peso ?></p>
                <p>Fumante: <?= $fumante ?></p>
                
            </body>
        </html>
        ```
        
    
    ---
    
    - Concatenação
        - Para isso usando o operador  .  que fará a concatenação
            
            ```php
            <!DOCTYPE html>
            <html lang="pt-br">
                <head>
                    <meta chanset="utf-8">
                    <meta name="viewport" content="width=device-width, initial scale=1.0">
                    <title>Teste PHP</title>
                </head>
                <body>
            
                    <?php
            
                        $nome = 'Fabiano';
                        $cor = 'azul';
                        $idade = 18;
            
                        // operador .
                        echo 'Olá ' . $nome .', vi que sua cor preferida é ' . $cor .', e que voce tem '. $idade .' anos';
            
                    ?>
                    
                </body>
            </html>
            ```
            
        - Ou é possível usar as “”
            - ela consegue ler e interpretar variáveis dentro de si
            
            ```php
            <!DOCTYPE html>
            <html lang="pt-br">
                <head>
                    <meta chanset="utf-8">
                    <meta name="viewport" content="width=device-width, initial scale=1.0">
                    <title>Teste PHP</title>
                </head>
                <body>
            
                    <?php
            
                        $nome = 'Fabiano';
                        $cor = 'azul';
                        $idade = 18;
            
                        echo "Olá  $nome, vi que sua cor preferida é  $cor, e sua idade é  $idade";
            
                    ?>
                    
                </body>
            </html>
            ```
            
            - ou seja, “” é um pouco mais lento, pois ele sempre irá conferir se há variáveis dentro de si, então caso não precise usar variáveis use a ‘ ’
    
    ---
    
    - Constantes
        - É uma variável que não será modificada em sua operação
            - ou seja, em momento algum ela poderá ser redefinida
        - Sintaxe de definição
            
            ```php
            define('NOME_VARIAVEL', 'valor')
            ```
            
        - Sintaxe de utilização
            
            ```php
            echo NOME_VARIAVEL;
            ```
            
            - é de boa prática mante maiúsculo o nome de variável constante
        - Exemplo
            
            ```php
            <!DOCTYPE html>
            <html lang="pt-br">
                <head>
                    <meta chanset="utf-8">
                    <meta name="viewport" content="width=device-width, initial scale=1.0">
                    <title>Teste PHP</title>
                </head>
                <body>
            
                    <?php
            
                        define('BD_URL', 'endereco_bd_dev');
                        define('BD_USUARIO', 'usuario_dev');
                        define('BD_SENHA', 'senha_dev');
            
                        echo BD_URL . '<br>';
                        echo BD_USUARIO . '<br>';
                        echo BD_SENHA;
            
                    ?>
                    
                </body>
            </html>
            ```
            
    
    ---
    
    - Tipo de dados
        
        
        | $inteiro = 100; | int | número inteiro |
        | --- | --- | --- |
        | $float = 10.5; | flaot  | casas decimais |
        | $boll = true; | verdadeiro/falso | ligado/desligado |
        | $string = “Olá Mundo!”; | String | cadeia de caracteres |
        | $array = [1, 2, 3]; | Array | coleção de valores |
        | $pessoa = new Pessoa(); | objeto | propriedade e métodos |
        | $nulo = null; | null | variável com o valor nulo |

---

- Comparadores
    1. Ele sempre irá comparar o valor da esquerda para o da direita
        - comparador
            
            
            | 2 == 3 | false |
            | --- | --- |
            | 100 == 100 | true |
            | 50 == ‘50’ | true |
            | 50 === ‘50’ | false |
        - ==
            - equivale a comparação
        - ===
            - verifica se o valor é igual
            - verifica se seu tipo é igual
        
        ---
        
        - diferente / não idêntico
            
            
            | 2 !=  3 | true |
            | --- | --- |
            | 2 <> 3 | true |
            | 50 != 50 | false |
            | 50 != ‘50’ | false |
            | 50 !== ‘50’ | true |
        - !=
            - equivale a diferente
        - <>
            - equivale a diferente
        - !==
            - verifica se o valor é diferente
            - verifica se o tipo é diferente
        
        ---
        
        - maior, menor, maior ou igual, menor ou igual
            
            
            | 2 >  3 | false |
            | --- | --- |
            | 2 < 3 | true |
            | 50 >= 50 | true |
            | 50 <= 50 | true |
            | 50 < 50 | false |
        
        ---
        
        - Spaceship operator
            
            
            | 1 <=> 1 | 0 | (1 == 1) |
            | --- | --- | --- |
            | 3 <=> 2 | 1 | (3 > 2) |
            | 1 <=> 2 | -1 | (1 < 2) |
            - sempre vai ser:
                - 0
                - 1
                - -1

---

- Operadores matemáticos
    
    
    | = | atribuição |
    | --- | --- |
    | + | soma |
    | - | subtração |
    | * | multiplicação |
    | / | divisão |
    | % | modulo (resto da divisão) |
    | ** | expoente (potência) |
    - Exemplo
        
        ```php
        <!DOCTYPE html>
        <html lang="pt-br">
            <head>
                <meta charset="UTF-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Document</title>
            </head>
            <body>
                <?php
                    echo 10 / 5;
        						echo 10 % 5;
        						echo 10 - 5;
                    echo 10 + 5;
        						echo 10 * 5;
        						echo 10 ** 5;
                ?>
            </body>
        
        </html>
        ```
        
        ```php
        <!DOCTYPE html>
        <html lang="pt-br">
            <head>
                <meta charset="UTF-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Document</title>
            </head>
            <body>
                <?php
                    $a = 10;
                    $b = 20;
                    $c = $d = $h = 100;
                    $resultado = $a + $b;
                    $resultado = $a + 100;
                    $resultado = $a * $b;
                    $resultado = 1000 + $a + 10 + $b;
        
                ?>
            </body>
        
        </html>
        ```
        
        - operações com a própria variável
        
        ```php
        <!DOCTYPE html>
        <html lang="pt-br">
            <head>
                <meta charset="UTF-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Document</title>
            </head>
            <body>
                <?php
                    $a = 10;
                    $a = $a + 20; #30
                    #ou
                    $a += 20; #30
                    #ou
                    $a++; # $a = $a + 1;
                    $a--; # $a = $a - 1;
                        #ela mostrará o valor com + ou - 1, na PRÓXIMA utilização
        
                    ++$a; # $a = $a + 1;
                    --$a; # $a = $a - 1;
                        #assim que é feito esse comando ele atribuirá esse valor imediatamente
                ?>
            </body>
        
        </html>
        ```
        
        - Exemplo
        
        ```php
        <!DOCTYPE html>
        <html lang="pt-br">
            <head>
                <meta charset="UTF-8">
                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                <title>Document</title>
            </head>
            <body>
                <?php
                    $a = 20;
                    echo $a++;
                    echo '<br>';
                    echo $a;
                    #
                    echo '<br>';
                    #
                    echo $b = 20;
                    echo '<br>';
                    echo ++$b;
                ?>
            </body>
        
        </html>
        ```
        
    
    ---
    
    - Eperação
        
        ```php
        <?php
            $num1 = 10;
            $num2 = 5;
            
            echo "A soma entre $num1 e $num2 é: " . ($num1 + $num2);
        ?>
        ```
        
        ```php
        <?php
            $num1 = 10;
            $num2 = 2;
            
            echo "$num1 elevado por $num2 é: " . ($num1 ** $num2);
        ?>
        ```
        

---

- Operadores lógicos
    
    
    | AND ou && | E | Verdadeiro se todas as expressões forem verdadeiro |
    | --- | --- | --- |
    | OR ou || | OU | Verdadeiro se pelo menos UMA das expressões for verdadeira |
    | XOR | XOR | Verdadeiro apenas se UMA das expressões forem verdadeira, MAS NÃO AMBAS (não importa a posição do verdadeiro e do falso) |
    | ! | Negação | Inverte o resultado da expressão |
    - Exemplo
        
        ```php
        <!DOCTYPE html>
        <html lang="pt-br">
            <head>
                <meta chanset="utf-8">
                <meta name="viewport" content="width=device-width, initial scale=1.0">
                <title>Teste PHP</title>
            </head>
            <body>
        
                <?php
        
                    //...  && . AND ... 
                    if (2 == 3 && /*AND*/10 > 3) {
                        echo 'Verdadeiro';
                    }else {
                        echo 'Falso';
                    }
        
                    echo '<br>';
        
                    //...  || . OR ... 
                    if (2 == 3 || /*OR*/10 > 3) {
                        echo 'Verdadeiro';
                    }else {
                        echo 'Falso';
                    }
        
                    echo '<br>';
        
                    //...  XOR ... 
                    if (2 == 3 XOR 10 > 3) {
                        echo 'Verdadeiro';
                    }else {
                        echo 'Falso';
                    }
        
                    echo '<br>';
        
                    //...  ! ... 
                    if (!(2 == 2)) {
                        echo 'Verdadeiro';
                    }else {
                        echo 'Falso';
                    }
        
                    echo '<br>';
        
                    //...  ! ... 
                    if (2 == 2 AND 3 == 3 AND 5!= 5) {
                        echo 'Verdadeiro';
                    }else {
                        echo 'Falso';
                    }
        
                ?>
                
            </body>
        </html>
        ```
        

---

- if/else
    - Sintaxe
        
        ```php
        if (condicao) {
        	//trecho do código
        }
        ```
        
    - ou
        
        ```php
        if (condicao) {
        	//trecho do código
        }else {
        	//trecho do código
        }
        ```
        
    - ou
        
        ```php
        if (condicao) {
        	//trecho do código
        }else if (condicao) {
        	//trecho do código
        }else if (condicao) {
        	//trecho do código
        }else {
        	//trecho do código
        }
        ```
        
    
    ---
    
    - Exemplo
        
        ```php
        <!DOCTYPE html>
        <html lang="pt-br">
            <head>
                <meta chanset="utf-8">
                <meta name="viewport" content="width=device-width, initial scale=1.0">
                <title>Teste PHP</title>
            </head>
            <body>
        
                <?php
        
                    if (2 == 2) {
                        echo 'Verdadeiro';
                    }else {
                        echo 'Falso';
                    }
                    
                    echo '<br>';
        
                    if (2 == 3) {
                        echo 'Verdadeiro';
                    }else {
                        echo 'Falso';
                    }
        
                ?>
                
            </body>
        </html>
        ```
        

---

- Operador ternário
    - Sintaxe
        
        ```php
        condicao ? true : false;
        ```
        
    - Exemplos
        
        ```php
        <!DOCTYPE html>
        <html lang="pt-br">
            <head>
                <meta chanset="utf-8">
                <meta name="viewport" content="width=device-width, initial scale=1.0">
                <title>Teste PHP</title>
            </head>
            <body>
        
                <?php
        
                    $condicao = true;
        
                    echo $condicao ? 'sim' : 'não';
                    $resposta = $condicao ? 'sim' : 'não';
                    echo $resposta;
        
                ?>
                
            </body>
        </html>
        ```
        
        ```php
        <!DOCTYPE html>
        <html lang="pt-br">
            <head>
                <meta chanset="utf-8">
                <meta name="viewport" content="width=device-width, initial scale=1.0">
                <title>Teste PHP</title>
            </head>
            <body>
        
                <?php
                    $valor = 1;
                    echo $valor == 1 ? 'Tá certo' : 'Tã errado';
                ?>
                    <?= $valor == 1 ? 'Tá certo' : 'Tã errado'; ?>
        
            </body>
        </html>
        ```
        

---

- Switch
    - Sintaxe
        
        ```php
        $opcao = 2;
        switch (opcao) {
        	case 1:
        		//trecho do código
        		break;
        	case 2:
        		//trecho do código;
        		break;
        	default:
        		//trecho do código;
        		break;
        }
        ```
        
        aula 319
        

---

- Casting
    - Ela converte um tipo de dado para outro
    - Sintaxe
        
        ```php
        $variavel = (tipo) $variavel;
        $variavel = (tipo) $variavel2;
        ```
        
    - Verificação do tipo
        - Exemplo 1
            
            ```php
            <?php
                //gettype()  =>  retorna o tipo da variável
                $valor = 10;
                $valor2 = (float) $valor; // float, double, real
            
                echo $valor . ' ' .gettype($valor);
                echo '<br>';
                echo $valor2 . ' ' . gettype($valor2);
            ?>
            ```
            
        - Exemplo 2
            
            ```php
            <?php
                //gettype()  =>  retorna o tipo da variável
                $valor = 15.35;
                $valor2 = (int) $valor; // float, double, real
            
                echo $valor . ' ' .gettype($valor);
                echo '<br>';
                echo $valor2 . ' ' . gettype($valor2);
            ?>
            ```
            
        - Exemplo 3
            
            ```php
            <?php
                //gettype()  =>  retorna o tipo da variável
                $valor = 15.35;
                $valor2 = (int) $valor; //integer, int
            
                echo $valor . ' ' .gettype($valor);
                echo '<br>';
                echo $valor2 . ' ' . gettype($valor2);
            ?>
            
            <?php
                //gettype()  =>  retorna o tipo da variável
                $valor = 15.35;
                $valor2 = (string) $valor;
            
                echo $valor . ' ' .gettype($valor);
                echo '<br>';
                echo $valor2 . ' ' . gettype($valor2);
            ?>
            ```
            
        - Exemplo 4
            
            ```php
            <?php
                //gettype()  =>  retorna o tipo da variável
                $valor = '22.12';
                $valor2 = (integer) $valor;
            
                echo $valor . ' ' .gettype($valor);
                echo '<br>';
                echo $valor2 . ' ' . gettype($valor2);
            ?>
            
            <?php
                //gettype()  =>  retorna o tipo da variável
                $valor = 'abc';
                $valor2 = (integer) $valor;
                echo $valor . ' ' .gettype($valor);
                echo '<br>';
                echo $valor2 . ' ' . gettype($valor2);
            ?>
            
            <?php
                //gettype()  =>  retorna o tipo da variável
                $valor = '22.12';
                $valor2 = (float) $valor; 
                echo $valor . ' ' .gettype($valor);
                echo '<br>';
                echo $valor2 . ' ' . gettype($valor2);
            ?>
            ```
            
        - Exemplo 5
            
            ```php
            <?php
                //gettype()  =>  retorna o tipo da variável
                $valor = '22.12';
                $valor2 = (boolean) $valor; // boolean, bool
            
                echo $valor . ' ' .gettype($valor);
                echo '<br>';
                echo $valor2 . ' ' . gettype($valor2);
            ?>
            
            <?php
                //gettype()  =>  retorna o tipo da variável
                $valor = '';
                $valor2 = (boolean) $valor; // boolean, bool
            
                echo $valor . ' ' .gettype($valor);
                echo '<br>';
                echo $valor2 . ' ' . gettype($valor2);
            ?>
            ```
            
        - Exemplo 6
            
            ```php
            <?php
                //gettype()  =>  retorna o tipo da variável
                $valor = true;
                $valor2 = (int) $valor; // boolean, bool
            
                echo $valor . ' ' .gettype($valor);
                echo '<br>';
                echo $valor2 . ' ' . gettype($valor2);
            ?>
            
            <?php
                //gettype()  =>  retorna o tipo da variável
                $valor = false;
                $valor2 = (int) $valor; // boolean, bool
            
                echo $valor . ' ' .gettype($valor);
                echo '<br>';
                echo $valor2 . ' ' . gettype($valor2);
            ?>
            
            <?php
                //gettype()  =>  retorna o tipo da variável
                $valor = false;
                $valor2 = (string) $valor; // boolean, bool
            
                echo $valor . ' ' .gettype($valor);
                echo '<br>';
                echo $valor2 . ' ' . gettype($valor2);
            ?>
            
            <?php
                //gettype()  =>  retorna o tipo da variável
                $valor = true;
                $valor2 = (string) $valor; // boolean, bool
            
                echo $valor . ' ' .gettype($valor);
                echo '<br>';
                echo $valor2 . ' ' . gettype($valor2);
            ?>
            ```
            

---

- Funções
    - Basicamente são usadas para não precisarem serem reescritas todas hora, então uma função atende a esse pedindo, sendo mais simples e rápido utiliza-la mais vezes
    - Também é mais fácil reorganizar caso tenha algum problema, pois basta ir na função e modificar o que é necessário
    - Sintaxe
        
        ```php
        function nomeFuncao (parametros/entrada de dados da funcao) {
        	echo "Olá";
        }
        ```
        
    - Exemplo da sintaxe
        
        ```php
        <?php
            function calcularAreaTerreno($paremetro1, $parametro2) {
                $area = $paremetro1* $parametro2;
                return $area;
            }
        ?>
        ```
        
    
    ---
    
    - Como chamar uma função?
        - basta colocar seu nome
            
            ```php
            <?php
                function exibirBoasVindas () {
                    echo "Salve meu bom, beleza? <br>";
                }
            
                exibirBoasVindas();
                exibirBoasVindas();
            ?>
            ```
            
            - ou seja, essa function utilizada é uma função void, ou seja SEM RETORNO (return)
        
        ---
        
        - function COM return
            
            ```php
            <?php
                function calcularAarea ($largura, $comprimento) {
                    return $largura * $comprimento;
                }
                echo calcularAarea(30, 50);
            ?>
            ```
            
            - repare que é necessário passar os valores para os parâmetros requeridos, como nesse exemplo tinha 2 valores , foi colocado 2 valores para serem atribuídos
        - Outro Exemplo
            
            ```php
            <?php
                function calcularMedia ($nota1, $nota2, $nota3, $nota4) {
                    $media = ($nota1 + $nota2 + $nota3 + $nota4) / 4;
                    return $media;
                }
                $resultado = calcularMedia(5, 5, 5, 5);
                echo $resultado;
            ?>
            ```
            
    
    ---
    
    - Pequeno exercício
        
        ```php
        <!DOCTYPE html>
        <html>
            <head>
                <meta chanset="utf-8">
                <meta name="viewprt" content="width=device-width, initial scale=1.0">
            </head>
            <body>
        
                <?php
        
                    function calcularImpostoDeReda ($salario) {
                        $imposto = 0;
                        if ($salario >= 1903.99 AND $salario <= 2826.65) {
                            $imposto = ($salario * 7.5) / 100;
                        }else if ($salario >= 2826.66 && $salario <= 3751.05) {
                            $imposto = ($salario * 15) / 100;
                        }else if ($salario >= 3751.06 AND $salario <= 4664.68) {
                            $imposto = ($salario * 22.5) / 100;
                        }else if ($salario > 4664.68) {
                            $imposto = ($salario * 27.5) / 100;
                        }else {
                            $imposto = 'isento';
                        }
                        return $imposto;
                    }
        
                    echo calcularImpostoDeReda(5000);
        
                ?>
        
            </body>
        
        </html>
        ```
        

---

- Manipulação de strings
    - funções de manipulação
        
        
        | strtolower($texto) | transforma todos os caracteres em minúsculos |
        | --- | --- |
        | strtoupper($text) | transforma todos os caracteres em maiúsculos |
        | ucfirst($text) | transforma o primeiro caracter em maiúsculo |
        | strlen($text) | conta a quantidade de caracteres (inclusive espaços) |
        | str_replace(<procura por>, <subsitui por>, $text) | substitui uma cadeia de caracteres por uma outra dentro de uma string |
        | substr($tex, <posicao inicial>, <qtde caracteres a partir da posição iniciada>) | retorna parte de uma string |
    - Exemplos
        
        ```php
        <?php
        
            $text = 'fabiano Santos de Negreiros';
        
            //string to lower
            echo $text . '<br>';
            echo strtolower($text);
            
            //string to upper
            echo '<hr>';
            echo $text . '<br>';
            echo strtoupper($text);
            
            //upper case first
            echo '<hr>';
            echo $text . '<br>';
            echo ucfirst($text);
            
            //string lenth
            echo '<hr>';
            echo $text . '<br>';
            echo strlen($text);
        
            /* ... IMPORTANTE ... */
        
                //outro texto
                $text1 = 'filha da puta';
                //string replace
                    //ela é case sensitive
                echo '<hr>';
                echo $text1 . '<br>';
                echo str_replace('puta','palavrão não',$text1);
                echo '<hr>';
                echo str_replace('.', ',', '20.20...');
                
                //string lenth
                    //sempre é iniciado por 0
                echo '<hr>';
                echo $text . '<br>';
                echo substr($text, 8, 6) . ' ...';
                
            /* ... IMPORTANTE ... */
        
        ?>
        ```
        
    - —F
        
        ```php
        $titulo = str_replace('#', '-', $_POST['titulo']);
        $categoria = str_replace('#', '-', $_POST['categoria']);
        $descricao = str_replace('#', '-', $_POST['descricao']);
        echo $texto = $titulo . '#' . $categoria . '#' . $descricao;
        ```
        

---

- Manipulação matemáticas
    - funções matemáticas
        
        
        | ceil($numero) | arredonda o valor para MAIS |
        | --- | --- |
        | floor($numero) | arredonda o valor para MENOS |
        | round($numero) | arredonda o valor com base nas casas decimais |
        | rand()
        ou
        rand(inicio, fim) | gera um inteiro aleatório |
        | sqrt($numero) | retorna a raiz quadrada |
        | pow($numero) | potência |
        - mais funções em:
            - [https://www.php.net/manual/pt_BR/ref.math.php](https://www.php.net/manual/pt_BR/ref.math.php)
    - Exemplo
        
        ```php
        <?php
        
            $num = 7.4999;
            echo $num . '<br>';
        
            echo ceil($num) . '<br>';
            echo floor($num) . '<br>';
        
            echo round($num) . '<br>'; 
                // .0 a .4 => pra baixo
                // .5 a .9 => pra cima
            
            echo rand(10, 20) . '<br>'; 
            echo getrandmax() . '<br>';  // valor máximo do sistema
        
            echo sqrt(10) . '<br>'; 
        
        ?>
        ```
        
    

---

- Manipulação de data
    - Funções de data
        - cata corrente
        
        | date(formato) | recuperar a data atual | https://www.php.net/manual/pt_BR/datetime.format.php |
        | --- | --- | --- |
        | date_default_timezone_get(timezone) | recuperar o timezone default da aplicação |  |
        | date_default_timezone_set(timezone) | atualizar o timezone default da aplicação | https://www.php.net/manual/en/timezones.php |
        | strtotime(data) | transformar datas textuais em segundo |  |
        | abs() | retorna um valor sempre positivo |  |
    
    ---
    
    - Exemplo do date
        
        ```php
        <?php
            echo date('d');
        ?>
        ```
        
        ```php
        <?php
            echo date('d/m/y H:i') . '<br>';
        			//é opicional a ordem e separação
            echo date('y-m-d i:H');
        ?>
        ```
        
        - essa operação é feita a partir do sistema operacional usado
            - ou seja é do service, NÃO do client
    
    ---
    
    - Exemplo date_default_timezone_get()
        - ela serve pra saber qual o timezone pré-definido
            
            ```php
            <?php
                echo date_default_timezone_get();
            ?>
            ```
            
    
    ---
    
    - Exemplo date_default_timezone_set()
        - ela serve para set o timezone
            
            ```php
            <?php
                echo date('d/m/y H:i') . '<br>';
                date_default_timezone_set('America/Sao_Paulo');
                echo date('d/m/y H:i') . '<br>';
            ?>
            ```
            
            - É possível fazer essa modificação pelo arquivo php.ini
                
                ![Untitled](PHP%20FULL%209da733f133934045afa87d7ba4e7997d/Untitled.png)
                
                ![Untitled](PHP%20FULL%209da733f133934045afa87d7ba4e7997d/Untitled%201.png)
                
                - ctrl + f
                    - escreva “timezone”
                
                ![Untitled](PHP%20FULL%209da733f133934045afa87d7ba4e7997d/Untitled%202.png)
                
                - então troque para o desejado
                
                ![Untitled](PHP%20FULL%209da733f133934045afa87d7ba4e7997d/Untitled%203.png)
                
                - Por fim, reinicie o sistema
    
    ---
    
    - Exemplo strtotime(data)
        
        ```php
        <?php
        
            $data_inicial = '2018-04-24';
            $data_final = '2018-05-15';
        
            //timestamp
                //ela espera um formato de data nesse estilo (ano-mes-dia)
            //01/01/1970
                //js -> milessegundos
                // php -> segundos
        
            $time_inicial = strtotime($data_inicial);
            $time_final = strtotime($data_final);
            echo $data_inicial . ' - ' . $time_inicial; //segundo inicial
            echo '<br>';
            echo $data_final . ' - ' . $time_final; //segundo final
        
            $diferenca_time = abs($time_inicial - $time_final);
            
            echo '<br>';
            echo 'A diferença de segundos entre a data inicial e final é: ' . $diferenca_time;
        
            $segundos_existem_dia = 24 * 60 * 60;
            echo '<br>';
            echo 'Um dia possui '. $segundos_existem_dia . ' segundos.';
        
            $diferenca_dia_datas = $diferenca_time / $segundos_existem_dia;
            echo '<br>';
            echo 'A direfença em dias é: ' . $diferenca_dia_datas;
        ?>
        ```
        

---

- False, Null, Empty
    
    
    | false | true/false | boolean / vazio |
    | --- | --- | --- |
    | null | valor especial | null / valor vazio  |
    | empty | valor especial | valor vazio |
    - False
        
        ```php
        <?php
        
            $funcionario3 = false;
        
            if(empty($funcionario3)){
                echo 'Sim a variavel está vazia';
            }else {
                echo 'Nao a variavel nn está vazia';
            }
        
        ?>
        ```
        
    - Null
        
        ```php
        <?php
            
            $funcionario2 = ''; //nao null
        
            if(is_null($funcionario2)){
                echo 'Sim a variavel é null';
            }else {
                echo 'Nao a variavel nn é null';
            }
        
        ?>
        ```
        
    - Empty
        
        ```php
        <?php
            
            $funcionario1 = null; // vazio
            $funcionario2 = ''; // vazio
        
            if(empty($funcionario1)){
                echo 'Sim a variavel está vazia';
            }else {
                echo 'Nao a variavel nn está vazia';
            }
        
            echo'<br>';
        
            if(empty($funcionario2)){
                echo 'Sim a variavel está vazia';
            }else {
                echo 'Nao a variavel nn está vazia';
            }
        
        ?>
        ```
        

---

- Array
    - Array básico
        - São basicamente variáveis que nos permitem relacionar itens associados a indices
        - Ela é um item q armazena vários outros
        - Existem dois tipos:
            1. **Sequenciais**
                - Sintaxe para criar
                    
                    ```php
                    $lista_frutas = array();
                    // ou 
                    $lista_drutas = [];
                    ```
                    
                - Sintaxe para adicionar
                    
                    ```php
                    $lista_frutas[] = 'valor';
                    ```
                    
                    - Exemplo
                        
                        ```php
                        <?php
                            //criando
                            $lista_frutas = array('Banana', 'Maça', 'Morango', 'Uva', 'Abacate');
                             // ou
                            // $lista_frutas = ['Banana', 'Maça', 'Morango', 'Uva', 'Abacate'];
                            
                        
                            //adicionando
                            $lista_frutas[] = 'Abacaxi';
                        ?>
                        ```
                        
                        - mostrando todos os valores
                            
                            ```php
                            echo '<pre>';
                              var_dump($lista_frutas);
                            echo '</pre>';
                            
                            echo '<hr>';
                            
                            echo '<pre>';
                              print_r($lista_frutas);
                            echo '</pre>';
                            ```
                            
                        - mostrando valores específicos
                            
                            ```php
                            echo $lista_frutas[2];
                            ```
                            
            2. **Associativos**
                - Sintaxe
                    
                    ```php
                    <?php
                    	$lista_frutas = array(
                    	        'a' => 'Banana',
                    	        'b' => 'Maça',
                    	        'x' => 'Morango',
                    	        'z' => 'Uva',
                    	        '2' =>'Abacate');
                    ?>
                    ```
                    
                    - ou
                    
                    ```php
                    <?php
                    	$lista_frutas = [
                    	        'a' => 'Banana',
                    	        'b' => 'Maça',
                    	        'x' => 'Morango',
                    	        'z' => 'Uva',
                    	        '2' =>'Abacate'];
                    ?>
                    ```
                    
                    - Adicionando
                        
                        ```php
                        <?php
                            //criando
                            $lista_frutas = array(
                                'a' => 'Banana',
                                'b' => 'Maça',
                                'x' => 'Morango',
                                'z' => 'Uva',
                                '2' =>'Abacate');
                            
                            //adicionando
                            $lista_frutas['w'] = 'Abacaxi';
                        ?>
                        ```
                        
                    - Mostrando
                        
                        ```php
                        <?php
                            //criando
                            $lista_frutas = array(
                                'a' => 'Banana',
                                'b' => 'Maça',
                                'x' => 'Morango',
                                'z' => 'Uva',
                                '2' =>'Abacate');
                            
                            //adicionando
                            $lista_frutas['w'] = 'Abacaxi';
                        
                        		//mostrando
                            echo $lista_frutas['2'];
                        
                        ?>
                        ```
                        
    
    ---
    
    - Array multidimensional
        - Basicamente são arrays de arrays
            - sendo uma lista dentro da outra
        - Exemplo de como funciona a criação
            
            ```php
            <?php
                
                $lista_coisas = array();
            
                $lista_coisas['frutas'] = [1 => 'Banana', 2 => 'Maça', 3 => 'Morango', 4 => 'Uva'];
            
                $lista_coisas['pessoas'] = array(1 => 'João', 2=> 'José', 3 => 'Maria');
            
                echo '<pre>';
                    print_r($lista_coisas);
                echo '</pre>';
            
            ?>
            ```
            
        - Exemplo de como funciona a recuperação
            
            ```php
            <?php
                echo $lista_coisas['frutas'][3];
                echo '<br>';
                echo $lista_coisas['pessoas'][2];
            ?>
            ```
            
    
    ---
    
    - Pesquisa interna
        - Existem dois comandos nativos do PHP
            - in_array()
                - Ele retorna true ou false para o requerimento
                - Sintaxe
                    
                    ```php
                    in_array('nome_do_elemento', $variavel_array);
                    ```
                    
                - Exemplo
                    
                    ```php
                    <?php
                        $lista_frutas = ['Banana', 'Maçã', 'Morango', 'Uva'];
                        
                        echo '<pre>';
                    	    print_r($lista_frutas);
                        echo '</pre>';
                    
                        $existe = in_array('slamano', $lista_frutas);
                        //verifica se existe oq é pedido
                        //true => 1
                        //false => vazio
                        if($existe) {
                            echo 'O valor pesquisado existe';
                        }else {
                            echo 'O valor pesquisado não existe';
                        }
                    ?>
                    ```
                    
            
            ---
            
            - array_serach()
                - Retorna o indece do valor pesquisado CASO ELE EXISTA
                - Sintaxe
                    
                    ```php
                    array_search('nome_do_elemento', $variavel_array);
                    ```
                    
                - Exemplo
                    
                    ```php
                    <?php
                        
                        $lista_frutas = ['Banana', 'Maçã', 'Morango', 'Uva'];
                        
                        echo '<pre>';
                        print_r($lista_frutas);
                        echo '</pre>';
                    
                        $existe = array_search('Uva', $lista_frutas);
                        //verifica se existe oq é pedido
                        //caso exista => valor do indice
                        //caso não => null => texto vazio
                    
                        if($existe != null) {
                            echo 'O valor pesquisado existe';
                        }else {
                            echo 'O valor pesquisado não existe';
                        }
                        
                    
                    ?>
                    ```
                    
            
            ---
            
            - Pesquisa em array multidimencional
                - Sintaxe
                    
                    ```php
                    in_array('nome_elemento', $array_multi[indice_do_array_requerido])
                    ```
                    
                - Exemplo
                    
                    ```php
                    <?php
                        $lista_frutas = ['Banana', 'Maçã', 'Morango', 'Uva'];
                        $lista_coisas = [
                            'frutas' => $lista_frutas,
                            'pessoas' => ['João', 'Maria']
                        ];
                    
                        echo '<pre>';
                        print_r($lista_frutas);
                        echo '</pre>';
                    
                        echo in_array('Uva', $lista_coisas['frutas']);
                        echo '<br>';
                        echo array_search('Uva', $lista_coisas['frutas']);
                    ?>
                    ```
                    
    
    ---
    
    - Funções array
        
        
        | is_array(array) | verifica se é um array |  |
        | --- | --- | --- |
        | array_keys(array) | retorna todas as chaves de um array |  |
        | sort(array) | ordena um array e reajusta seus indices |  |
        | asort(array) | ordena  um array preservando os indices |  |
        | count(array) | conta a quantidade de elementos de um array |  |
        | array_merge(array) | funde um ou mais arrays | array_merge($array1, $array2) |
        | explode(array) | divide uma string baseada em um delimitador | $string = ‘26/04/2018’);
        explode(’/’, $string); |
        | implode(array) | junta elementos de um array em uma string | $array = [’a’, ‘b’, ‘x’, ‘y’];
        implode(’,’, $array); |
        - —F
            
            ```php
            echo implode('#', str_replace('#', '-', $_POST));
            ```
            

---

- While
    - Sintaxe
        
        ```php
        while (condicao) {
        	operacao
        }
        ```
        
    - Exemplo comum
        
        ```php
        <?php
            $num = 1;
            while ($num <10){
        	    echo "$num <br>";
              $num++;
            } 
        ?>
        ```
        
    - Exemplo com break
        - interrompe completamente o while, pulando pra próxima operação
        
        ```php
        <?php
            $num = 1;
            while (true){
        	    echo "$num <br>";
        	    $num++;
        	    if($num > 100){
        	        break;
        	    }
        		} 
        ?>
        ```
        
    - Exemplo com continue
        - ele pula pro início do mesmo while ignorando o resto do conteúdo desse while
        
        ```php
        <?php
            $num = 1;
        
            while ($num < 10){
            $num++;
            if($num == 2 OR $num == 6){
                continue;    
            }
            echo "$num <br>";
        } 
        ?>
        ```
        

---

- Do while
    - Ele sempre vai ser executado no mínimo uma vez, pois a condição do loop será verificada DEPOIS da execução
    - Sintaxe
        
        ```php
        do {
        
        }while(condicao);
        ```
        
    - Exemplo
        
        ```php
        <?php
            $x = 0;
            do {
                $x++;
                if($x % 2 == 0){
                    continue;
                }
                echo "$x <br>";
        
            }while($x < 20);
        ?>
        ```
        

---

- For
    - Sintaxe
        
        ```php
        for (variavel; condicao; incremento){
        	operacao
        }
        ```
        
    - Exemplo
        
        ```php
        <?php
            for($x = 1; $x <= 10; $x++) {
                echo "$x <br>";
            }
        ?>
        ```
        
        ```php
        <?php
            for($x = 1; true ; $x++) {
                if($x >= 20){
                    break;
                }
                echo "$x <br>";
            }
        ?>
        ```
        

---

- Foreache
    - Sintaxe para os elementos do array
        
        ```php
        foreach($array as $elemento) {
        }
        ```
        
        - ou seja, ele inicia por um array, e o item recebe um item em sequencia do array, então cada vez ele será o próximo item do array
        - Exemplo
            
            ```php
            <?php
                $itens = ['sofá', 'mesa', 'cadeira', 'fogão', 'geladeira'];
            
                echo '<pre>';
                print_r ($itens);
                echo '</pre>';
            
                foreach($itens as $item){
                    echo "$item <br>";
                }
            ?>
            ```
            
    - Sintaxe para os indeces do array
        
        ```php
        foreach($array as $indice => $elemento) {
                echo "Indice = $indice - Elemento = $elemento";
            }
        ```
        
        - Exemplo
            
            ```php
            <?php
                $funcionarios = ['João', 'Maria', 'Júlia'];
                echo '<pre>';
                print_r ($funcionarios);
                echo '</pre>';
                foreach($funcionarios as $idx => $nome) {
                    echo "ID $idx - Nome: $nome <br>";
                }
            ?>
            ```
            
    - Exemplo completo
        
        ```php
        <?php
            $funcionarios = array(
                array('nome' => 'João', 'salario'=> 2500, 'data_nascimento' => "06/03/1970"),
                array('nome' => 'Maria', 'salario'=> 3000),
                array('nome' => 'Júlia', 'salario'=> 2200),
            );
        
            echo '<pre>';
            print_r($funcionarios);
            echo '</pre>';
        
            foreach($funcionarios as $idx => $nome_funcionario){
                foreach($nome_funcionario as $idx2 => $valor){
                    echo "$idx2 - $valor <br />";
                }
                echo "<hr />";
            }
        ?>
        ```
        

---

- Exemplo de laço de repetição com array
    - While
        
        ```php
        $registros = array(
                array('titulo' => 'Título notícia 1', 'conteudo' => 'Conteúdo notícia 1'),
                array('titulo' => 'Título notícia 2', 'conteudo' => 'Conteúdo notícia 2'),
                array('titulo' => 'Título notícia 3', 'conteudo' => 'Conteúdo notícia 3'),
                array('titulo' => 'Título notícia 4', 'conteudo' => 'Conteúdo notícia 4'),
            );
        
            echo '<pre>';
            print_r($registros);
            echo '</pre>';
            echo '<br /><br /><br />';
             $idx = 0;
        
            //count -> conta a quantidade de elementos de array
            echo 'O array possui ' . count($registros) . ' registros';
            
            while ($idx < count($registros)) {
                echo '<h3>' . $registros[$idx]['titulo'] . '</h3>';
                echo '<p>' . $registros[$idx]['conteudo'] . '</p>';
        
                echo '<hr />';
        
                $idx++;
            }
        ```
        
    - Do while
        
        ```php
        <?php
            $registros = array(
                array('titulo' => 'Título notícia 1', 'conteudo' => 'Conteúdo notícia 1'),
                array('titulo' => 'Título notícia 2', 'conteudo' => 'Conteúdo notícia 2'),
                array('titulo' => 'Título notícia 3', 'conteudo' => 'Conteúdo notícia 3'),
                array('titulo' => 'Título notícia 4', 'conteudo' => 'Conteúdo notícia 4'),
            );
        
            echo '<pre>';
            print_r($registros);
            echo '</pre>';
            echo '<br /><br /><br />';
             $idx = 0;
        
            //count -> conta a quantidade de elementos de array
            echo 'O array possui ' . count($registros) . ' registros';
            
            do {
                echo '<h3>' . $registros[$idx]['titulo'] . '</h3>';
                echo '<p>' . $registros[$idx]['conteudo'] . '</p>';
        
                echo '<hr />';
        
                $idx++;
            } while ($idx < count($registros));
        ?>
        ```
        
    - For
        
        ```php
        <?php
            $registros = array(
                array('titulo' => 'Título notícia 1', 'conteudo' => 'Conteúdo notícia 1'),
                array('titulo' => 'Título notícia 2', 'conteudo' => 'Conteúdo notícia 2'),
                array('titulo' => 'Título notícia 3', 'conteudo' => 'Conteúdo notícia 3'),
                array('titulo' => 'Título notícia 4', 'conteudo' => 'Conteúdo notícia 4'),
            );
        
            echo '<pre>';
            print_r($registros);
            echo '</pre>';
            echo '<br /><br /><br />';
             $idx = 0;
        
            //count -> conta a quantidade de elementos de array
            echo 'O array possui ' . count($registros) . ' registros';
            
            for ($idx = 0; $idx < count($registros); $idx++) {
                echo '<h3>' . $registros[$idx]['titulo'] . '</h3>';
                echo '<p>' . $registros[$idx]['conteudo'] . '</p>';
        
                echo '<hr />';
            }
        ?>
        ```
        
    
    ---
    
    - outro exemplo
        
        ```php
        <?php
            $array = array();
        
            while(count($array) <= 5){
                $num = rand(1, 60);
                if(!in_array($num, $array)){
                    $array[] = $num;
                }
            }
            echo '<pre>';
        	    print_r($array);
            echo '</pre>';
        ?>
        ```
        

---

- Requisição
    - Para fazer uma requisição PHP é preciso de algumas coisas
    - <form>
        - por exemplo no <form> a requisição é usando o action, e direcionando para o arquivo .php
            
            ```php
            <form action="nome_arquivo.php">
            </form>
            ```
            
            - ou desse forma
            
            ```php
            <form action="http://localhost/app_help_desk/nome_arquivo.php">
            	<button class="btn btn-lg btn-info btn-block" type="submit">Entrar</button>
            </form>
            ```
            
        - é importante ressaltar que deve se ter um cuidado, é importante atribuir um valor type=”submit” para enviar todo o conteúdo do <form>
    
    ---
    
    - Então para isso é necessário da um name para os inputs se tornando assim uma espécie de variável, onde será guardado o valor inserido nela
    - Por exemplo:
        
        ```php
        <input name="email" type="email" class="form-control" placeholder="E-mail">
        <input name="senha" type="password" class="form-control" placeholder="Senha">
        ```
        
    - obs: o retorno para a requisição NÃO É nosso script PHP, e sim o RESULTADO da interpretação é possível conferir no (fd)

---

- Método de requisição GET
    - Esse método é feito usando a super global $_GET, onde serão colocadas como parâmetro na URL
        - ficando algo assim:
            
            ```php
            http://site.com/seu_programa/login?emil=teste.gmail.com&senha=123123
            ```
            
        - ou seja, ele atribui um ? querendo dizer q o resto pra direita é um parâmetro php
    - Então o super global $_GET recupera esses parâmetros na URL
        - ela é usada como um array então ficaria assim
            
            ```php
            <?php
                print_r($_GET);
                echo '<br>';
                echo $_GET['email']; // name que foi colocado em email
                echo '<br>';
                echo $_GET['senha']; // name que foi colocado em password
            ?>
            ```
            

---

- Método de requisição POST
    - Esse método é feito usando a super global $_POST
        - ele anexa os dados do formulário dentro da própria requisição, tirando assim os dados da URL
    - Então para isso é necessário atribuir o atributo “method” com o elemento “post”
        
        ```php
        <form action="valida_login.php" method="post">
        ```
        
    
    ---
    
    - Então para recuperar esses dados tenha o seguinte exemplo
        
        ```php
        <?php
            print_r($_POST);
            
            echo '<br>';
            echo $_POST['email'];
            echo '<br>';
            echo $_POST['senha'];
        ?>
        ```
        
    
    ---
    
    - Repare que os dados estão sendo enviado junto com o formulário
        
        ![Untitled](PHP%20FULL%209da733f133934045afa87d7ba4e7997d/Untitled%204.png)
        

---

- Verificação de dados
    - Um exemplo de código para verificação
        
        ```php
        <?php
            $usuarios = array(
                array('email' => 'adm@teste.com.br','senha' => '123123'),
                array('email' => 'user@teste.com.br','senha' => '123123'),
            );
        
            foreach($usuarios as $user){
                echo 'Usuario app: ' . $user['email'] . ' / ' . $user['senha'];
                echo '<br>';
                echo 'Usuario form: ' . $_POST['email'] . ' / ' . $_POST['senha'];
                echo '<hr>';
        
            }
        ?>
        ```
        
    - Exemplo completo
        
        ```php
        <?php
            //verificação
            $usuario_autenticado = false;
            $usuarios = array(
                array('email' => 'adm@teste.com.br','senha' => '123123'),
                array('email' => 'user@teste.com.br','senha' => '123123'),
            );
        
            foreach($usuarios as $user){
                if ($user['email'] == $_POST['email'] && $user['senha'] == $_POST['senha']) {
                    $usuario_autenticado = true;
                }
            }
            if ($usuario_autenticado) {
                echo 'Usuário autenticado';
            }else {
                header('Location: index.php?login=erro');
            }
        ?>
        ```
        

---

- Função header()
    - Ela espera uma localização para onde deve ser encaminhada (um desvio), forçando assim para onde ele deve ir
        - e é legal passar um parâmetro
    - Sintaxe
        
        ```php
        header('Location: index.php?login=erro');
        ```
        

---

- isset()
    - Verifica se foi setado um valor
        
        ```php
        if(isset($_GET['login'])){
        	echo($_GET['login'];
        }
        ```
        

---

- —F
    
    ```php
    <?php
      if(isset($_GET['login']) && $_GET['login'] == 'erro')**{**
    ?>
    
        algo deu errado
    
    <?php **}** ?>
    ```
    
    - ou seja, as {} foi aberta em um elemento php e fechada em outra

---

- session
    - A partir de um recurso session a gente irá permitir ou negar acesso
    - É DE EXTERMA IMPORTÂNCIA sempre que for utilizar o session usar o sessions_start() sempre antes de qualquer outra função session ou de qualquer exibição de texto
    - então geralmente utilizamos ela sempre no começo do código php
        - tela1
            
            ```php
            session_start();
                $_SESSION['x'] = 'valor de sessão!';
                print_r($_SESSION);
                echo '<hr>';
                
                echo $_SESSION['y'] . '<br>';
            ```
            
        - tela2
            
            ```php
            <?php
              session_start();
              print_r($_SESSION);
              echo '<br>';
              echo $_SESSION['x'];
            
              $_SESSION['y'] = '1500';
            ?>
            ```
            
            - ou seja, é possível interligar valores de uma página a outra
    - Essas sessões dura por volta de 3 horas no cookie
    
    ---
    
    - Exemplo completo
        - Tela1
            
            ```php
            <?php
            
                session_start();
                
                //verificação
                $usuario_autenticado = false;
                $usuarios = array(
                    array('email' => 'adm@teste.com.br','senha' => '123123'),
                    array('email' => 'user@teste.com.br','senha' => '123123'),
                );
            
                foreach($usuarios as $user){
                    if ($user['email'] == $_POST['email'] && $user['senha'] == $_POST['senha']) {
                        $usuario_autenticado = true;
                    }
                }
                if ($usuario_autenticado) {
                    echo 'Usuário autenticado';
                    $_SESSION['autenticacao'] = true;
                }else {
                    header('Location: index.php?login=erro');
                    $_SESSION['autenticacao'] = false;
                }
            ?>
            ```
            
        - Tela2
            
            ```php
            <?php
              session_start();
              if(!isset($_SESSION['autenticacao']) || $_SESSION['autenticacao'] != true){
                header('Location: index.php?login=naopoassimnao');
              }
            ?>
            
            <html>
            	...
            ```
            

---

- include / include_once
    - include
        - inclusão
        - Em caso de erro o include retorna um warning
            - NÃO é barrada
        - script1
            
            ```php
            inicio | minha rede | vagas
            <hr>
            ```
            
        - script2 (o qual será apresentado)
            
            ```php
            <?php
                include("menu.php");
            ?>
            Conteúdo da página (início)
            ```
            
            - ou
            
            ```php
            <?php
                include "menu.php";
            ?>
            Conteúdo da página (início)
            ```
            
    
    ---
    
    - include_once
        - É feito da mesma forma do include, da mesma sintaxe e tudo mais
        - Porém, se ja tiver outro include_once ele não irá repetir, ela é desconsiderada,
            - então será executado apenas um include_once, será você que irá decidir o como será executado

---

- require / require_once
    - É utilizado para importação de outro arquivo
    - Essa importação não inclui function e constantes
    - Apenas class e interface
    - require
        - inclusão
        - Em caso de erro o require retorna um fatal error
            - ou seja, para
            - é barrada
        - script1
            
            ```php
            inicio | minha rede | vagas
            <hr>
            ```
            
        - script2 (o qual será apresentado)
            
            ```php
            <?php
                require("menu.php");
            ?>
            Conteúdo da página (início)
            ```
            
            - ou
            
            ```php
            <?php
                require "menu.php";
            ?>
            Conteúdo da página (início)
            ```
            
    
    ---
    
    - require_once
        - É feito da mesma forma do require, da mesma sintaxe e tudo mais
        - Porém, se ja tiver outro require_once ele não irá repetir, ela é desconsiderada,
            - então será executado apenas um require_once, será você que irá decidir o como será executado

---

- unset()
    - Serve para excluir indices de QUALQUER array
    - Exemplo
        
        ```php
        <?php
            session_start();
            echo '<pre>';
                print_r($_SESSION);
            echo "</pre><hr>";
        
            unset($_SESSION['x']); //remove apenas se existir
            
            echo '<pre>';
                print_r($_SESSION);
            echo "</pre><hr>";
        
        ?>
        ```
        
        - então caso o indice não exista, ele não retornará um erro, ele apenas irá ignorar

---

- session_destroy()
    - Destroi os indices da super global $_SESSION
    - Exemplo
        
        ```php
        <?php
            session_start();
            session_destroy();
            header('Location: index.php');
        
        ?>
        ```
        
        - ele destroi apenas na próxima execução que não teremos mais acesso as variáveis do session
            - ou seja, mesmo após a execução do session_destroy, nós teremos acessos aos valores das vereáveis de seção, porque a requisição já foi feita
            - então teremos que fazer uma nova requisição para enxergar a a destruição desses valores
    - Então é comum forçar um redirecionamento
        - ou seja, forcar uma nova requisição

---

- fopen() / fwrite() / fclose()
    - Os parâmetros se encontram nessa página
        - [https://www.php.net/manual/en/function.fopen](https://www.php.net/manual/en/function.fopen)
    - fopen()
        - Sintaxe
            
            ```php
            fopen('nome_do_arquivo', parâmetros);
            //ou
            $arquivo = fopen('nome_do_arquivo', parâmetros);
            ```
            
    
    ---
    
    - fwrite()
        - Sintaxe
            
            ```php
            fwrite($arquivo, $texto);
            ```
            
    
    ---
    
    - fclose()
        - Sintaxe
            
            ```php
            fwrite($arquivo);
            ```
            
            - $arquivo esse que tinha sido aberto
    
    ---
    
    - Exemplo final
        
        ```php
        <?php
            echo '<pre>';
            print_r($_POST);
            echo '</pre>';
        
            //tratativa do texto
            $texto = implode('#', str_replace('#', '-', $_POST));
            
            //abrindo o arquivo
            $arquivo = fopen('arquivo', 'a');
            
            //escrevendo o texto
            fwrite($arquivo, $texto);
        
            //fechando o arquivo
            fclose($arquivo);
            
        ?>
        ```
        

---

- PGP_EOL
    - Sigla
        - E = end;
        - O = of;
        - L = line;
    
    ---
    
    - Ela é meio que uma continuação/junção com o fopen(), fwrite(), fclose()
    - Ela basicamente quebra a linha
    - Exemplo final
        
        ```php
        <?php
            echo '<pre>';
            print_r($_POST);
            echo '</pre>';
        
            //tratativa do texto
            $texto = '/*'. implode('#', str_replace('#', '-', $_POST)) . '*/' . PHP_EOL . PHP_EOL;
            
            //abrindo o arquivo
            $arquivo = fopen('arquivo', 'a');
            
            //escrevendo o texto
            fwrite($arquivo, $texto);
        
            //fechando o arquivo
            fclose($arquivo);
            
        ?>
        ```
        

---

- feof()
    - END OF FILE
    - É uma função nativo da PHP
    - Ela percorre até o fim do arquivo
    - Caso ela encontre o final do arquivo ela retorna true
        - caso contrário retorna false
    - Ou seja, ela confere se é a ultima linha
    - Exemplo
        
        ```php
        $arquivo = fopen('arquivo.txt', 'r');
        while(!feof($arquivo)){
        }
        fclose($arquivo); //é IMPORTANTE FECHAR O ARQUIVOO
        ```
        

---

- fgets()
    - Ele recupera o que está naquela linha
        - até o fim,
        - ou se pode colocar a quantidade de bits limite
    - Exemplo
        
        ```php
        $arquivo = fopen('arquivo.txt', 'r');
          while(!feof($arquivo)){
            fgets($arquivo);
          }
          fclose($arquivo);
        ```
        

---

- —F
    - Repare que cada linha foi atribuída a um array
    
    ```php
    $chamados = [];
    
      $arquivo = fopen('arquivo.txt', 'r');
      while(!feof($arquivo)){
        $registro = fgets($arquivo);
        $chamados[] = $registro;
      }
    ```
    

---

- Segurança
    - Se você reparar, os scripts estão sempre ficando no diretório público
    - Então para resolver isso temos as seguintes etapas:
        1. Abra o explorer que tenha os arquivou
            1. ou em
            
            ![Untitled](PHP%20FULL%209da733f133934045afa87d7ba4e7997d/Untitled%205.png)
            
        2. Então crie uma pasta com o nome desejado
            
            ![Untitled](PHP%20FULL%209da733f133934045afa87d7ba4e7997d/Untitled%206.png)
            
        3. Passe para essa pasta os arquivos sigilosos/importantes
            
            ![Untitled](PHP%20FULL%209da733f133934045afa87d7ba4e7997d/Untitled%207.png)
            
        4. Crie um arquivo .php no lugar do qual foi retirado o script importante, com o mesmo nome para não quebrar o script
            
            ![Untitled](PHP%20FULL%209da733f133934045afa87d7ba4e7997d/Untitled%208.png)
            
        5. Então basta criar um script para chamar o arquivo necessário
            
            ```php
            <?php
                require "../../app_help_desk/valida_login.php";
            ?>
            ```
            
        6. Por fim, troque os diretórios do arquivo “arquivo.txt” para seu local de destino
            
            ```php
            <?php
                require "../../app_help_desk/valida_login.php";
            ?>
            
            <?php
            	$arquivo = fopen('../../app_help_desk/arquivo.txt', 'r');
            ?>
            ```
            

---

- Orientação a objeto
    - Introdução
        - Para acessar atributos ou métodos usamos o “->”
        - Para recuperar um atributo usamos o $this
            
            
            | $this | aponta para o próprio objeto |
            | --- | --- |
            | -> | acessa uma variavél externa ou interna |
            - então ficaria algo assim:
                - $this->nomeVariavel
        - Então para deixar claro
            
            
            | $this->nomeVarivel | variável EXTERNA |
            | --- | --- |
            | $this->$nomeVarivel | variável SETADA NA FUNÇÃO |
        - Exemplo de sintaxe
            
            ```php
            <?php
                
                //modelo //primeira letra é sempre maiusculo(boa pratica)
                class Funcionario{
                    //atributos
                    public $nome = 'José';
                    public $telefone = '99999-9999';
                    public $numFilhos = 2; //segunda paralavra com letra maiuscula
            
                    //métodos
                    //segunda paralavra com letra maiuscula
                    function resumirCadFunc() {
                        return "$this->nome possui $this->numFilhos filho(s)";
                    }
            
                    //segunda paralavra com letra maiuscula
                    function modificarNumFilhos($numFilhos) {
                        //afetar um atributo do objeto
                        $this->numFilhos = $numFilhos;
                    }
                }
            
                $y = new Funcionario();
                //a partir dessa variavel temos acesso ao objeto
            
                echo $y->resumirCadFunc();
                $y->modificarNumFilhos(3);
                echo '<br>';
                echo $y->resumirCadFunc();
                echo '<hr>';
            
                $x = new Funcionario();
                echo $x->resumirCadFunc();
                echo '<br>';
                $x->modificarNumFilhos(1);
                echo $x->resumirCadFunc();
            
            ?>
            ```
            
    
    ---
    
    - OO - Pilares de orientação a objeto
        - Abstração (métodos)
            - Métodos Setters/Getters
                - Setters
                    
                    ```php
                    <?php
                    		public $nome = null;
                        public $telefone = null;
                        public $numFilhos = null;
                    
                        //setters
                        function setNome($nome) {
                            $this->nome = $nome;
                        }
                        function setNumFilhos($numFilhos) {
                            $this->numFilhos = $numFilhos;
                        }
                    	?>
                    ```
                    
                - Getters
                    
                    ```php
                    <?php
                    		public $nome = null;
                    		        public $telefone = null;
                    		        public $numFilhos = null;
                    		
                    		        //getters
                    		        function getNome() {
                    		            return $this->nome;
                    		        }
                    		        function getNumFilhos() {
                    		            return $this->numFilhos;
                    		        }
                    	?>
                    ```
                    
                - Exemplo dos dois
                    
                    ```php
                    class Funcionario{
                            //atributos
                            public $nome = null;
                            public $telefone = null;
                            public $numFilhos = null;
                    
                            //setters
                            function setNome($nome) {
                                $this->nome = $nome;
                            }
                            function setNumFilhos($numFilhos) {
                                $this->numFilhos = $numFilhos;
                            }
                            //getters
                            function getNome() {
                                return $this->nome;
                            }
                            function getNumFilhos() {
                                return $this->numFilhos;
                            }
                    }
                    $x = new Funcionario();
                        $x->setNome('Maria');
                        $x->setNumFilhos(0);
                        echo $x->getNome() . ' possui ' . $x->getNumFilhos() . ' filhos';
                    ```
                    
            
            ---
            
            - Método Overloading / sobrecarga
                - É simplesmente uma forma de otimizar o método acima, pois ela resolve o problema de ter que criar inúmeras variáveis
                - Sintaxe __set (setters)
                    
                    ```php
                    function __set($atributo, $valor) {
                                $this->$atributo = $valor;
                            }
                    ```
                    
                - Sintaxe __get (getters)
                    
                    ```php
                    function __get($atributo) {
                                return $this->$atributo;
                            }
                    ```
                    
                - Utilização
                    
                    ```php
                    $y->__set('salario', 3000.00);
                        echo $y->__get('nome') . ' possui ' . $y->__get('numFilhos') . ' filhos, tem o cargo de ' . $y->__get('cargo') . ' e seu salário é de ' . $y->__get('salario');
                    ```
                    
                
                ---
                
                - Exemplo
                    
                    ```php
                    <?php
                        
                        //modelo //primeira letra é sempre maiusculo(boa pratica)
                        class Funcionario{
                            //getters setters (overloading / sobrecarga)
                            function __set($atributo, $valor) {
                                $this->$atributo = $valor;
                            }
                    
                            function __get($atributo) {
                                return $this->$atributo;
                            }
                        }
                    
                        $y = new Funcionario();
                        $y->__set('nome', 'José');
                        $y->__set('numFilhos', 2);
                        $y->__set('cargo', 'Padeiro');
                        $y->__set('salario', 3000.00);
                        echo $y->__get('nome') . ' possui ' . $y->__get('numFilhos') . ' filhos, tem o cargo de ' . $y->__get('cargo') . ' e seu salário é de ' . $y->__get('salario');
                    
                        echo '<hr>';
                    
                        $x = new Funcionario();
                        $x->__set('nome', 'Maria');
                        $x->__set('numFilhos', 0);
                        $x->__set('cargo', 'Cozinheira');
                        $x->__set('salario', 4000.00);
                        echo $x->__get('nome') . ' possui ' . $x->__get('numFilhos') . ' filhos, tem o cargo de ' . $x->__get('cargo') . ' e seu salário é de ' . $x->__get('salario');
                    
                    ?>
                    ```
                    
                    - Resumindo
                        - $y->__set(’nome’, ‘Maria’)
                            - o ‘nome’ é o valor para $atributo, ou seja, falando a grosso modo, é como um nome de variável para o $atributo
                            - e ‘Maria’ é o valor atribuído para ‘nome’
                        
                        ---
                        
                        - $y->__get(’nome’)
                            - ele faz um return de ‘nome’ com o valor atribuído recentemente com a function __set
            
            ---
            
            - Acessando outros métodos
                - Sintaxe
                    
                    ```php
                    $this->outraFuncao(argumento)
                    ```
                    
                - Exemplo
                    
                    ```php
                    <?php
                        
                        //modelo //primeira letra é sempre maiusculo(boa pratica)
                        class Funcionario{
                            public $nome = 'José';
                            public $numFilhos = 2;
                            //getters setters (overloading / sobrecarga)
                            function __get($atributo) {
                                return $this->$atributo;
                            }
                            function resumirCadFunc() {
                                return $this->__get('nome') . " possui " .  $this->__get('numFilhos') . " filho(s)";
                            }
                        }
                        $y = new Funcionario();
                        echo $y->resumirCadFunc();
                    ?>
                    ```
                    
                    - Nesse exemplo caso você não tenha entendido o motivo do __get conseguir fazer essa função temos a seguinte explicação:
                        - você dá a ele o argumento ‘nome’, dele ele retorna para o $this
                        - então o $this aponta para o nome, então
                        - $this->nome
                        - e nome é a variável externa que tem o valor de ‘José’
            
            ---
            
            - __construct()/__destruct()
                - __construct()
                    - É ativado na instancia do objeto, podendo usar objetos privados e protegidos
                        - podendo ou não receber parâmentros
                    - Exemplo
                        
                        ```php
                        function __construct($nome)
                                {
                                    echo 'Objeto iniciado';
                                    $this->nome = $nome;
                                }
                        ```
                        
                
                ---
                
                - __destruct()
                    - É executado automaticamente assim que um objeto é removido/movido da memória
                    - Ela é ativada também na finalização do script do backend
                    - Exemplo
                        
                        ```php
                        function __destruct()
                                {
                                    echo 'Objeto removido';
                                }
                        ```
                        
                
                ---
                
                - Exemplo geral
                    
                    ```php
                    <?php
                        class Pessoa
                        {
                            public $nome = null;
                    
                            function __construct($nome)
                            {
                                echo 'Objeto iniciado';
                                $this->nome = $nome;
                            }
                    
                            function __destruct()
                            {
                                echo 'Objeto removido';
                            }
                    
                            function __get($atributo)
                            {
                                return $this->$atributo;
                            }
                            function correr(){
                                return $this->__get('nome') . ' esta correndo';
                            }
                    
                        }
                        $pessoa = new Pessoa('Jorge');
                        echo '<br /> Nome: ' . $pessoa->__get('nome');
                        echo '<br /> ' . $pessoa->correr();
                        echo '<br />';
                        unset($pessoa);
                    ?>
                    ```
                    
        
        ---
        
        - Herança (extends/junção)
            - É possível linkar uma função com outra, por exemplo
                - existem duas functions, e nelas temos 5 elementos, porém 3 desses elementos existem nos dois objetos, então o **extends** juntará os dois objetos
            - Sintaxe
                
                ```php
                class NomeObjeto extends NomeDoObjetoHeranca
                
                ```
                
            - Exemplo
                
                ```php
                <?php
                
                    class Carro extends Veiculo
                    {
                        public $teto_solar = true;
                
                        function abrirTetoSoalr()
                        {
                            echo 'Abrir teto solar';
                        }
                        function alterarPosicaoVolante()
                        {
                            echo 'Alterar posição volante';
                        }
                    }
                    class Moto extends Veiculo
                    {
                        public $contraPesoGuidao = true;
                
                        function empinar()
                        {
                            echo 'Empirar';
                        }
                    }
                    class Veiculo
                    {
                        public $placa = null;
                        public $cor = null;
                        function acelerar()
                        {
                            echo 'Acelerar';
                        }
                    }
                
                    $carro = new Carro();
                    $moto = new Moto();
                
                    echo '<pre>';
                        print_r($carro);
                        echo '<br>';
                        print_r($moto);
                    echo '</pre>';
                ?>
                ```
                
            - Exemplo final
                
                ```php
                <?php
                
                    class Carro extends Veiculo
                    {
                        public $teto_solar = true;
                
                        function __construct($placa, $cor)
                        {
                            $this->placa = $placa;
                            $this->cor = $cor;
                        }
                
                        function abrirTetoSoalr()
                        {
                            echo 'Abrir teto solar';
                        }
                        function alterarPosicaoVolante()
                        {
                            echo 'Alterar posição volante';
                        }
                    }
                    class Moto extends Veiculo
                    {
                        public $contraPesoGuidao = true;
                
                        function __construct($placa, $cor)
                        {
                            $this->placa = $placa;
                            $this->cor = $cor;
                        }
                
                        function empinar()
                        {
                            echo 'Empirar';
                        }
                    }
                    class Veiculo
                    {
                        public $placa = null;
                        public $cor = null;
                        function acelerar()
                        {
                            echo 'Acelerar';
                        }
                        function freiar()
                        {
                            echo 'Freiar';
                        }
                    }
                
                    $carro = new Carro('ABC1234', 'Branco');
                    $moto = new Moto('DEF1122', 'Preto');
                
                    echo '<pre>';
                        print_r($carro);
                        echo '<br>';
                        print_r($moto);
                    echo '</pre>';
                    echo '<hr>';
                    $carro->abrirTetoSoalr();
                    echo '<br>';
                    $carro->acelerar();
                    echo '<br>';
                    $carro->freiar();
                
                    echo '<hr>';
                    
                    $moto->empinar();
                    echo '<br>';
                    $moto->acelerar();
                    echo '<br>';
                    $moto->freiar();
                ?>
                ```
                
        
        ---
        
        - Polimorfismo (sobrescrita)
            - Sobrescrita de métodos
            - Então ele reescreve por cima de alguma function filho, ou seja,
                - o método que recebe o atribulo extends vai sobrescrever a herança q ele receberá
            - Exemplo
                
                ```php
                <?php
                use Veiculo as GlobalVeiculo;
                    class Carro extends Veiculo
                    {
                        public $teto_solar = true;
                
                        function __construct($placa, $cor)
                        {
                            $this->placa = $placa;
                            $this->cor = $cor;
                        }
                
                        function abrirTetoSoalr()
                        {
                            echo 'Abrir teto solar';
                        }
                        function alterarPosicaoVolante()
                        {
                            echo 'Alterar posição volante';
                        }
                    }
                    class Caminhao extends Veiculo
                    {
                    }
                    class Moto extends Veiculo
                    {
                        public $contraPesoGuidao = true;
                
                        function __construct($placa, $cor)
                        {
                            $this->placa = $placa;
                            $this->cor = $cor;
                        }
                
                        function empinar()
                        {
                            echo 'Empirar';
                        }
                        function trocarMarcha()
                        {
                            echo 'Desengatar empreagem com o mão e engatar com marcha com a pé';
                        }
                    }
                    class Veiculo
                    {
                        public $placa = null;
                        public $cor = null;
                        function acelerar()
                        {
                            echo 'Acelerar';
                        }
                        function freiar()
                        {
                            echo 'Freiar';
                        }
                        function trocarMarcha()
                        {
                            echo 'Desengatar empreagem com o pé e engatar com marcha com a mão';
                        }
                    }
                    $carro = new Carro('ABC1234', 'Branco');
                    $moto = new Moto('DEF1122', 'Preto');
                    $caminhao = new Caminhao('DEF1122', 'Preto');
                
                    $carro->trocarMarcha();
                    echo '<br />';
                    $moto->trocarMarcha();
                    echo '<br />';
                    $caminhao->trocarMarcha();
                ?>
                ```
                
        
        ---
        
        - Encapsulamento (segurança)
            - É um meio de segurança onde iremos proteger nossos objetos
            
            ---
            
            - public
                - Dá um acesso público para a aplicação
                - Pode ser herdado e alterado no objeto filho
            
            ---
            
            - protected
                - Restringe o acesso para a aplicação
                - É possível acessar ou modificar esse método a partir de funções
                    - caso ela seja publica
                - Exemplo
                    
                    ```php
                    <?php
                    	protected $sobrenome = 'Silva';
                    	public function getNome()
                    	  {
                    	      return $this->sobrenome;
                    	  }
                    	echo $pai->getNome();
                    ?>
                    ```
                    
                - Pode ser herdado e alterado no objeto filho
            
            ---
            
            - private
                - Restringe o acesso para a aplicação
                - É possível acessar ou modificar esse método a partir de funções
                    - caso ela seja publica
                - Exemplo
                    
                    ```php
                    <?php
                    	private $nome = 'Jorge';
                    	public function getNome()
                    	  {
                    	      return $this->nome;
                    	  }
                    	echo $pai->getNome();
                    ?>
                    ```
                    
                - Porém ele tem uma peculiaridade
                    - Em uma function extends ou função herança ele não poderá ser acessado
            
            ---
            
            - Em ponto de vista de aplicação, “protected” e “private” não tem diferenças, mas cada um tem sua peculiaridade
            - Caso você esteja utilizando o método __get() ou __set(), ele utilizará automaticamente para recuperar ou modificar dados private ou protected
            - Exemplo com o método __get()
                
                ```php
                <?php
                
                    class Pai
                    {
                        private $nome = 'Jorge';
                        protected $sobrenome = 'Silva';
                        public $humor = 'Feliz';
                
                        public function __get($attr)
                        {
                            return $this->$attr;
                        }
                        public function __set($attr, $value)
                        {
                            $this->$attr = $value;
                        }
                
                    }
                    $pai = new Pai();
                    
                    echo $pai->nome;
                
                ?>
                ```
                
            
            ---
            
            - Exemplo com o método __set()
                
                ```php
                <?php
                
                    class Pai
                    {
                        private $nome = 'Jorge';
                        protected $sobrenome = 'Silva';
                        public $humor = 'Feliz';
                
                        public function __get($attr)
                        {
                            return $this->$attr;
                        }
                        public function __set($attr, $value)
                        {
                            $this->$attr = $value;
                        }
                
                    }
                    $pai = new Pai();
                    
                    
                    echo $pai->nome;
                    echo '<br>';
                    echo $pai->nome = 'Allam';
                    echo '<br>';
                    echo $pai->nome;
                
                ?>
                ```
                
            
            ---
            
            - É possível usar métodos públicos para acessar outros privados
                
                ```php
                private function executarMania()
                        {
                            echo 'Assobiar';
                        }
                
                protected function responder()
                        {
                            echo 'Oi';
                        }
                public function executarAcao()
                        {
                            $x = rand(1, 10);
                            if($x <= 5){
                                $this->executarMania();
                            }else{
                                $this->responder();
                            }
                        }
                ```
                
            
            ---
            
            - Herança
                - get_claass_methods()
                    - Mostra todos os métodos/funções dentro do objeto
                        
                        ```php
                        <?php
                        use Pai as GlobalPai;
                            class Pai
                            {
                                private $nome = 'Jorge';
                                protected $sobrenome = 'Silva';
                                public $humor = 'Feliz';
                                public function getAtributo($attr)
                                {
                                    return $this->$attr;
                                }
                                
                                public function setAtributo($attr, $value)
                                {
                                    $this->$attr = $value;
                                }
                            }
                            class Filho extends GlobalPai{
                        
                            }
                            $filho = new Filho();
                            
                            echo'<pre>';
                            print_r(get_class_methods($filho));
                            echo'<pre>';
                        
                        ?>
                        ```
                        
                    - Resultado
                        
                        ```php
                        Array
                        (
                            [0] => getAtributo
                            [1] => setAtributo
                        )
                        ```
                        
                
                ---
                
                - Possibilidades no objeto de herança filho
                    - Caso os objetos mágicos __set e __get estiverem no objeto filho, será possível acessar apenas:
                        - É possível alterar um objeto public
                        - É possível alterar um objeto protected
                        - Não é possível alterar um objeto private
                            - porém é possível altera-lo
                    - Caso tenha percebido, os métodos protected e private são diferentes, sendo o protected podendo ser herdado, porém ele não será visível, pois ele ainda continuará sendo um método protected
                    
                    ```php
                    <?php
                    
                    use Pai as GlobalPai;
                    
                        class Pai
                        {
                            private $nome = 'Jorge';
                            protected $sobrenome = 'Silva';
                            public $humor = 'Feliz';
                        }
                        
                        class Filho extends GlobalPai{
                            public function getAtributo($attr)
                            {
                                return $this->$attr;
                            }
                            
                            public function setAtributo($attr, $value)
                            {
                                $this->$attr = $value;
                            }
                        }
                        $filho = new Filho();
                        //é possível alterar um objeto public
                        echo'<pre>';
                        print_r($filho);
                        echo'<pre>';
                        echo $filho->getAtributo('humor');
                        $filho->setAtributo('humor', 'Triste');
                        echo '<br>';
                        echo $filho->getAtributo('humor');
                    
                        echo '<hr>';
                        
                        //é possível alterar um objeto protected
                        echo'<pre>';
                        print_r($filho);
                        echo'<pre>';
                        echo $filho->getAtributo('sobrenome');
                        $filho->setAtributo('sobrenome', 'Pereira');
                        echo '<br>';
                        echo $filho->getAtributo('sobrenome');
                    
                        echo '<hr>';
                        
                        //não é possível alterar um objeto private
                        echo'<pre>';
                        print_r($filho);
                        echo'<pre>';
                        echo $filho->getAtributo('nome');
                    
                        //porém é possivel altera-lo
                        $filho->setAtributo('nome', 'Santos');
                        echo'<pre>';
                        print_r($filho);
                        echo'<pre>';
                        echo $filho->getAtributo('nome');
                    
                    ?>
                    ```
                    
                
                ---
                
                - Possibilidades no objeto Pai para o objeto herança
                    - Caso os objetos mágicos __set e __get estiverem no objeto pai, e for passado de herança para o objeto filho, será possível acessa-los
                        - (objetos: public, protected e private)
                    
                    ```php
                    <?php
                    use Pai as GlobalPai;
                    
                        class Pai
                        {
                            private $nome = 'Jorge';
                            protected $sobrenome = 'Silva';
                            public $humor = 'Feliz';
                            public function getAtributo($attr)
                            {
                                return $this->$attr;
                            }
                            
                            public function setAtributo($attr, $value)
                            {
                                $this->$attr = $value;
                            }
                        }
                        
                        class Filho extends GlobalPai{
                        }
                        $filho = new Filho();
                        //é possível alterar um objeto public
                        echo'<pre>';
                        print_r($filho);
                        echo'<pre>';
                        echo $filho->getAtributo('nome');
                        echo '<br>';
                        echo $filho->getAtributo('sobrenome');
                        echo '<br>';
                        echo $filho->getAtributo('humor');
                    
                    ?>
                    ```
                    
                    - Então se for alterado alguma coisa a partir da herança filho pelo método __set ou por outro método, ele será alterado no objeto Pai
                
                ---
                
                - Debug
                    - Como o a function __contruct() é iniciada na instancia do objeto, ele é uma ótima escolha para debug
                    - Pois ele conseguirá acessar todos os métodos (public, private, protected)
                    - Exemplo
                        
                        ```php
                        <?php
                        use Pai as GlobalPai;
                            class Pai
                            {
                                private $nome = 'Jorge';
                                protected $sobrenome = 'Silva';
                                public $humor = 'Feliz';
                                public function getAtributo($attr)
                                {
                                    return $this->$attr;
                                }
                                public function setAtributo($attr, $value)
                                {
                                    $this->$attr = $value;
                                }
                                private function executarMania()
                                {
                                    echo 'Assobiar';
                                }
                                protected function responder()
                                {
                                    echo 'Oi';
                                }
                                public function executarAcao()
                                {
                                    $x = rand(1, 10);
                                    if($x <= 5){
                                        $this->executarMania();
                                    }else{
                                        $this->responder();
                                    }
                                }
                            }
                            class Filho extends GlobalPai{
                                public function __construct()
                                {
                                echo'<pre>';
                                print_r(get_class_methods($this));
                                echo'<pre>';
                                }
                            }
                            $filho = new Filho();
                        ?>
                        ```
                        
                    - Então, internamente ele tem acesso ao métodos
                    - Já a aplicação possuí apenas acesso para métodos públicos
                
                ---
                
                - Possibilidade gerais
                    - Como existem funções que utilizam métodos privados ou protegidos de um objeto pai
                    - Ao utiliza-lo no objeto filho o PHP tem a inteligência de utilizar a função protegida/privada do objeto pai no objeto filho
                    - Exemplos
                        - Usando
                            
                            ```php
                            <?php
                            use Pai as GlobalPai;
                                class Pai
                                {
                                    private $nome = 'Jorge';
                                    protected $sobrenome = 'Silva';
                                    public $humor = 'Feliz';
                                    public function getAtributo($attr)
                                    {
                                        return $this->$attr;
                                    }
                                    
                                    public function setAtributo($attr, $value)
                                    {
                                        $this->$attr = $value;
                                    }
                                    private function executarMania()
                                    {
                                        echo 'Assobiar';
                                    }
                            
                                    protected function responder()
                                    {
                                        echo 'Oi';
                                    }
                                    public function executarAcao()
                                    {
                                        $x = rand(1, 10);
                                        if($x <= 5){
                                            $this->executarMania();
                                        }else{
                                            $this->responder();
                                        }
                                    }
                                }
                                class Filho extends GlobalPai{
                                    public function __construct()
                                    {
                                    echo'<pre>';
                                    print_r(get_class_methods($this));
                                    echo'<pre>';
                                    }
                                }
                                $filho = new Filho();
                            
                                $filho->executarAcao();
                            
                            ?>
                            ```
                            
                        - Resultado
                            
                            ```php
                            Array
                            (
                                [0] => __construct
                                [1] => getAtributo
                                [2] => setAtributo
                                [3] => responder
                                [4] => executarAcao
                            )
                            Oi
                            ```
                            
                            ```php
                            Array
                            (
                                [0] => __construct
                                [1] => getAtributo
                                [2] => setAtributo
                                [3] => responder
                                [4] => executarAcao
                            )
                            Assobiar
                            ```
                            
                    
                    ---
                    
                    - Ou seja, é possível acessar qualquer objeto de seu pai a partidor do filho, mesmo o filho não tendo herdado todos os métodos
                    - Então nesse contexto, ele utilizará apenas as funções do objeto pai, mesmo existindo essa função no objeto filho
                    
                    <aside>
                    ❗ Porém é importante dizer que isso não será aplicado ao método protected, pois ele pode ser sobreposto no objeto filho
                    Então ele não será usado mais a função do objeto pai, mas sim do objeto filho
                    
                    </aside>
                    
    
    ---
    
    - Atributos e métodos estáticos
        - É possível acessar métodos e atributos estáticos sem a iniciação de uma instancia do objeto
        - Porém não é possível acessar atributos e métodos comuns a partir disso
        - Exemplo
            - não é necessário utilizar
                - $var = new Objeto();
            - simplesmente utilize
                - Objeto::$var;
            
            ```php
            <?php
                class Exemplo {
                    public static $atributo1 = 'Atributo estático';
                    public $atributo2 = 'Atributo normal';
            
                    public static function metodo1()
                    {
                        echo 'Método estático';
                    }
            
                    public function metodo2()
                    {
                        echo 'Método normal';
                    }
                }
            
                //$x = new Exemplo();
                echo Exemplo::$atributo1;
                echo '<br>';
                Exemplo::metodo1();
            ?>
            ```
            
        
        ---
        
        - Não é possível acessar atributos utilizando o ‘→’ a partir de uma instancia
        - Exemplo de erro
            
            ```php
            <?php
                class Exemplo {
                    public static $atributo1 = 'Atributo estático';
                    public $atributo2 = 'Atributo normal';
            
                    public static function metodo1()
                    {
                        echo 'Método estático';
                    }
            
                    public function metodo2()
                    {
                        echo 'Método normal';
                    }
                }
            
                $x = new Exemplo();
                $x->$atributo1;
            
            ?>
            ```
            
        
        ---
        
        - Não é possível utilizar o ‘$this’ em métodos
        - Exemplo de erro
            
            ```php
            <?php
                class Exemplo {
                    public static $atributo1 = 'Atributo estático';
                    public $atributo2 = 'Atributo normal';
            
                    public static function metodo1()
                    {
                        $this->atributo1;
                        echo 'Método estático';
                    }
            
                    public function metodo2()
                    {
                        echo 'Método normal';
                    }
                }
                Exemplo::metodo1();
            ?>
            ```
            
        
    
    ---
    
    - Interfaces
        - Ela iniciará penas os métodos, atributos não poderão ser inicializado
        - Sua sintaxe é semelhante a de uma class, sendo
            
            ```php
            interface nomeInterface{
                public function exemplo();
                public function outroExemplo();
            }
            ```
            
        - Perceba que ela apenas iniciará os métodos, e seu escopo será definido posteriormente fora da interface
        
        ---
        
        - Então para implementar a interface em uma class é feito da seguinte forma:
        - Sintaxe
            
            ```php
            interface nomeInterface{
                public function exemplo();
                public function outroExemplo();
            }
            class ObjetoTeste implements nomeInterface
            {
            
            }
            ```
            
        - Porém se for deixado dessa maneira, acontecerá um fatal error, pois não foi implementado conteúdo ao(s) método(s)
        - Então
            
            ```php
            interface nomeInterface{
                public function exemplo();
                public function outroExemplo();
            }
            class ObjetoTeste implements nomeInterface
            {
                public function exemplo()
                {
                    echo 'Exemplo';
                }
                public function outroExemplo()
                {
                    echo 'Outro exemplo';
                }
            }
            ```
            
        
        <aside>
        ❗ É bom relembrar que, não faz muito sentido implementar na interface métodos private ou protected
        
        </aside>
        
        - Exemplo complementar
            
            ```php
            <?php
            
                interface equipamentoEletronicoInterface{
                    public function ligar();
                    public function desligar();
                }
            
                class Geladeira implements equipamentoEletronicoInterface
                {
                    public function abrirPorta()
                    {
                        echo 'Abrir a porta';
                    }
                    public function ligar()
                    {
                        echo 'Ligar';
                    }
                    public function desligar()
                    {
                        echo 'Desligar';
                    }
            
                }
            
                class TV implements equipamentoEletronicoInterface
                {
                    public function trocarCanal()
                    {
                        echo 'Trocar canal';
                    }
                    public function ligar()
                    {
                        echo 'Ligar';
                    }
                    public function desligar()
                    {
                        echo 'Desligar';
                    }
                }
            
                $x = new Geladeira();
                $y = new TV();
            ?>
            ```
            
        
        ---
        
        - Para implementar mais de uma interface basta colocar uma virgula(,) e colocar o próximo nome da interface
        - Sintaxe
            
            ```php
            class Humano implements Mamiferointerface, TerrestreInterface{
                    [...]
                }
            ```
            
        - Exemplo
            
            ```php
            <?php
                interface Mamiferointerface{
                    public function respirar();
                }
                interface TerrestreInterface{
                    public function andar();
                }
                interface AquaticoInterface{
                    public function nadar();
                }
            
                class Humano implements Mamiferointerface, TerrestreInterface
                {
                    public function andar()
                    {
                        echo 'andar';
                    }
            
                    public function respirar()
                    {
                        echo 'respirar';
                    }
                    public function conversar()
                    {
                        echo 'conversar';
                    }
                }
            
                class Baleia implements Mamiferointerface, AquaticoInterface
                {
                    public function respirar()
                    {
                        echo 'respirar';
                    }
                    public function nadar()
                    {
                        echo 'nadar';
                    }
                    protected function esguichar()
                    {
                        echo 'esguichar';
                    }
                }
            ?>
            ```
            
        
        ---
        
        - Herança de interface
            - interface também pode receber herança de outra interface, então
            - Sintaxe
                
                ```php
                interface Primeiro
                {
                    public function ExemploPrimeiro();
                }
                interface Segunda extends Primeiro
                {
                    public function ExemploSegundo();
                }
                class Codigo implements Segunda
                {
                    public function ExemploPrimeiro()
                    {
                        echo 'pri';
                    }
                    public function ExemploSegundo()
                    {
                        echo 'seg';
                    }
                }
                ```
                
            - Perceba que é obrigatório utilizar os métodos da interface e a herança que ela recebeu
            - Exemplo concreto
                
                ```php
                <?php
                    interface AnimalInterface
                    {
                        public function comer();
                    }
                    interface AveInterface extends AnimalInterface
                    {
                        public function voar();
                    }
                    class Papagaio implements AveInterface
                    {
                        public function voar()
                        {
                            echo 'voar';
                        }
                        public function comer()
                        {
                            echo 'comer';
                        }
                    }
                ?>
                ```
                
            
        

---

- Namespaces
    - É usado para “separar”/”isolando” métodos com o mesmo nome
    - Exemplo
        
        ```php
        namespace A;
        quadrado()
        {
        }
        
        /*a partir daqui o quadrado selecionado
        sem nenhum parâmetro receberá o namespace B*/
        
        namespace B;
        quadrado()
        {
        }
        ```
        
    - Então para acessar outro namespace é necessário utilizar o \
    - Sintaxe
        
        ```php
        namespace A;
        quadrado()
        {
        }
        namespace B;
        quadrado()
        {
        }
        
        $c = new \A\quadrado();
        ```
        
    - Exemplos
        
        ```php
        <?php
        
            namespace A;
            class Cliente
            {
                public $nome = 'Jorge';
                public function __get($attr)
                {
                    return $this->$attr;
                }
            }
            namespace B;
            class Cliente
            {
                public $nome = 'Jamilton';
                public function __get($attr)
                {
                    return $this->$attr;
                }
            }
            $c = new \A\Cliente();
            print_r($c);
            echo $c->__get('nome');
        ?>
        ```
        
        - É possível implementar uma interface de outro namespace
            
            ```php
            <?php
            
                namespace A;
                class Cliente implements \B\CadastroInterface
                {
                    public $nome = 'Jorge';
            
                    public function __contruction()
                    {
                        echo '<pre>';
                        print_r(get_class_methods($this));
                        echo '</pre>';
                    }
            
                    public function __get($attr)
                    {
                        return $this->$attr;
                    }
                    public function salvar()
                    {
                        echo 'salvar';
                    }
                    public function remover()
                    {
                        echo 'remover';
                    }
                }
                interface CadastroInterface
                {
                    public function salvar();
                }
            
                namespace B;
                class Cliente implements \A\CadastroInterface
                {
                    public $nome = 'Jamilton';
            
                    public function __contruction()
                    {
                        echo '<pre>';
                        print_r(get_class_methods($this));
                        echo '</pre>';
                    }
            
                    public function __get($attr)
                    {
                        return $this->$attr;
                    }
                    public function remover()
                    {
                        echo 'remover';
                    }
                    public function salvar()
                    {
                        echo 'salvar';
                    }
                }
                interface CadastroInterface
                {
                    public function remover();
                }
            
                $c = new \b\Cliente();
                print_r($c);
                echo $c->__get('nome');
            ?>
            ```
            

---

- Packagist
    - [https://packagist.org](https://packagist.org/)
    - É usado para utilização de bibliotecas

---

- Bibliotecas
    - Relembrando que na hora da importação de uma biblioteca utilizando o require, importará apenas class e interface
    - Utilizando a biblioteca
        
        ```php
        <?php
            require "../Biblioteca/Lib1/lib1.php";
            require "../Biblioteca/Lib2/lib2.php";
        
            use A\Cliente;
        
            $c = new Cliente();
            echo '<pre>';
            print_r($c);
            echo '</pre>';
            echo $c->__get('nome');
        ?>
        ```
        
    
    ---
    
    - Renomeando um use de uma biblioteca
        
        ```php
        <?php
            require "../Biblioteca/Lib1/lib1.php";
            require "../Biblioteca/Lib2/lib2.php";
        
            use A\Cliente as C1;
            use B\Cliente;
        
            $c = new C1();
            echo '<pre>';
            print_r($c);
            echo '</pre>';
            echo $c->__get('nome');
        ?>
        ```
        
    

---

- Tratamento de erros
    - try
        - É possível utilizar quantos try forem necessário
        - Ele transformará um fatal error em um error, podendo assim ser tratado de alguma forma
        - Ele precisa ser utilizado com pelo menos o catch ou o finally, ou seja, é possível utilizar os dois juntos, ou apenas um deles
    
    ---
    
    - catch()
        - Sintaxe
            
            ```php
            catch(Error $var)
            {
            		//conteúdo
            }
            ```
            
        - É importante sitar que, só será executado o catch somente se ocorrer um Error
        - Exemplo
            
            ```php
            <?php
            
                try{
                    echo '<h3> *** try *** </h3>';
                    $sql = 'Select * from clientes';
                    mysql_query($sql);
                }
                catch(Error $e)
                {
                    echo '<h3> *** catch *** </h3>';
                    echo '<p style="color: red">', $e, '</p>';
                }
                finally{
                    echo '<h3> *** finally *** </h3>';
                }
            ?>
            ```
            
    
    ---
    
    - finally
        - Caso tenho o try e o catch é opcional a utilização do finally
        - Amostra
            
            ```php
            <?php
            
                try{
                    echo '<h3> *** try *** </h3>';
                    $sql = 'Select * from clientes';
                    mysql_query($sql);
                }
                catch(Error $e)
                {
                    echo '<h3> *** catch *** </h3>';
                    echo '<p style="color: red">', $e, '</p>';
                }/*
                finally{
                    echo '<h3> *** finally *** </h3>';
                }*/
            ?>
            ```
            
    
    ---
    
    - throw
        - É usado para efetuar um erro
            
            ```php
            <?php
            
                try{
                    echo '<h3> *** try *** </h3>';
                    /* $sql = 'Select * from clientes';
                    mysql_query($sql); */
                    if(!file_exists('require_arquivo_a.php'))
                    {
                        throw new Exception('O arquivo deveria estar disponível as '. date('d/m/Y H:i:s').' mas não estava, porém vamos seguir');
                    }
                }
                catch(Error $e)
                {
                    echo '<h3> *** catch Error *** </h3>';
                    echo '<p style="color: red">'. $e . '</p>';
                }
                catch(Exception $e)
                {
                    echo '<h3> *** catch Exception *** </h3>';
                    echo '<p style="color: red">'. $e . '</p>';
            
                }
                finally{
                    echo '<h3> *** finally *** </h3>';
                }
            ?>
            ```
            
        - É possível utilizar Error no lugar de Exception também
    
    ---
    
    - Erros customizados
        
        ```php
        <?php
        
            class MinhaExceptionCustomizada extends Exception
            {
                private $erro = '';
                
                public function __construct($erro)
                {
                    $this->erro = $erro;
                }
                public function exibirMensagemErroCustomizada()
                {
                    return $this->erro;
                }
            }
        
            try{
                throw new MinhaExceptionCustomizada('Esse é um erro de teste');
            }
            catch(MinhaExceptionCustomizada $e)
            {
                echo $e->exibirMensagemErroCustomizada();
            }
        ?>
        ```
        
        - Perceba que é possível utilizar herdado métodos nativos do php
        - Então a partir disso é simples customizar erros

---

- Produção do App Send Email
    - Introdução/Recursos
        - Para a criação dessa aplicação utilizaremos as seguintes coisas:
            - Código
                
                ```php
                <html>
                	<head>
                		<meta charset="utf-8" />
                    	<title>App Mail Send</title>
                
                    	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
                
                	</head>
                
                	<body>
                
                		<div class="container">  
                
                			<div class="py-3 text-center">
                				<img class="d-block mx-auto mb-2" src="logo.png" alt="" width="72" height="72">
                				<h2>Send Mail</h2>
                				<p class="lead">Seu app de envio de e-mails particular!</p>
                			</div>
                
                      		<div class="row">
                      			<div class="col-md-12">
                  				
                					<div class="card-body font-weight-bold">
                						<form>
                							<div class="form-group">
                								<label for="para">Para</label>
                								<input type="text" class="form-control" id="para" placeholder="joao@dominio.com.br">
                							</div>
                
                							<div class="form-group">
                								<label for="assunto">Assunto</label>
                								<input type="text" class="form-control" id="assunto" placeholder="Assundo do e-mail">
                							</div>
                
                							<div class="form-group">
                								<label for="mensagem">Mensagem</label>
                								<textarea class="form-control" id="mensagem"></textarea>
                							</div>
                
                							<button type="submit" class="btn btn-primary btn-lg">Enviar Mensagem</button>
                						</form>
                					</div>
                				</div>
                      		</div>
                      	</div>
                
                	</body>
                </html>
                ```
                
            
            ---
            
            - Imagem
                - Para esse recurso, você poderá utilizar de qualquer imagem de seu interesse
                - Recebendo a seguinte nomenclatura:
                    - logo.png
    
    ---
    
    - Ação/Execução
        - action
            - De início devemos utilizar o atributo ‘action’ dentro do form para o envio dos dados passar por um arquivo .php, para ser decidido o que deverá acontecer com esse form, junto com o atributo ‘method’, com o parâmetro ‘post’ para o envio de dados do programa, ficando assim:
                
                ```php
                <form action="processa_envio.php" method="post">
                ```
                
            - Então deverá ser criado um novo arquivo chamado ‘processa_envio.php’
        
        ---
        
        - name
            - Depois devemos nomear com o ‘name’ cada input:
                
                ```php
                <input name="para" type="text" class="form-control" id="para" placeholder="joao@dominio.com.br">
                <input name="assunto" type="text" class="form-control" id="assunto" placeholder="Assundo do e-mail">
                <textarea name="mensagem" class="form-control" id="mensagem"></textarea>
                ```
                
        
        ---
        
        - 1º teste
            - Para nosso 1º teste vamos escrever no novo arquivo criado:
                
                ```php
                <?php
                    print_r($_POST);
                ```
                
            - Caso esteja aparecendo as informações corretamente, iremos proceguir
        
        ---
        
        - class Mensagem
            - Agora iremos iniciar uma function para o processamento dos dados
            - Nela iremos colocar 3 variáveis que servirão de base para cada um dos inputs
            - Atribuiremos o método __get e __set
            - Então iniciaremos a instancia de um objeto para a utilização do mesmo
            - Assim setaremos com o método __set cada uma das variáveis
                
                ```php
                <?php
                    class Mensagem
                    {
                        private $para = null;
                        private $assunto = null;
                        private $mensagem = null;
                
                        public function __get($attr)
                        {
                            return $this->$attr;
                        }
                
                        public function __set($attr, $valor)
                        {
                            $this->$attr = $valor;
                        }
                
                    }
                    $mensagem = new Mensagem();
                    $mensagem->__set('para', $_POST['para']);
                    $mensagem->__set('assunto', $_POST['assunto']);
                    $mensagem->__set('mensagem', $_POST['mensagem']);
                
                    print_r($mensagem);
                ```
                
        
        ---
        
        - Verificação de dados
            - Faremos uma verificação se os dados estão validos, se estão preenchidos
                
                ```php
                <?php
                    class Mensagem
                    {
                        private $para = null;
                        private $assunto = null;
                        private $mensagem = null;
                
                        public function __get($attr)
                        {
                            return $this->$attr;
                        }
                
                        public function __set($attr, $valor)
                        {
                            $this->$attr = $valor;
                        }
                
                        public function mensagemValida()
                        {
                            if(empty($this->para) || empty($this->assunto) ||empty($this->mensagem))
                            {
                                return false;
                            }
                            return true;
                        }
                
                    }
                    $mensagem = new Mensagem();
                    $mensagem->__set('para', $_POST['para']);
                    $mensagem->__set('assunto', $_POST['assunto']);
                
                		//reparem que essa condicional está depois de serem setados os dados
                    $mensagem->__set('mensagem', $_POST['mensagem']);
                    if($mensagem->mensagemValida())
                    {
                        echo 'Mensagem válida';
                    }else
                    {
                        echo 'Mensagem inválida';
                    }
                ```
                
        
        ---
        
        - Inclusão de biblioteca
            - Entraremos no site:
                1. [https://packagist.org/packages/phpmailer/phpmailer](https://packagist.org/packages/phpmailer/phpmailer)
            - Então iremos para o github do criador e baixaremos a ultima versão
            - Então extraia o arquivo
            - Depois disso copie para a pasta de nossa aplicação, a pasta ‘scr’ extraida
            - Renomeie para ‘PHPMailer’ essa pasta para facilitar o entendimento
            
            ---
            
            - Então, no arquivo ‘processa_envio’, incluiremos as bibliotecas:
                
                ```php
                require "./PHPMailer/Exception.php";
                require "./PHPMailer/OAuth.php";
                require "./PHPMailer/PHPMailer.php";
                require "./PHPMailer/POP3.php";
                require "./PHPMailer/SMTP.php";
                ```
                
            
            ---
            
            - Fazemos agora a configuração do namespace
            - Como ele já tem um namespace apenas colocaremos no nosso código, igual está no próprio arquivo
                
                ```php
                use PHPMailer\PHPMailer\PHPMailer;
                use PHPMailer\PHPMailer\Exception;
                use PHPMailer\PHPMailer\SMTP;
                ```
                
        
        ---
        
        - Reorganizando
            - Agora iremos reorganizar nosso código para implementar o código já feito na biblioteca
            - Retire o else e rearrange o if da seguinte maneira
                
                ```php
                if(!$mensagem->mensagemValida())
                    {
                        echo 'Mensagem inválida';
                    }
                ```
                
            - Então copie o código que está no github para o nosso código, ficando assim:
                
                ```php
                <?php
                
                    require "./PHPMailer/Exception.php";
                    require "./PHPMailer/OAuth.php";
                    require "./PHPMailer/PHPMailer.php";
                    require "./PHPMailer/POP3.php";
                    require "./PHPMailer/SMTP.php";
                
                    use PHPMailer\PHPMailer\PHPMailer;
                    use PHPMailer\PHPMailer\Exception;
                    use PHPMailer\PHPMailer\SMTP;
                
                    class Mensagem
                    {
                        private $para = null;
                        private $assunto = null;
                        private $mensagem = null;
                
                        public function __get($attr)
                        {
                            return $this->$attr;
                        }
                
                        public function __set($attr, $valor)
                        {
                            $this->$attr = $valor;
                        }
                
                        public function mensagemValida()
                        {
                            if(empty($this->para) || empty($this->assunto) ||empty($this->mensagem))
                            {
                                return false;
                            }
                            return true;
                        }
                
                    }
                    $mensagem = new Mensagem();
                    $mensagem->__set('para', $_POST['para']);
                    $mensagem->__set('assunto', $_POST['assunto']);
                    $mensagem->__set('mensagem', $_POST['mensagem']);
                
                    //print_r($mensagem);
                
                    if(!$mensagem->mensagemValida())
                    {
                        echo 'Mensagem inválida';
                    }
                
                    $mail = new PHPMailer(true);
                
                    try {
                        //Server settings
                        $mail->SMTPDebug = SMTP::DEBUG_SERVER;                      //Enable verbose debug output
                        $mail->isSMTP();                                            //Send using SMTP
                        $mail->Host       = 'smtp.example.com';                     //Set the SMTP server to send through
                        $mail->SMTPAuth   = true;                                   //Enable SMTP authentication
                        $mail->Username   = 'user@example.com';                     //SMTP username
                        $mail->Password   = 'secret';                               //SMTP password
                        $mail->SMTPSecure = PHPMailer::ENCRYPTION_SMTPS;            //Enable implicit TLS encryption
                        $mail->Port       = 465;                                    //TCP port to connect to; use 587 if you have set `SMTPSecure = PHPMailer::ENCRYPTION_STARTTLS`
                    
                        //Recipients
                        $mail->setFrom('from@example.com', 'Mailer');
                        $mail->addAddress('joe@example.net', 'Joe User');     //Add a recipient
                        $mail->addAddress('ellen@example.com');               //Name is optional
                        $mail->addReplyTo('info@example.com', 'Information');
                        $mail->addCC('cc@example.com');
                        $mail->addBCC('bcc@example.com');
                    
                        //Attachments
                        $mail->addAttachment('/var/tmp/file.tar.gz');         //Add attachments
                        $mail->addAttachment('/tmp/image.jpg', 'new.jpg');    //Optional name
                    
                        //Content
                        $mail->isHTML(true);                                  //Set email format to HTML
                        $mail->Subject = 'Here is the subject';
                        $mail->Body    = 'This is the HTML message body <b>in bold!</b>';
                        $mail->AltBody = 'This is the body in plain text for non-HTML mail clients';
                    
                        $mail->send();
                        echo 'Message has been sent';
                    } catch (Exception $e) {
                        echo "Message could not be sent. Mailer Error: {$mail->ErrorInfo}";
                    }
                ```
                
            - Para mostrar aonde eu peguei, aqui está o link e uma amostra de onde foi retirado:
                - [https://github.com/PHPMailer/PHPMailer/tree/v6.6.2](https://github.com/PHPMailer/PHPMailer/tree/v6.6.2)
                
                ![Untitled](PHP%20FULL%209da733f133934045afa87d7ba4e7997d/Untitled%209.png)
                
        
        ---
        
        - Parando processo
            - Então caso a mensagem seja inválida, iremos parar todo o processo, utilizando o método nativo do PHP die()
            - Ficando assim:
                
                ```php
                if(!$mensagem->mensagemValida())
                {
                    echo 'Mensagem inválida';
                    die();
                }
                ```
                
        
        ---
        
        - Configurando processos para teste
            - Agora iremos mudar no ‘processa_envio.php’ as credenciais bases para envio do email
                
                ![Untitled](PHP%20FULL%209da733f133934045afa87d7ba4e7997d/Untitled%2010.png)
                
            - Agora precisaremos saber o SMTP do servidor que enviará o email
            - Utilizaremos a do google, o gmail
            - Então pesquisaremos ‘SMTP google gmail server’
                - Link: [https://support.google.com/a/answer/176600?hl=pt](https://support.google.com/a/answer/176600?hl=pt)
            - DNS do gmail:[smtp-relay.gmail.com](http://smtp-relay.gmail.com/)
                
                ![Untitled](PHP%20FULL%209da733f133934045afa87d7ba4e7997d/Untitled%2011.png)
                
            - Afim de testes deixaremos dessa maneira
                
                ![Untitled](PHP%20FULL%209da733f133934045afa87d7ba4e7997d/Untitled%2012.png)
                
            - E não utilizaremos anexos
                
                ![Untitled](PHP%20FULL%209da733f133934045afa87d7ba4e7997d/Untitled%2013.png)
                
            - Conteúdo do email
                
                ![Untitled](PHP%20FULL%209da733f133934045afa87d7ba4e7997d/Untitled%2014.png)
                
        
        ---
        
        - Configurações de envio finais
            - Agora iremos recuperar pela instancia
                - $mensagem→__get(’var’)
            - Ficando desta forma
            
            ```php
            $mail->addAddress($mensagem->__get('para'));
            $mail->Subject = $mensagem->__get('assunto');
            $mail->AltBody = $mensagem->__get('mensagem');
            $mail->AltBody = 'É necessário ter suporte HTML para ter acesso total a essa mensagem';
            //embaixo de $mail->send();
            echo 'E-magil enviado com sucesso!';
            ```
            
        
        ---
        
    
    ---
    
    - Restrições
        - Primeiro ao invés de matar o processor com o die(), iremos renvia-lo ao index.php
            
            ```php
            //die();
            header('Location: index.php?erroAoEnviar');
            ```
            
        
        ---
        
        - Agora caso tenha feito o envio da mensagem
        - Criaremos primeiro um array para isso
        - Logo embaixo das variáveis criadas
            
            ```php
            public $status = ['codigo_status' => null, 'descricao_status' => ''];
            ```
            
        - Agora embaixo de ‘$mail->sendo();’
            
            ```php
            $mensagem->status['codigo_status'] = 1;
            $mensagem->status['descrição_status'] = 'E-magil enviado com sucesso!';
            ```
            
        - Agora em catch
            
            ```php
            $mensagem->status['codigo_status'] = 2;
            $mensagem->status['descrição_status'] = 'E-mail não enviado!' . 'Detalhes do erro: ' . $mail->ErrorInfo
            ```
            
        - Mude
            
            ```php
            $mail->SMTPDebug = SMTP::DEBUG_SERVER;
            	//para
            $mail->SMTPDebug = false;
            ```
            
            - comente o print_r
        - Agora ao fim do comando <?php ?>
            
            ```php
            <html>
                <head>
                <meta charset="utf-8" />
                	<title>App Mail Send</title>
            
                	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
                </head>
                <body>
                    <div class="container">
                    <div class="py-3 text-center">
            				<img class="d-block mx-auto mb-2" src="logo.png" alt="" width="72" height="72">
            				<h2>Send Mail</h2>
            				<p class="lead">Seu app de envio de e-mails particular!</p>
            			</div>
                        <div class="row">
                            <div class="col-md-12">
                                <?php
                                    if($mensagem->status['codigo_status'] == 1)
                                    {
                                ?>
                                    <div class="container">
                                        <h1 class="display-4 text-success">Sucesso</h1>
                                        <p>
                                            <?=
                                                $mensagem->status['descricao_status']
                                            ?>
                                        </p>
                                        <a href="index.php" class="btn-success btn-lg mt-5 text-white">voltar</a>
                                    </div>
                                <?php
                                    }
                                ?>
                                
                                <?php
                                    if($mensagem->status['codigo_status'] == 2)
                                    {
                                ?>
                                    <div class="container">
                                        <h1 class="display-4 text-danger">Ops!</h1>
                                        <p>
                                            <?=
                                                $mensagem->status['descricao_status']
                                            ?>
                                        </p>
                                        <a href="index.php" class="btn-success btn-lg mt-5 text-white">voltar</a>
                                    </div>
                                    
                                <?php
                                    }
                                ?>
                            </div>
                        </div>
                    </div>
                </body>
            </html>
            ```
            
            - nesse código ja tem feito a lógica de envio de email feito
    
    ---
    
    - Segurança
        - Agora iremos mover o arquivo processa_envio.php para uma pasta fora do htdocs
        - Então crie uma pasta e coloque nosso arquivo la
        - Então no iremos criar um novo arquivo que irá substituir o processa_envio.php
        - Criaremos um novo arquivo com o mesmo nome (processa_envio.php), na pasta onde fica o index.php
        - Então esse arquivo enviará para o arquivo original
            - Seu conteúdo será:
                
                ```php
                <?php
                    require "../../app_send_mail/processa_envio.php";
                ?>
                ```
                
        - Não será preciso se preocupar com os requires dentro do arquivo original, pois ele será pego no contexto certo já