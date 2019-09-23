# Banco Imobiliário
Banco imobiliário é uma versão de um dos jogos de tabuleiro mais conhecidos e populares do mundo, o *Monopoly*. Neste projeto foi implementada uma versão em Java, que funciona com uma interface textual simples e opera com base nas regras brasileiras do jogo.

## O projeto
O projeto Banco Imobiliário foi desenvolvido pelo aluno, do terceiro período de licenciatura em ciências da computação, Clebson Augusto Fonseca e pelas alunas, também do terceiro período, de bacharelado em sistemas de informação, Amanda Azevedo Martins, Joana Darck Soares da Silva e Joyce Sousa dos Santos.
> Equipe: Equipe 2.</br>
> Link Github: [dcx-cursos/projeto-poo-2019-1-jo/tree/dev](https://github.com/dcx-cursos/projeto-poo-2019-1-jo/tree/dev).</br>
> Link para o relátorio da entrega 3 no Google Docs [aqui!](https://docs.google.com/document/d/1L0anaP1qEhIjeSjO97k65kLi4fCZBfWWgY82ikcp_xA/edit?usp=sharing).

## Instalação
Primeiramente, certifique-se de que você tenha instalados:
 - JDK 8
 - Eclipse ou Netbeans
 - git
 
 em seguida crie um diretório para ser sua Workspace e clone o repositório dentro desta pasta:

    # clonar o repositório:
    git clone https://github.com/dcx-cursos/projeto-poo-2019-1-jo.git

Após ter realizado o paço acima, mude a branch para "entrega3"

    # mudar a branch
    git checkout entrega3
Agora abra o projeto na sua IDE selecionando a opção: 

    # Para o Eclipse
    > File > Open Projects from File System...
    
    # Para o NetBeans
    > Arquivo > Abrir Projeto

Pronto, tudo instalado! 

Para jogar Banco Imobiliário execute a classe `Main.java`,  do pacote `src/ufpb/jogo`.

Para verificar os testes feitos execute a classe `nomeDaClasse.java` do pacote `src/ufpb/tests`.

- Para verificar os testes é importante que as seguintes dependências estejam devidamente configuradas: 
	 -  JUnit5
	 - Mockito

## Organização deste repositório
 - `Arquivos/` - Contém arquivos com dados das posições do tabuleiro e conteúdo das cartas de sorte ou revés. 
 - `diagrama-de-classes/` - Contém a versão mais atualizada do diagrama de *UML* do jogo.
 - `lib/`- Contém a dependência do Mockito.
 - `relatorio/`- Contém os arquivos .docx e .pdf dos relatórios de todas as entregas.
 - `src/` - Contém o pacote  `ufpb/`, nele são encontrados todos os outros pacotes que possuem as classes do sistema do jogo.</br>
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- `ufpb/cartas/` - Contém as classes que possuem relação com sorte ou revés. </br>
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- `ufpb/exception/` - Contém as classes de exceção.</br>
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- `ufpb/jogo/` - Contém as classes que possuem relação com o jogo.</br>
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- `ufpb/lougradouros/` - Contém as classes que são posição do tabuleiro.</br>
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- `ufpb/opcoes/` - Contém as classes que são comandos do jogo, como por exemplo, jogar, pagar, sair, etc.</br>
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- `ufpb/recuperaDados/` - Contém as classes de persistência de dados.</br>
		&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- `ufpb/tests/` - Contém as classes de teste.</br>

## Padrões de projetos implementados
|Padrão de protejo| Maneira como foi implementado |
|--|--|
| Facade  | Foi utilizado como uma fachada de comunicação da logica do banco imobiliário com a parte visível para o jogador. |
| Factory | Foi utilizado para tratar as opções dos jogadores, quando se está na prisão, uma serie de opções está disponível e quando não está as opções normais são usadas. Também foi usado na implementação de títulos que tinham um evento muito parecido. |
| Strategy| Foi utilizado para em tempo de execução fosse feito um evento/ação do baralho/tabuleiro. |


## Diagrama de classes 

![enter image description here](https://raw.githubusercontent.com/joanasoaresd/ProjetoBancoImobiliario/master/diagrama%20da%202%C2%AA%20entrega.png?token=AKUQEUNIHQWCYVTNPLJWYWC5R5STM)


- Descrição do diagrama de classes UML

|Nome do Pacote| Descrição |
|--|--|
|ufpb.jogo  | Tabuleiro.java se relaciona com SorteOuReves.java, com recuperaDadosDoTXT.java, com Posicao.java [...] Jogador.java se relaciona com TituloFactory,java [...] JogoFactory.java com Opcao.java,JogoFactoryPrisao.java[...]JogoFacade.java |
| ufpb.opcoes | Este pacote é referente às opções que cada jogador tem durante sua jogada. {add como ela se relaciona com o padrão JogoFactory e pq disso} |
|ufpb.cartas  |Neste pacote são armazenadas as classes que *extends* a superclasse, `SorteOuReves.java`. Nela foi criada uma classe para cada tipo de carta de Sorte ou Revés, que realizam ações com base na sua descrição. A classe de `SorteOuReves.java` {tipo de relação com Tabuleiro.java e o que acontece tanto} |
| ufpb.lougradouros | Por implementar Posicao.java, todas as classes deste pacote possuem um método evento(), esse método possibilita que ao o jogador se mover no tabuleiro e parar em uma nova posição, ele execute apenas a ação prevista para aquela posição. |
| ufpb.exception | Todas as exceções deste pacote são lançadas e tratadas nas classes `Conta.java`, `Jogador.java`, `JogoFacade.java`, `JogoFactory.java`, `JogoFactoryPrisao.java` e `Jogo.java`, do pacote `ufpb.jogo`.   {add como elas são lançadas e tratadas}|
| ufpb.recuperaDados | Este pacote é referente a camada de persistência de dados em arquivos, onde conseguimos recuperar os dados, em forma de String dos arquivos `.txt`, para serem convertidos em objetos na classe `Tabuleiro.java`.|


## Ações desenvolvidas por cada integrante da equipe
|Nome|Ações|
|--|--|
|Amanda| fdsvadf |
|Clebson| svf |
|Joana|  sdfvsd|
|Joyce| sdvvcsdc |
