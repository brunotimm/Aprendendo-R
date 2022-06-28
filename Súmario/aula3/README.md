# Aula 3
## Tipos de Dados
R tem seis tipos básicos de dados; numérico, inteiro, lógico, complexo, caractere e brutos. Compreender os diferentes tipos de dados e como o R lida com esses dados é importante e útil para lidar com alguns problemas e imprevistos durante os trabalhos que se realiza, mas principalmente quando se trata da importação e manipulação de base de dados. 


Os tipos de dados são: 

* *Dados numéricos:* 
São números que contêm um decimal. Na verdade, eles também podem ser números inteiros, mas não vamos entrar em detalhes sobre isso nesse material.

* *Dados inteiros:*
Os inteiros são números inteiros (os números sem um ponto decimal).

* *Dados lógicos:*
Os dados lógicos assumem o valor de TRUE ou FALSE. Há também outro tipo especial de lógica chamada NA para representar valores ausentes.

* *Caracteres:*
Dados de caractere são usados para representar valores de string. Caracteres nada mais são do que uma palavra (ou várias palavras). Um tipo especial de string de caracteres é um factor , que é uma string mas com atributos adicionais (como níveis ou uma ordem). Abordaremos os fatores mais tarde.

* *Dados Brutos:*
Dados brutos sao os dados que encontramos nas planilhas eletrônicas (como Excel por exemplo). Eles são brutos porque não receberam qualquer tipo de tratamento ou organização até a coleta feita. 


![imagem3a](https://user-images.githubusercontent.com/96084042/174133950-e01b134e-3d80-4ffe-b686-274a3ffd5bbd.png)

Outra maneira de descobrir um tipo de daod é por meio de um teste lógico, com a função is.tipodedado que se quer confirmar. Os resultados desse comando resultaram sempre em *TRUE* ou *FALSE* o que signfica se o seu objeto corresponde ou não ao tipo de dado que você atribuiu a ele. 

![imagem3b](https://user-images.githubusercontent.com/96084042/174135026-bf26ed6d-e051-4ec8-b936-d507c0d06373.png)


Em alguns momentos pode ser necessário converter o tipo de dado de uma variavel. Esse processo pode ser realizado por meio da familia de funções de coerção as.nomeclass

![imagem3c](https://user-images.githubusercontent.com/96084042/174137134-c952e053-6126-4ebc-b2fc-83c348bc5bd8.png)


### Estrutura de Dados

Depois de visto alguns tipos de dados que podemos trabalhar no R, iremos abordar agora algumas estruturas de dados muito usadas em R para armazenar esses tipos de dados. 

###### Vetores
Os *vetores* contem dois ou mais elementos (ou valores) dentro dele e podem conter números, caracteres, fatores ou lógicas. O principal aspecto a se lembrar em relação aos vetores é o de que que todos os elementos dentro de um vetor devem ser da mesma classe. Os vetores que contem um unico valor sao chamados de *escalares*. 

##### Matrizes e Arrays
Uma matriz é simplesmente um vetor que possui atributos adicionais chamados dimensões. Arrays são matrizes multidimensionais. Novamente, matrizes e arrays devem conter todos os elementos da mesma classe de dados.
Para criar uma matriz ou uma arrays usamos as funções matrix()e array()

![imagem3d](https://user-images.githubusercontent.com/96084042/174661496-81e6d900-d14b-4f0a-ba8d-ed0abd3ec48a.png)

* No primeiro exemplo temos uma matriz preenchida em linha com o argumento *byrow = TRUE*
* No segundo exemplo temos uma matriz tradicional em que a contagem é feita por colunas. 

![imagem3e](https://user-images.githubusercontent.com/96084042/174662582-ae79b374-5527-4252-9105-161731b65363.png)


* Ao usar a função array(), definimos as dimensões usando o *dim = argumento* . Nesse caso temos uma matriz com 2 linhas, 4 colunas em 2 matrizes diferentes. No exemplo com a função matrix() temos uma matriz unidimensional. O que muda portanto é que definimos as mesmas características para a nossa estrutura em apenas uma matriz no primeiro caso e em uma matriz bidimensional nesse. 

Podemos dar nomes as linhas e colunas de nossas matrizes

![imagem3f](https://user-images.githubusercontent.com/96084042/174664610-c97df71e-8c6f-47cf-b800-8a72e6171fac.png)

Assim como vimos com os vetores que criamos com as matrizes também é possível realizar operações o R possui várias funções internas para executar operações de matrizes. Vamos dar uma olhada nas principais a seguir

#### Operações com matrizes

![imagem3g](https://user-images.githubusercontent.com/96084042/174665612-187bcc22-757b-40ed-adc5-3a366ab245af.png)

* temos aqui a extração da diagonal principal de nossa matriz e a sua transposta.

![imagem3h](https://user-images.githubusercontent.com/96084042/174666211-7b7b1c78-ff2d-4356-9ae9-23eb3599e059.png)

**I: soma de matrizes**;

**II : produtos de cada elemento das matrizes**; 

**III: multiplicaçao de matrizes**


### Listas 

As listas são capazes de armazenar assim como as matrizes e vetores,  com a diferença que nas listas é possível armazenar misturas de tipos de dados, podemos até armazenar outras estruturas de dados, como vetores e matrizes. Para criar uma lista, podemos usar a função list() 

    list_1 <- list(c("azul", "rosa" , "verde"), c(TRUE, FALSE, TRUE), matrix(1:4, nrow = 2))
    list_1


    list_2 <- list(Colours = c("azul", "rosa" , "verde"), 
               Evaluation = c(TRUE, FALSE, TRUE),
               Time = matrix(1:4, nrow = 2))  
    list_2


    names(list_1) <- c("Colours", "Evaluation", "Time") 
    list_1


![imagem3i](https://user-images.githubusercontent.com/96084042/176233359-2b0b3db6-2de6-446a-b2f2-769f42ab14e7.png)
































