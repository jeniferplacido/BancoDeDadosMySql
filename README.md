## Introdução ao Banco de Dados

Segundo Korth, um banco de dados “é uma coleção de dados inter-relacionados,
representando informações sobre um domínio específico”, ou seja, sempre que for
possível agrupar informações que se relacionam e tratam de um mesmo assunto,
posso dizer que tenho um banco de dados.
Por exemplo as informações armazenadas de uma lista telefônica, um registros de
usuários em um sistema de e-commerce, um sistema de controle de RH de uma
empresa, um sistema de clinica para cadastro de pacientes.

------

Já um sistema de gerenciamento de banco de dados (SGBD) é um software que possui
recursos capazes de manipular as informações do banco de dados e interagir com o
usuário. 

Exemplos de SGBDs são: Oracle, SQL Server, DB2, PostgreSQL, MySQL, o próprio Access ou Paradox, entre outros.

Por último, temos que entender que um sistema de banco de dados é como o conjunto
de quatro componentes básicos: dados, hardware, software e usuários.

O objetivo de um sistema de banco de dados são o de isolar o usuário dos detalhes
internos do banco de dados (promover a abstração de dados) e promover a
independência dos dados em relação às aplicações, ou seja, tornar independente da
aplicação, a estratégia de acesso e a forma de armazenamento.

<p align="center">
  <img width="700" height="256" src="https://www.portalgsti.com.br/media/uploads/marcomascarenhas/banco-de-dados-mysql.jpg">
</p>

------

<p align="center">
  <img width="700" height="356" src="https://www.educative.io/v2api/editorpage/6575689680551936/image/4670199253958656">
</p>

------

## Tipo de Dados

Agora que entendemos o conceito de banco de dados, também, precisamos
entender que assim como tudo que manipula dados precisamos definir a “Tipagem” dos
dados, vamos ver algumas:

| Dado                                  | Tipo       |
| ------------------------------------- | ---------- |
| Texto                                 | VARCHAR(n) |
| Carácter                              | CHAR(n)    |
| Data                                  | DATE       |
| Data e hora                           | DATETIME   |
| Inteiro                               | INT        |
| Decimal                               | DECIMAL    |
| Ponto Flutuante                       | FLOAT      |
| Ponto Flutuante mais casas decimais   | DOUBLE     |
| Numero Decimal alterável padrão(10,0) | DECIMAL    |
| Booleano (Verdadeiro ou Falso)        | BOOLEAN    |

[Documentação tipo de dados](https://www.w3schools.com/sql/sql_datatypes.asp)

------

## MER - Modelo Entidade Relacional

Assim como todo os projetos, devemos iniciar por um “esboço” do que de fato será a nossa base de dados, quando desenhamos esta estrutura, á chamamos de MER - Modelo Entidade Relacional onde com apenas um papel e uma caneta podemos desenhar o modelo do nosso banco de dados expondo todos os relacionamento entre as tabelas.

<p align="center">
  <img width="700" height="356" src="http://arquivo.devmedia.com.br/artigos/Joel_Rodrigues/mer/image001.png">
</p>

------

## DER - Diagrama Entidade Relacional

Assim como o MER, o DER - Diagrama Entidade Relacional também pode ser visto como um “esboço” de uma forma mais detalhada em comparação ao MER da nossa base
d, porém ele é feito através de uma ferramenta especifica, onde podemos compartilhar de uma forma segura com os demais membros de nossa equipe, e também extrair as o nosso DER em forma de query **(o código sql usado para manipular o banco de dados**).

<p align="center">
  <img width="700" height="356" src="https://i.stack.imgur.com/mEapJ.png">
</p>

------

## Relacionamento Entre Tabelas

Uma vez que terminamos o nosso MER e o nosso DER, precisamos definir o relacionamento entre as tabelas, De acordo com a quantidade de objetos envolvidos em cada lado do relacionamento, podemos classifica-los de três formas:

**Relacionamento 1...1 (um para um**): cada uma das duas entidades envolvidas referenciam obrigatoriamente apenas uma unidade da outra. Por exemplo, em um banco de dados de currículos, cada usuário cadastrado pode possuir apenas um
currículo na base, ao mesmo tempo em que cada currículo só pertence a um único usuário cadastrado.

**Relacionamento 1...n (um para muitos)**: uma das entidades envolvidas pode referenciar várias unidades da outra, porém, do outro lado cada uma das várias unidades referenciadas só pode estar ligada uma unidade da outra entidade. Por
exemplo, em um sistema de plano de saúde, um usuário pode ter vários dependentes, mas cada dependente só pode estar ligado a um usuário principal.
Note que temos apenas duas entidades envolvidas: usuário e dependente. O que muda é a quantidade de unidades/exemplares envolvidas de cada lado.

<p align="center">
  <img width="814" height="424" src="https://dkrn4sk0rn31v.cloudfront.net/2019/04/16112722/Picture1N.png">
</p>

Relacionamento n...n ou ... (muitos para muitos): neste tipo de relacionamento cada entidade, de ambos os lados, podem referenciar múltiplas unidades da outra.

Por exemplo, em um sistema de biblioteca, um titulo pode ser escrito por vários autores, ao mesmo tempo em que um autor pode escrever vários titulos. Assim, um objeto do tipo autor pode referenciar múltiplos objetos do tipo titulo, e vice versa.

**Bom agora que já definimos a estrutura do nosso banco de dados e o relacionamento entre**
**as tabelas, Vamos por a mão na massa!**

