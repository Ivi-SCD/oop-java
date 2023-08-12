# Programação Orientada a Objetos (P.O.O) 

Esse repositório foi criado com o intuito de ajudar estudantes que desejam
iniciar seus estudos em Programação Orientada a Objetos ou melhorar suas 
habilidades em linguagens que possuem esse paradigma, a principal linguagem
que será utilizada nesse repositório será a Linguagem Java, porém seus conceitos
são facilmente aplicadas a outras linguagens com o mesmo paradigma como o C#.

#

#### Tópicos
* [Introdução](#i)
  *  [O que é Programação Orientada a Objetos?](#oqpoo)
  *  [Vantagens e princípios fundamentais](#vpf)
* [Classes e Objetos](#co)
  * [Definindo classes e objetos](#dco)
  * [Atributos e métodos de classe](#amc)
* [Encapsulamento e Modificadores de Acesso](#ema)
  * [Visibilidade de membros (public, private, protected)](#vm)
   * [Métodos getters, setters e Construtor](#mgsc)
* Herança e Polimorfismo
  * Herança de classes e subclasses
  * Polimorfismo e sobrescrita de métodos

#

## <a name="i">Introdução</a>

### <a name="oqpoo">O que é Programação Orientada a Objetos?</a>

A tão famosa Programação Orientada a Objetos (P.O.O) é um dos vários paradigmas de
programação que se baseia no próprio conceito de "objetos", permitindo a modelagem
e organização de sistemas complexos de forma mais intuitiva e modular. Ela fornece
uma abordagem para projetar e estruturar programas de computador e sistemas em torno
de entidades autônomas chamadas objetos, que representam em geral, elementos do mundo
real ou abstrações. Por exemplo podemos abstrair do mundo real um Telefone Celular e
tornamos ele um objeto para manipulação na linguagem.

```java
public class Telefone {
}
```

#

### <a name="vpf">Vantagens e princípios fundamentais</a>

A Programação Orientada a Objetos (P.O.O.) oferece várias vantagens e se baseia em 
princípios fundamentais que a tornam uma abordagem poderosa para o desenvolvimento 
de software. Aqui vão algumas das principais vantagens e princípios da P.O.O.:

#

**Modularidade**

Os programas são divididos em módulos independentes (classes), o que facilita 
a manutenção e o desenvolvimento de partes específicas do software.

#

**Reutilização de Código**

Um poderoso recurso que nos permite a reutilização de código é o conceito e 
aplicabilidade da herança (assunto que será abordado com mais profundidade mais 
á frente) permite que você reutilize código de classes existentes, 
economizando tempo e esforço na criação de funcionalidades similares.

#

**Abstração**

 A facilidade de abstrair complexidades reduz a dificuldade geral do sistema, 
 tornando-o mais compreensível e gerenciável, podendo nos proporcionar também
 uma escalabilidade vantajosa para o sistema em desenvolvimento.

 #

 **Flexibilidade e Extensibilidade**

 A capacidade de estender e modificar facilmente classes existentes permite adaptar 
 o software a novos requisitos sem grandes alterações, facilitanto também o desenvolvimento
 em ambientes ágeis.

 #

**Polimorfismo**

Esse assunto importantíssimo também será trabalhado com mais detalhes mais à frente
porém no geral, ele permite que diferentes classes implementem o mesmo método de maneiras 
específicas, o que leva a um código mais genérico e flexível.

#

**Encapsulamento**

 Outro conceito que será mais abordado mais adiante, ele permite que haja a proteção dos 
 detalhes internos de uma classe, o que também simplifica a manutenção e evita alterações 
 acidentais ou comportamentos indesejados em partes mais sensíveis do código.

#

Em resumo, a P.O.O. nos traz muitos benefícios em oferecer uma abordagem poderosa para 
desenvolver sistemas de software robustos, organizados e escaláveis. Ela promove uma 
mentalidade voltada para a modelagem do mundo real e ajuda a criar estruturas de código 
que são mais fáceis de entender, manter e expandir.

## <a name="co">Classes e Objetos</a>

Antes de iniciar essa parte gostaria de explicar com mais detalhes a diferença entre
Classes e Objetos. Uma classe sempre é um molde para a criação do objeto, é na Classe
onde são definidos as características do objeto e quais ações esse objeto vai possuir,
um exemplo de Classe no mundo real seria uma Classe chamada de Cachorro, com as 
características de idade e nome e com as ações de latir e andar. Já um Objeto seria
uma instância concreta da classe, ela é a represetação real da entidade Cachorro.

### <a name="dco">Definição de classes e objetos</a>

*Obs: Os atributos e métodos serão explicados no próximo tópico, peço que quando
finalizar a leitura do próximo tópico volte para esta para ter uma melhor compreensão
do assunto e também não deixe de praticar pois a prática é a aliada que nos leva
a excelência.*

**Classe**:

Uma classe em Java é um modelo (Como já explicado, um molde) ou um plano para criar objetos. 
Ela define a estrutura e o comportamento dos objetos que serão criados a partir dela. 
Uma classe é como um molde que define os atributos (características) e os métodos (ações) 
que os objetos desse tipo terão. É importante notar que uma classe é apenas uma descrição, 
e não ocupa espaço na memória.

Exemplo de uma classe em Java:

```java
public class Pessoa {
    // Atributos 
    String nome;
    int idade;

    // Construtor (Método que será explicado mais a frente, mas resumidamente
    // é ele que permite a instanciação dessa Classe).
    public Pessoa(String nome, int idade) {
        this.nome = nome;
        this.idade = idade;
    }

    // Método
    public void saudacao() {
        System.out.println("Olá, meu nome é " + nome + " e tenho " + idade + " anos.");
    }
}
```

**Objeto:**
Um objeto é uma instância concreta de uma classe. Ele representa um único item ou entidade 
que possui características `(atributos)` e pode realizar ações `(métodos)` conforme definido na classe. 
Cada objeto criado a partir de uma classe tem seu próprio conjunto de valores para os atributos.

Exemplo de criação e uso de objetos em Java:

```java
public class Exemplo {
    public static void main(String[] args) {
        // Criando objetos da classe Pessoa
        Pessoa pessoa1 = new Pessoa("Alice", 25);
        Pessoa pessoa2 = new Pessoa("Bob", 30);

        // Chamando métodos nos objetos
        pessoa1.saudacao(); // Saída: Olá, meu nome é Alice e tenho 25 anos.
        pessoa2.saudacao(); // Saída: Olá, meu nome é Bob e tenho 30 anos.

        // Modificando atributos
        pessoa1.idade = 26;
        pessoa1.saudacao(); // Saída: Olá, meu nome é Alice e tenho 26 anos.
    }
}
```
Neste exemplo, a classe `Pessoa` define uma estrutura que contém um `nome` e uma `idade`, juntamente com 
um método `saudacao()` para imprimir uma saudação com base nos atributos. Os objetos `pessoa1` e `pessoa2` 
são instâncias da classe `Pessoa`, cada um com seus próprios valores para os atributos. Eles podem executar 
o método `saudacao()` para se apresentar. Além disso, o exemplo demonstra como modificar o valor do atributo 
`idade` em um dos objetos.

#

### <a name="amc">Atributos e métodos de classe</a>

**Atributos de Classe:**

Os atributos de classe, também conhecidos como variáveis de instância, são as características ou propriedades 
que definem o estado de um objeto. Eles armazenam os valores específicos para cada instância da classe. Os atributos 
representam informações que um objeto possui e podem ser de diferentes tipos de dados, como inteiros, strings, booleanos, 
etc.

Exemplo em Java:

```java
public class Pessoa {
    String nome;   // Atributo de instância
    int idade;     // Atributo de instância
    static int totalPessoas;  // Atributo de classe (estático)

    public Pessoa(String nome, int idade) {
        this.nome = nome;
        this.idade = idade;
        totalPessoas++;
    }
}
```

No exemplo acima, `nome` e `idade` são atributos de instância, ou seja, cada objeto `Pessoa` terá seus próprios valores para 
esses atributos. O atributo `totalPessoas` é um atributo de `classe` (ou `estático`), o que significa que ele é compartilhado por 
todas as instâncias da classe. Ele é usado para rastrear o número total de objetos `Pessoa` criados.


**Métodos de Classe:**
Os métodos de classe são as ações ou comportamentos que um objeto da classe pode executar. Eles são funções definidas na classe 
e podem ser chamados em objetos dessa classe para realizar operações específicas.

Exemplo em Java:

```java
public class Calculadora {
    public static int somar(int a, int b) {
        return a + b;
    }

    public static int subtrair(int a, int b) {
        return a - b;
    }
}
```

Neste exemplo, `somar` e `subtrair` são métodos de classe (estáticos) da classe `Calculadora`. Eles podem ser chamados diretamente 
na classe, 
sem a necessidade de criar uma instância da classe. Por exemplo:

```java
int resultadoSoma = Calculadora.somar(5, 3); // resultadoSoma = 8
int resultadoSubtracao = Calculadora.subtrair(10, 4); // resultadoSubtracao = 6
```

Em resumo, **os atributos de classe definem o estado ou as características dos objetos**, enquanto **os métodos de classe definem o 
comportamento ou as ações que os objetos podem executar**. Os atributos de classe podem ser específicos de cada objeto ou compartilhados 
por todos os objetos da mesma classe, enquanto os métodos de classe realizam operações específicas e podem ser chamados na classe sem 
a necessidade de criar instâncias.

#

### <a name="ema">Encapsulamento e Modificadores de Acesso</a>

*Nesta seção, vamos explorar o conceito de encapsulamento em Programação Orientada a Objetos (P.O.O.), juntamente com os modificadores 
de acesso que controlam a visibilidade dos membros de uma classe.*

#### <a name="vm">Visibilidade de membros (public, private, protected)</a>

Os modificadores de acesso **determinam como os atributos e métodos de uma classe podem ser acessados por outras partes do programa**. 
Os três principais modificadores de acesso são:

* **public**: Membros públicos podem ser acessados a partir de qualquer lugar, seja dentro da classe, subclasses ou outras classes.

* **private**: Membros privados são acessíveis apenas dentro da classe onde foram declarados. Não podem ser acessados diretamente de
  fora da classe.

* **protected**: Membros protegidos são semelhantes aos privados, mas também podem ser acessados por subclasses da classe onde foram
  declarados.

Segue uma tabela para facilitar o entendimento do conceito referente a a visibilidade de cada modificador:

Modificador | Visibilidade
----------- | ------------
     public | Acesso em qualquer lugar.
    private	| Acesso apenas dentro da própria classe.
  protected	| Acesso dentro da classe e subclasses.
  (default)	| Acesso dentro do mesmo pacote.


### <a name="mgsc">Métodos getters, setters e Construtor></a>

Métodos `getters e setters` são **importantíssimos para acessarmos e modificarmos atributos privados de uma classe de maneira controlada
e padronizada**. Além disso, os construtores são usados para inicializar objetos. Aqui estão exemplos de implementação:


```java
public class Pessoa {
    private String nome;
    private int idade;

    // Construtor
    public Pessoa(String nome, int idade) {
        this.nome = nome;
        this.idade = idade;
    }

    // Getter para o nome
    public String getNome() {
        return nome;
    }

    // Setter para o nome
    public void setNome(String nome) {
        this.nome = nome;
    }

    // Getter para a idade
    public int getIdade() {
        return idade;
    }

    // Setter para a idade
    public void setIdade(int idade) {
        this.idade = idade;
    }
}
```

Neste exemplo, a classe `Pessoa` encapsula os atributos `nome` e `idade`. Os métodos `getters e setters` permitem o acesso 
controlado a esses atributos, enquanto o construtor é usado para inicializar os objetos da classe.
