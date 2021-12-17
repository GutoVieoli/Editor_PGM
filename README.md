Documentação do programa de edição PGM

Documentação referente ao programa final a partir da linha 60

Elaboração do algoritmo a partir das orientações em aula.
-------------------------------------------------------------

Um único vetor, em ordem, com toda a matriz imagem.

 - Variáveis -
x - número de linhas
y - número de colunas
i - auxiliar para preencher o vetor com o arquivo mãe.
res - quantidade de tons de cinza
cont - opção atual escolhida

_______________________________
 - Imagem Negativa -
 Pega cada elemento em ordem, e subtrai do valor máximo de tons (res), o
valor do pixel atual (line). EX: 255-8 = 247

________________________________
 - Espelho V -
 Apenas passa a matriz ao contrário, de trás pra frente.
 Um "for" com uma variável "kont" que recebe o tamanho da matriz, e vai decrementando
e indicando os valores de trás para frente a serem inscritos.

________________________________
 - Espelho H -
 Um "for", que anda linha por linha (representado por kontx), com outro "for" que escreve a
linha ao contrário (konty).
 Kontx recebe o zero, e vai incrementando, enquanto konty recebe o numero de linhas, e vai 
decrementando, possibilitando que a linha seja escrita de trás para frente.

________________________________
 - Girar 90 Anti H -
 Insere o último elemento de cada uma das linhas, em seguida o penúltimo e assim por diante
 Em um "for", pega o tamanho da linha (kontx), e vai decrementando até chegar em zero, e dentro
disso, vai pulando de linha em linha até o final do arquivo. (konty)
 1 2   3   4  5
 6 7   8   9  10      x = 5; y = 3
11 12 13  14  15
                                  
5  10  15            5 + (0 * 5) = 5 
4   9  14            5 + (1 * 5) = 10
3   8  13            5 + (2 * 5) = 15
2   7  12            4 + (0 * 5) = 4
1   6  11            4 + (1 * 5) = 9     (...)
________________________________

--------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------
Versão Trabalho AEDS II - Ponteiros, manipulação de imagem, criação de 
funções e cabeçalho
Alunos:

André Augustho Sarti Trindade Silva - 2021.1.08.001
Augusto Vieira de Oliveira - 2021.1.08.002
Diego de Magalhães Vieira - 2021.1.08.004
--------------------------------------------------------------------------------------
Notas de atualização:


Atualização 17/12/2021 - Para usuários Netbeans

Execução no Netbeans comprometida por duplicidade de declaração. 
A solução da versão anterior se torna um problema quando executada no netbeans.
Para execução no netbeans se faz necessária a exclusão da linha declarada no 
arquivo funcImg.h responsável por chamar o arquivo funcs.cc. 

        #include <fstream>
---->>  #include "funcs.cc"  <<--- excluir linha 2 no arquivo funcImg.h
        using namespace std;

-- Vinheta

Implementação da função Vinheta (Escurecimento das bordas).

-- VS Code: memória destinada ao compilador. 
Gerenciar/
configurações/
Buscar: compiler/
-- Aqui nessa opção de flags inserir o código abaixo
--> C-cpp-complie-run:Cpp-glags

Código:
... (180 linhas)
