# PHP FULL

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
                
                ![Untitled](PHP%20FULL%20deaf1067b7044f18b0e965cace7e519f/Untitled.png)
                
                ![Untitled](PHP%20FULL%20deaf1067b7044f18b0e965cace7e519f/Untitled%201.png)
                
                - ctrl + f
                    - escreva “timezone”
                
                ![Untitled](PHP%20FULL%20deaf1067b7044f18b0e965cace7e519f/Untitled%202.png)
                
                - então troque para o desejado
                
                ![Untitled](PHP%20FULL%20deaf1067b7044f18b0e965cace7e519f/Untitled%203.png)
                
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
                    echo "$item <br.>";
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
        
        ![Untitled](PHP%20FULL%20deaf1067b7044f18b0e965cace7e519f/Untitled%204.png)
        

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
    - Repare q cada linha foi atribuída a um array
    
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
            
            ![Untitled](PHP%20FULL%20deaf1067b7044f18b0e965cace7e519f/Untitled%205.png)
            
        2. Então crie uma pasta com o nome desejado
            
            ![Untitled](PHP%20FULL%20deaf1067b7044f18b0e965cace7e519f/Untitled%206.png)
            
        3. Passe para essa pasta os arquivos sigilosos/importantes
            
            ![Untitled](PHP%20FULL%20deaf1067b7044f18b0e965cace7e519f/Untitled%207.png)
            
        4. Crie um arquivo .php no lugar do qual foi retirado o script importante, com o mesmo nome para não quebrar o script
            
            ![Untitled](PHP%20FULL%20deaf1067b7044f18b0e965cace7e519f/Untitled%208.png)
            
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

- Glossário
    
    fd == ao clicar em f12 e ir em network/rede/ou_algo_do_tipo é possível ver as requisições feito ao servidor
    
    —F == importante