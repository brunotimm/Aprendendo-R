# Aula 0 
## Apresentação do R e RStudio

A aula de apresentação da linguagem R, aborda o que é o R e o RStudio, como efetuar seus downloads, algumas informações gerais e funções básicas muito úteis de se conhecer,
logo que se tem contato com a linguagem, como por exemplo a função help.

### O que é o R e RStudio?

R é uma linguagem/ softwaree de computação estatística e gráfica de código aberto e disponível gratuitamente. R é um software para análise estatística que permite de forma robusta todo e qualquer cálculo estatístico que se faz necessário fornecendo uma ampla variedade de técnicas, como por exemplo modelagem linear, testes estatísticos clássicos, análise de séries temporais, etc. Além disso é uma ferramenta que permite criar gráficos e relatórios do mais alto nivel, bem projetados e que inclua símbolos e fórmulas matemáticas. Já o  RStudio é um software de ambientação de desenvolvimento integrado (IDE) para o R, ou seja, um ambiente complementar a linguagem que permite melhor trabalho e visualização com a programação em R. (Imagens abaixo)


##### Imagem do software R

![Imagem0b](https://user-images.githubusercontent.com/96084042/168374190-0d339f1d-c0f7-424d-b5d8-03f081bd9ad5.png)



##### Imagem do IDE RStudio 

![Imagem0a](https://user-images.githubusercontent.com/96084042/168373758-ec657c74-a1a8-4eeb-8e0a-68cbae46aad3.png)



### Pacotes
É possível fazer muita coisa em termos de ciência de dados no R no entanto as vezes é necessário alguns recursos adicionais que podem ser encontrados nos pacotes. Os pacotes são uma coleções de funções, dados e arquivos de ajuda reunidos em uma estrutura, que podem ser instaladas no R de uma maneira muito simples e prática de várias fontes, como por exemplo (e os mais populares) CRAN e o GitHub. 
Para instalar um pacote do CRAN usamos a função install.packages. Suponha que queremos instalar o pacote tidyverse (que será abordado posteriormente nesse material), devemos prosseguir da seguinte forma

      install.packages("tidyverse") 
      
* Uma vez instalado, o pacote ficará salvo na memória do R e para utiliza-lo basta usar o comando de carregamento de pacotes que veremos a seguir
* É necessário colocar o nome do pacote que se quer instalar entre aspas simples ou duplas (tanto faz) para que a instalação seja realizada com sucesso. 

##### Carregando os pacotes
Depois de instalar o pacote no R, ele não está automáticamente sendo usado. Para conseguirmos utilizar os pacotes baixados, precisamos carregá-los por meio da função library(). A função library também carregará quaisquer pacotes adicionais necessários e poderá imprimir informações adicionais do pacote.
      
      library(tidyverse)
      
* É importante perceber que toda vez que você inicia uma nova sessão do R (ou restaura uma sessão salva anteriormente), você precisa carregar os pacotes que for usar novamente.
* Se tentarmos usar uma função sem antes carregar o pacote que ele está contido, o R retornará um erro como esse

      could not find package "tidyverse"



### Ajuda no R
Um dos muitos aspectos positivos do R é o seu sistema de ajuda, seja ela dentro do próprio sistema, através da imensa e ativa comunidade de pessoas que usam o R ou por meio da riqueza de recursos on-line onde você pode obter mais informações. Independemente do canal que você utilize, as ferramentas de ajuda são muito acessíveis, o que torna fácil obter a resposta para a dúvida e problema que você pode estar enfrentando (e acredite vão ser muitos). O lado bom é que provavelmente alguém já deve ter passado pelo mesmo problema que você e portanto a solução para isso será muito mais simples para você do que foi para aqueles que te deram a resposta. Algumas das formas de se obter ajuda em R são:

Função help(): A função help() é utilizada para acessar o recurso de ajuda interno do R para obter informações sobre qualquer função, como por exemplo pedir ajuda sobre a mediana de um conjunto de dados:

      help(median)

* (Importante: para a utilização da função help é necessário saber o nome da função que se deseja buscar ajuda).

Outra alternativa é usar ?nome da função, no caso da função median ficaria

      ?median
      
 * O resultado produzido é exatamente o mesmo que help(median)

![Imagem0c](https://user-images.githubusercontent.com/96084042/168378483-717089aa-eb8b-4578-81f6-1502de199e93.png)



Mas e se você não lembrar o nome da função que gostaria de usar? Bem, o R tem uma outra forma de pedir ajuda ao sistema! Nesse caso, basta saber uma palavra-chave referente ao que se busca. Por exemplo, gostaria de criar um diagrama de caixa mas não me recordo o comando desse, contudo sei que o termo "plot" refere-se a plotagem (criação) de gráficos. Podemos utilizar então a função apropos, nesta, colocamos a palavra-chave sobre aspas dentro do parênteses da funçao e ela nos lista todas as funções com esse termo chave.

      apropos("plot")
      
![Imagem0d](https://user-images.githubusercontent.com/96084042/168484889-4b3af483-bf83-409e-b919-184e9d27af81.png)

      
 * O comando que buscavamos era o "Boxplot" que está grifado na imagem.    
      


Além dessas duas formas de se obter ajuda que mostradas, existem milhares de outros recursos para se obter ajuda tanto dentro do R quanto fora, que não dariam pra ser abordados aqui. Alguns dos outros meios de se obter ajuda são por meio dos cheatsheets, cartões resumos sobre os principais recursos (https://www.rstudio.com/resources/cheatsheets/), funções e dicas de R, no próprio site R (https://www.r-project.org/), e nas mais  diversas comunidades ativas do R e forúns como o Stack Overflow.    
      
      
         
