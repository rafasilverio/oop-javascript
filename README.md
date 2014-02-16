## OOP (Object-oriented Programming)

### Introdução

![](http://octodex.github.com/images/socialite.jpg)

Também conhecida como OOP (Object-oriented Programming), em português Programação Orientada a Objetos, se resume a arquitetura e modelagem de um sistema com base na definição e criação de objetos que simulam o mais próximo possível do mundo real, dentro do mundo virtual. O que seria essa simulação de realidade dentro de um software? Significa você moldar as características e componentes do seu software baseado em objetos reais que tragam algum significado real para sua aplicação, aonde estes objetos devem ser compostos por atributos e funções e se comunicar através do envio e recebimento de mensagens, assim como ocorre no mundo real.

A OOP tem várias virtudes, uma delas é a facilidade em eliminar *"gaps (lacunas) semânticos"*, ou seja, facilitar o entendimento e a comunicação dentro da arquitetura do sistema, eliminando possíveis ruídos e abstrações do mesmo, tornado-o assim mais óbvio e natural. Podemos ainda citar outras virtudes como: ganho de produtividade, redução na complexidade do sistema e auxílio para reutilização de códigos.

Alguns paradigmas clássicos de programação, quando em conjunto com o conceito de OOP facilitam muito o processo de arquitetura de um sistema, são eles: DRY (Don't Repeat Yourself), SOLID Principles e Design Patterns. Estes paradigmas não serão abordados neste artigo, porém pode-se dizer que todos eles auxiliam e pregam muito a modularização e re-aproveitamento de código, partindo da idéia de criação de componentes dentro de uma aplicação e aplicando o máximo de independência possível entre estes componentes, forçando o programador a se tornar um arquiteto ativamente pensante sobre a estrutura como de um modo geral.

Partindo de um conceito mais tradicional, temos a Precedural Programming, ou Programação Procedural em português. Com um nome bem intuito, a programação procedural é baseada em programador orientado à procedimentos e funções. A programação orientada a objetos não substitui a programação procedural, muito pelo contrário, pode-se dizer que uma é a evolução da outra, pois introduz conceitos e boas práticas que não foram formalizados, como definição de variáveis locais/globais, métodos privados/públicos e escopos de classe. Porém, fica confuso quando tenta-se diferenciar programação estruturada de OOP, pois a primeira se baseia em uma cadeia de procedimentos (ações e funções) executados em determinada ordem, enquanto OOP se preocupa com a criação dos objetos, seus métodos, atributos e relacionamentos.

Neste método de programação toda a mágica ocorre através da criação de um **conjunto de classes** que formam a modelagem do sistema. Ao criar uma classe determina-se quais são os **objetos** presentes dentro deste sistema. Cada classe contém determinados **comportamentos e estados**, assim como relacionamentos com outras classes, conceito também conhecido como **herança**.

C++, C♯, .NET, Java, Object Pascal, Objective-C, Python, SuperCollider, Ruby, Self, IO e Smalltalk são exemplos de linguagens de programação orientadas a objetos. Na grande maioria das linguagens citadas, a programação orientada a objetos não é uma regra, mas sim uma possibilidade. Onde você pode tanto programar seguindo OOP, quanto programar no modelo procedural, ou misturar os dois conceitos. Porém, existem algumas linguagens que optaram por ser mais "puras" durante a sua construção, e nelas temos todo o seu core (essência) baseado em OOP, que é o caso de Smalltak, Self e IO.

### Fatos Históricos

A programação orientada a objetos demorou um tempo para ser aceita pelas grande empresas de software, fato esse que atrasou um pouco sua disseminação entre as comunidades. Porém, OOP é um termo antigo e já usado a um bom tempo.

— ***Falar sobre smalltalk e simula67***

### Entendendo os Principais Conceitos

Dê um modo geral, dentro da programação existem diversos conceitos que podem acabar definer os aspectos e características das linguagens, alguns destes conceitos são mais específicos e não são aplicados em todas as linguagens de programação, e outros são mais genéricos.

Para poder exemplificar e começar a falar sobre Orientação a Objetos, é necessário o conhecimento destes conceitos, e é de extrema importância aprender e estar bem familiarizado com cada um desses deles, pois são itens usados no dia-a-dia de um programador.

Como estamos abordando Javascript como principal linguagem deste artigos, vamos usufruir de um exemplo real criado com Javascript para poder exemplificar cada um desses conceitos.

#### Classe:

No começo pode ser difícil entender o conceito de classe e objeto, porém é imprescindível que saibamos a diferença entre estes dois itens, e para explicar de uma maneira eficiente é preciso se fazer comparação em relação à criação de classes e objetos. Por isso deve-se entender bem o conceito de objeto, atributos, funções e mensagens dentro de uma classe.

As classes nos ajudam a classificar nosso sistema em grupos, formando assim definições mais claras e reais de como aquela aplicação é modelada. Uma classe é uma abstração, ou seja, um modelo de definição para classificar a criação de objetos. Diferente do objeto, uma classe não tem vida, ela apenas simboliza e cria um conceito classificativo.

Para ficar mais fácil de entender, vamos criar um exemplo criando uma classe Cars. A classe Cars, dentro de um sistema, classificaria todos os carros da aplicação. Esta classe, por sua vez, poderia conter atributos do tipo "model" (modelo) e "manufacturing date" (data de fabricação), e também poderia conter métodos como "turn on" (ligar) e "turn off" (desligar).

Este é o exemplo de como poderíamos criar esta classe em Javascript

```javascript
function Cars(model, manufacturingDate) {
	this.model = model;
	this.manufacturingDate = manufacturingDate;
};

Cars.prototype.turnOn = function() {
	console.log('car is on!')
};

Cars.prototype.turnOff = function() {
	console.log('car is off!')
};
```

A partir deste código temos um classe Cars criada. Definimos dois atributos para a classe: "model" e "manufacturing date", também definimos dois métodos: um método chamado "turnOn" e outro "turnOff".

***Observações:*** Em Javascript não existe uma definição oficial para a criação de classes como em outras linguagens como Ruby e Python, por exemplo. Porém, existem algumas maneiras que podemos usufruir para fazer isto. Neste exemplo estou usando as chamadas Funções Construtoras, que é um dos métodos que temos disponíveis para criar uma classe. Mais para frente abordaremos quais técnicas podemos usar para a criação de classes em javascript e quais as vantagens e desvantagens de cada uma.

##### Padronização e Boas Práticas na escrita de Códigos:

Fugindo rapidamente dos conceitos atrelados à programação orientada a objetos, falaremos um pouco sobre padrões de código, que são essenciais para facilitar a manutenção do seu código e torná-lo mais legível.

É importante adotar padrões ao escrever classes, atributos e métodos, pois um código deve ter legibilidade e ser de fácil entendimento, para que não apenas uma única possa trabalhar com este código, mas qualquer pessoa que entenda e saiba programar na linguagem proposta. Porém, os padrões que podem ser utilizados em um projeto depende muito da linguagem que se está trabalhando, gosto pessoal, ou ainda, os padrões já definidos na documentação do projeto.

Veremos agora um pouco sobre um padrão de escrita de código muito conhecido, que é o padrão ***CamelCase***. Este padrão tem uma difusão muito grande na maioria das linguagens mais populares de programação, como PHP, Ruby, Python e Javascript. Está técnica consiste basicamente em escrever uma série de palavras ou frase, usufruindo da primeira letra da palavra em maiúsculo e unindo todas estas palavras sem espaços, vejamos um exemplo:

> ThisIsABigPhraseWithCamelCase

Porém, não é comum escrever frases usando CamelCase, mas sim palavras compostas. Também é importante citar que existem variações dentro desta técnica como, por exemplo, ***lowerCamelCase***. O lowerCamelCase é muito parecido com o CamelCase padrão, porém define que a primeira letra da primeira palavra deve ser minúscula. É interessante observar que esta é uma técnica muito difundida e usada no Javascript.

Ok, e aonde aplicamos a técnica de CamelCase, lowerCamelCase e dentre outras? Para a criação de classes e objetos, algo muito citado nas comunidades de programação, é que o melhor padrão para se usar é o CamelCase. O argumento é que em todo o lugar de um código que houver algo escrito em CamelCase, fica explícito que aquilo se trata de uma instância de uma classe. 

Já para a criação de método e atributos, ocorre uma variação no padrão de escrita de acordo com a linguagem que se está programando. Por exemplo, em Ruby, um padrão comum é separar as palavras por "_" (underline), já em Javascript o padrão mais usado é o lowerCamelCase.

Como dito anteriormente, a maneira com que você trabalha seus padrões vai depender de muitos fatores, porém, é essencial que se adaptar à algum deles e mater uma base firme para escrita de código.

#### Objeto/Instância de Classe:

Partindo de uma abordagem mais real, um objeto pode ser tratado como algo vivo e já definido dentro de uma aplicação. Ele não é apenas uma abstração ou conceito classificativo, o objeto, diferente da classe, já possui uma lista atributos definidos e pode usufruir de todos os métodos públicos de sua classe, além de poder se comunicar com outros objetos, seja da mesma classe ou de outras.

Com a criação da classe "Cars", fica mais fácil entender o conceito de objeto. Um exemplo de objeto, ou instância da classe "Cars", seria um carro com modelo Fusca e ano de fabricação 1979. A partir deste exemplo, podemos definir um objeto que contém atributos próprios e pode usufruir de todos os métodos definidos dentro da classe "Cars", como "turn on" e "turn off", e ainda se comunicar com qualquer outro objeto dentro de uma aplicação.

Para instanciar uma classe, ou criar um objeto, usufruímos de um construtor. Em breve será abordardo o que são os construtores e como devemos usá-los em Javascript.

#### Mensagem:	

Mensagens definem a maneira com que nos comunicamos com um objeto, ou basicamente, a invocão de um metódo deste objeto. Veja um exemplo simples de invocação de método.

```javascript
var fusca = new Cars('Fusca', 1979);

fusca.turnOn();
```

Podemos também nos comunicar enviando mensagens entre objetos. O objeto Fusca, que foi citado anteriormente, poderia  receber uma mensagem de um outro objeto da classe "People" invocando seu método "turn on". Esta mensagem faria com que o método "turn on" do objeto Fusca fosse ativado no contexto executado. Veja um exemplo:

```javascript
var fusca = new Cars('Fusca', 1979) // instancia um objeto através da classe "Cars"
var john = new People('John'); // instancia um objeto através da classe "People"

john.car = fusca; // define que o atributo "car" será o objeto fusca
john.car.turnOn(); // ativa o metódo do objeto herdado através da instancia da classe "Cars"
```

Neste exemplo, criamos o objeto John e definimos que seu atributo "car" será outra instância de objeto. Assim podemos enviar uma mensagem através de John para ligar seu carro fusca, usufruindo do método "turn on".

#### Atributos/Propriedades:	

Os atributos são valores únicos e formam a estrutura de dados de uma classe. Dentro de um objeto, são denominadoscomo propriedades do objeto. Cada atributo da classe, ou propriedade do objeto possui um valor, este por sua vez, pode tomar a forma de uma variável ou uma função. Quando função torna-se um método.

Na forma de variáveis, os atributos são armazenadas em pares contendo nome-valor e possuem um tipo. Este tipo pode ser uma "string", "número (inteiro ou float)" ou um "array" (coleção de dados).

Dentro da classe "Cars" temos, por exemplo, o atributo "model", que pode ser do tipo String. A partir da criação deste atributo, todos os objetos, ou instâncias criadas a partir desta classe, poderão ter um atributo "model".

Em Javascript, este é o trecho do código da classe "Cars" onde definimos seus atributos:

```javascript
this.model = model;
this.manufacturingDate = manufacturingDate;
```

Podemos usufruir de dois tipos de atributos, os estáticos e dinâmicos. Atributos estáticos são atributos os que são definidos dentro do escopo da classe e não usufruem do construtor para setá-los. Já os atributos dinâmicos são setados através de parâmetros e definidos no objeto através do construtor.

Exemplo de atributo estático:

```javascript
function Cars() {
	this.wheels = 4;
};
``` 

Exemplo de atributo dinâmico:

```javascript
function Cars(wheels) {
	this.wheels = wheels;
};
```

No primeiro exemplo, estamos definindo que o atributo "wheels" da classe "Cars" é um valor estático, ou seja, já está definido dentro do seu escopo, e independente da instancia de objeto que fizermos, seu valor será 4.

Já no segundo exemplo, definimos o valor de wheels apenas quando instanciamos um objeto e passamos o valor do atributo a partir do construtor.

***OBS:*** Em linguagens não tipadas, não precisamos definir o tipo do atributo, pois o tipo do atributo é determinado quando definido o valor ao criar o objeto.

#### Métodos:

Os métodos são definições que executam determinado procedimento ou função e ajudam à definir as habilidades que a classe terá. É comum que um método receba argumentos, ou seja, parâmetros para que o mesmo possa ser executado de uma forma mais genérica usufruindo de uma lógica dependente do parâmetro.

Para que um método seja executado o mesmo deve ser invocado. Os métodos podem ser invocados a partir de outro método dentro do objeto, ou durante a execução do programa. A partir do momento que você instância uma classe você herda desta classe todos os seus métodos, podendo assim invocar os métodos pertencentes ao objetos. A invocação de um método ocorre através do envio de mensagens entre os objetos. Cada invocação de método deve ser pertencente ao objeto em si e não de outro objeto.

Citando ainda o exemplo do objeto da classe Carro de modelo Fusca. Este mesmo objeto conteria todos os métodos da sua classe, ou seja, habilidades de acelerar, freiar, abrir as portas, ligar, etc.

Uma dica importante para a criação de métodos é em relação ao tempo verbal empregado ao descrever um métodos. Sempre use verbos que indiquem ações quando for definir um método, como no exemplo acima.

E este é o trecho de código da classe Carros que usamos para definir seu método "acelerar":

```javascript
Cars.prototype.turnOn = function() {
	console.log('car is on!')
};
```

#### Construtor:

Construtores são a maneira com que instanciamos uma classe, ou seja, criamos um objeto. Quando definimos uma classe especificamos os atributos que esta contém e quais são os tipos deste atributos. Por exemplo, na classe Carros temos um atributo modelo que é do tipo String e um atributo ano de fabricação que é do tipo Number. Em linguagens não tipadas, não é preciso especificar o tipo do atributo.

Porém, ao especificar os atributos de uma classe você não está criando de fato estes atributos, você apenas está comunicando ao seu sistema quais atributos esta classe terá. A criação em si do atributo só será definida no construtor, ou seja, no momento que você instanciar sua classe.

Para instanciarmos a classe Carros com um construtor em Ruby, usaríamos um código como esse:

```javascript
fusca = Carro.new('Fusca', 1979)
```

A partir de um construtor acabamos de criar nosso objeto Fusca, que é uma instância da classe Carros, passando os parâmetros "nome" do tipo String, e "anoDeFabricacao" do tipo Number.

#### Namespaces:	

#### Herança:

#### Herança Múltipla:

#### Encapsulamento/Closure:

#### Polimorfismo:

#### Interfaces:

### Artigos e Referências

- http://pt.wikipedia.org/wiki/Orienta%C3%A7%C3%A3o_a_objetos
- http://www.hardware.com.br/artigos/programacao-orientada-objetos/
- http://www.training.com.br/lpmaia/pub_prog_oo.htm
- http://javascriptbrasil.com/2013/10/07/objetos-javascript-em-detalhe/
- http://www.abequar.net/objetos-funcoes-e-classes-em-javascript/
- https://developer.mozilla.org/pt-PT/docs/Javascript_orientado_a_objetos
- http://tableless.com.br/javascript-objetos-literais-vs-funcoes-construtoras/
- http://jcemer.com/construtores-em-javascript.html
