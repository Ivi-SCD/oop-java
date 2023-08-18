<div align="center">
  
  ![PROGRAMAÇÃO ORIENTADA A OBJETOS](https://github.com/Ivi-SCD/poo-java/assets/81643916/14e08a34-7c21-4a8c-9b83-1ca6333257ea)
   
  [![License MIT](https://img.shields.io/github/license/Ivi-SCD/poo-java?style=for-the-badge&logo=License")](https://github.com/Ivi-SCD/poo-java/blob/main/LICENSE)
  ![Stars](https://img.shields.io/github/stars/Ivi-SCD/poo-java?style=for-the-badge&logo=License")
  ![Forks](https://img.shields.io/github/forks/Ivi-SCD/poo-java?style=for-the-badge&logo=License")
  
</div>

 #

Esse repositório foi criado com o intuito de **ajudar estudantes que desejam
iniciar seus estudos em Programação Orientada a Objetos** ou melhorar suas 
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
  * [Métodos Estáticos e de Instância](#mei)
  * [Classes Genéricas (Generics)](#cg)
  * [Construtores Chaining](#cc) 
  * [Classes Internas (Inner Classes)](#ci)
* [Encapsulamento e Modificadores de Acesso](#ema)
  * [Visibilidade de membros (public, private, protected)](#vm)
  * [Métodos getters, setters e Construtor](#mgsc)
* [Herança e Polimorfismo](#hp)
  * [Herança de Classes, Subclasses e Sobrescrita de Métodos](#hcssm)
  * [Polimorfismo](#p)

#

#### Lista de Exercios
* [Classes e  Objetos](https://github.com/Ivi-SCD/poo-java/tree/main/exercises-pt/classes-e-objetos.md)
* [Encapsulamento e Modificadores de Acesso](https://github.com/Ivi-SCD/poo-java/tree/main/exercises-pt/encapsulamento-e-modificadores.md)
* [Herança e Polimorfismo](https://github.com/Ivi-SCD/poo-java/tree/main/exercises-pt/heranca-e-polimorfismo.md)

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

Os 4 principais pilares da Programação Orientada a Objetos são **Abstração, Encapsulamento,
Herança e Polimorfismo.**

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

#

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

### <a name="mei">Métodos Estáticos e de Instância</a>

Na Programação Orientada a Objetos, os métodos em uma classe podem ser categorizados em dois tipos principais: **métodos estáticos e métodos 
de instância**.

#### Métodos Estáticos

Os métodos estáticos, também conhecidos como métodos de classe, **pertencem à classe em vez de pertencer a instâncias individuais dessa classe**.
Eles são definidos com o modificador `static`. Métodos estáticos não podem acessar ou modificar atributos de instância, pois não estão vinculados 
a nenhuma instância específica. Eles são invocados usando o nome da classe, não uma instância.

Os métodos estáticos possui algumas características:

- Eles podem ser chamados diretamente usando o nome da classe, sem a necessidade de criar uma instância.
- Eles são frequentemente usados pra operações que se aplicam a toda a classe, como utilitários e funções auxiliares.
- Eles não podem acessar variáveis de instância diretamente, mas podem acessar variáveis estáticas (também conhecidas como variáveis de classe) e
outros métodos estáticos.

Exemplo de método estático:

```java
public class MathUtils {
    // Exemplo de Método Estático que retorna soma dois valores
    public static int soma(int a, int b) {
        return a + b;
    }
}
```


#### Métodos de Instância

Métodos de instância, por outro lado, estão **vinculados a objetos específicos criados a partir de uma classe**. Eles podem acessar e modificar 
atributos de instância e também podem chamar outros métodos de instância e métodos estáticos da mesma classe.

Os métodos de instância são definidos sem o modificador `static`. Eles são chamados em uma instância específica da classe, usando a notação 
de ponto após a instância.

Exemplo de método de instância:

```java
public class Circulo {
    private double raio;

    public Circulo(double raio) {
        this.raio = raio;
    }

    // Exemplo de Método de Instância que calcula a área de um circulo
    public double calcularArea() {
        return Math.PI * raio * raio;
    }
}
```
Uso Adequado de Métodos Estáticos e de Instância:

- Use métodos estáticos para funcionalidades que não dependem do estado da instância e não precisam de acesso a atributos
de instância.
- Use métodos de instância para operações que envolvem o estado da instância e requerem acesso aos atributos de instância.
- Lembre-se de que os métodos estáticos não podem ser sobrescritos, pois não estão associados a instâncias.
- Ao entender a diferença entre métodos estáticos e de instância, você pode escolher o tipo certo de método para a tarefa
em questão e criar classes mais coesas e eficientes.

#

### <a name="cg">Classes Genéricas (Generics)</a>

As classes genéricas são um recurso fundamental na linguagem Java que permitem criar componentes reutilizáveis que podem 
trabalhar com diferentes tipos de dados, mantendo a segurança de tipos em tempo de compilação. Isso ajuda a evitar erros 
relacionados a tipos e promove a reutilização de código.

#### Declaração de Classe Genérica

A declaração de uma classe genérica é feita usando a sintaxe Classe<T>, onde T é um parâmetro de tipo genérico que representa 
o tipo que será fornecido quando a classe for instanciada.

```java
public class MinhaClasse<T> {
    // Atributos, métodos, construtores, etc.
}
```

#### Uso de Classes Genéricas

As classes genéricas permitem que você escreva código que funciona com tipos específicos sem precisar criar uma classe 
separada para cada tipo. Isso é especialmente útil para coleções, estruturas de dados e algoritmos que não dependem de um 
tipo específico.

##### Exemplo de Uso: Lista Genérica
Suponha que você queira criar uma lista que possa armazenar qualquer tipo de dado. Com uma classe genérica, você pode criar uma estrutura de dados flexível e reutilizável.

```java
public class MinhaLista<T> {
    private Object[] elementos;
    private int tamanho;

    public MinhaLista(int capacidade) {
        elementos = new Object[capacidade];
        tamanho = 0;
    }

    public void adicionar(T elemento) {
        if (tamanho < elementos.length) {
            elementos[tamanho] = elemento;
            tamanho++;
        }
    }

    public T obter(int indice) {
        if (indice >= 0 && indice < tamanho) {
            return (T) elementos[indice];
        }
        throw new IndexOutOfBoundsException("Índice inválido");
    }
}
```

Nesse exemplo, a classe `MinhaLista` é genérica, permitindo que você crie listas de qualquer tipo.

Instanciando uma Lista Genérica

```java
MinhaLista<Integer> listaDeInteiros = new MinhaLista<>(10);
MinhaLista<String> listaDeStrings = new MinhaLista<>(5);

listaDeInteiros.adicionar(42);
listaDeStrings.adicionar("Olá, Mundo!");

Integer numero = listaDeInteiros.obter(0);
String texto = listaDeStrings.obter(0);
Restrições e Limitações
```

É possível adicionar restrições aos tipos que podem ser usados em uma classe genérica. Isso é feito usando a palavra-chave `extends` ou `super`.

```java
public class MinhaClasse<T extends Number> {
    // ...
}
```

Isso limita os tipos que podem ser usados a subclasses da wrapper class `Number`.


#

### <a name="cc">Construtores Chaining</a>

Construtores chaining, também conhecido como encadeamento de construtores, é uma técnica usada em programação para criar construtores 
que chamam outros construtores da mesma classe. Isso ajuda a simplificar a criação de objetos com diferentes configurações, tornando 
o código mais flexível e legível.

#### Sintaxe de Encadeamento de Construtores

A ideia básica do encadeamento de construtores é que um construtor chame outro usando a palavra-chave this. O construtor chamado deve 
estar definido na mesma classe e deve ter uma assinatura que corresponda aos argumentos passados.

```java
public class MinhaClasse {
    private int parametro1;
    private int parametro2;

    public MinhaClasse(int parametro1) {
        this(parametro1, 0); // Chama o outro construtor da classe
    }

    public MinhaClasse(int parametro1, int parametro2) {
        this.parametro1 = parametro1;
        this.parametro2 = parametro2;
    }
}
```

Nesse exemplo, o primeiro construtor chama o segundo construtor passando um valor padrão para `parametro2`.


#

### <a name="ci">Classes Interas (Inner Classes)</a>

As classes internas, também conhecidas como classes aninhadas, são classes definidas dentro de outras classes em Java. 
Elas podem ser úteis para melhorar a organização do código além de também encapsular funcionalidades relacionadas. 
Existem quatro tipos principais de classes internas em Java:

#### Classe Interna de Membro (Member Inner Class):

Uma classe interna de membro é **definida diretamente dentro de outra classe e tem acesso aos membros (campos e métodos) da 
classe externa**, incluindo aqueles marcados como privados. Para criar uma instância da classe interna de membro, você precisa 
primeiro criar uma instância da classe externa.

```java
public class Outer {
    private int outerField;

    public class Inner {
        private int innerField;

        public void doSomething() {
            outerField = 10;
            innerField = 5;
        }
    }
}
```

#### Classe Interna Estática (Static Nested Class):

Uma classe interna estática é semelhante a uma classe de membro, mas é definida como estática. Isso significa que ela não 
tem acesso aos membros não estáticos da classe externa, mas pode ser instanciada diretamente sem a necessidade de uma instância 
da classe externa.

```java
public class Outer {
    private static int outerField;

    public static class Nested {
        private int nestedField;

        public void doSomething() {
            outerField = 10;
            nestedField = 5;
        }
    }
}
```

#### Classe Local (Local Inner Class):

Uma classe local é definida dentro de um método ou bloco de código. Ela tem acesso aos membros da classe externa e também aos 
parâmetros e variáveis finais do método ou bloco onde está definida.

```java
public class Outer {
    private int outerField = 10;

    public void createLocalInner() {
        final int localVar = 5;

        class LocalInner {
            public void doSomething() {
                outerField = 20;
                System.out.println(localVar);
            }
        }

        LocalInner inner = new LocalInner();
        inner.doSomething();
    }
}
```

#### Classe Anônima (Anonymous Inner Class):

Uma classe anônima é uma forma especial de classe local que é definida e instanciada em uma única expressão. Elas são frequentemente 
usadas para implementar interfaces ou extender classes abstratas de forma concisa.

```java
public class Outer {
    public void createAnonymousInner() {
        Runnable runnable = new Runnable() {
            @Override
            public void run() {
                System.out.println("Anonymous inner class running");
            }
        };

        Thread thread = new Thread(runnable);
        thread.start();
    }
}
```

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

Neste exemplo, a classe `Pessoa` encapsula os atributos `nome` e `idade`. Os métodos `getters e setters` permitem o 
acesso  controlado a esses atributos, enquanto o construtor é usado para inicializar os objetos da classe.

## <a name="hp">Herança e Polimorfismo</a>

Neste tópico darei mais atenção e explicarei com o maior número de detalhes possível pois são dois conceitos essenciais
para a dominação desse paradigma. Dominando esses conceitos fica mais fácil de fazer quaisquer coisas envolvendo esse paradigma 
além de também permitir o avanço no estudo de recursos mais avançados da linguagem tal como implementação de programas mais 
eficientes e complexos.

A herança e o polimorfismo são dois mecanismos importantíssimos em linguagens que possuem o paradigma de orientação a
objetos. Na teoria a herança é um **conceito em que uma classe (subclasse) é criada com base em outra classe já existente 
(superclasse)**. A subclasse herda os atributos e métodos da superclasse, permitindo reutilização de código e estabelecendo 
uma relação de "é um". Já o Polimorfismo é um princípio que **permite que objetos de diferentes classes sejam tratados de 
forma uniforme através de interfaces comuns**. Isso possibilita a substituição de implementações e a execução de métodos de
maneiras específicas para cada classe, promovendo flexibilidade e reutilização de código.

### <a name="hcssm">Herança de Classes, Subclasses e Sobrescrita de Métodos</a>

A herança como já explicado, é um mecanismo que permite criar uma nova classe (subclasse ou classe derivada) com base em uma 
classe existente (superclasse ou classe base). A subclasse herda os atributos e métodos da superclasse, além de poder adicionar 
novos atributos e métodos ou sobrescrever os existentes.

#

#### Criando uma subclasse em Java utilizando herança

Para criar uma subclasse em Java, utilizamos a palavra-chave `extends`. A subclasse **herda todos os membros (atributos e métodos 
não privados) da superclasse**.

```java
//Superclasse
public class Animal {
    void emitirSom() {
       System.out.println("Som genérico de um animal");
   }
}
```

```java
//Subclasse
public class Cachorro extends Animal {
    // ...
}
```

No exemplo acima a classe `Cachorro` herdou as mesmas características que a Classe `Animal` definiu no seu corpo, obtendo a relação de
um Cachorro **É UM** Animal. Além disso, os membros herdados de uma superclasse podem ser acessados diretamente em uma subclasse. Eles
mantêm a visibilidade original (public, protected) na subclasse.

#

#### Métodos de Sobrescrita

Em muitos casos, você pode querer **modificar o comportamento de um método herdado na subclasse**. Isso é feito através da sobrescrita de método, 
usando a anotação `@Override`.

```java
public class Cachorro extends Animal {
    @Override
    void emitirSom() {
        System.out.println("Latido de um cachorro");
    }
}
```

Nesse exemplo o método que existia na superclasse foi herdado pela subclasse e sobrescrito, alterando assim o seu comportamento original.

#

#### Palavra-chave `super`

A palavra-chave  `super` é **usada para chamar construtores e métodos da superclasse**. Isso é útil para evitar ambiguidades entre membros 
herdadose membros da própria classe.

Utilize a herança quando houver uma relação "é um" clara entre as classes. Evite herança apenas por conveniência, priorizando a composição 
e a modularização.

Exemplo Prático:

```java
public class Veiculo {
    int velocidade;

    void acelerar() {
        // Lógica para acelerar
    }
}
```

Nesse exemplo a classe `Veiculo` possui um atributo velocidade e um método `acelerar()` podendo receber uma lógica para essa ação.

```java
public class Carro extends Veiculo {
    int numPortas;

    @Override
    void acelerar() {
        super.acelerar();
        // Lógica específica para carros
    }
}
```

Aqui a Classe `Carro` herda todos os atributos (`velocidade`) e métodos (`acelerar()`) da superclasse (`Veiculo`), além disso essa Classe
também possui um atributo específico da subclasse que é o `numPortas`, além de sobrescrever o método `acelerar()` chamando a lógica que já
existe na superclasse com a palavra-chave `super` e complementando uma lógica adicional respeitada apenas pelas Classes Carro.

#### Dicas e Boas Práticas:

* Use herança quando houver uma relação lógica e natural entre as classes.
* Evite hierarquias profundas e complexas de herança.
* Prefira [composição](https://www.devmedia.com.br/entendendo-o-conceito-de-heranca-e-composicao/25456) quando a relação não for claramente "é um".
* Sempre use a anotação `@Override` ao sobrescrever métodos.
* Sempre utiliza a palavra-chave `super`para acessar membros da superclasse.

#

### <a name="p">Polimorfismo</a>

Nesta seção, vamos mergulhar fundo no conceito de polimorfismo em Programação Orientada a Objetos (P.O.O.) usando a linguagem Java. 
O polimorfismo é um dos pilares da P.O.O. que **permite que objetos de diferentes classes sejam tratados de maneira uniforme através de 
interfaces comuns**. Vamos explorar suas variantes, implementações e benefícios em detalhes.

#

#### Tipos de Polimorfismo

**a) Polimorfismo de Sobrecarga**

É quando um único método possui várias implementações, diferenciadas por parâmetros. Isso é conhecido como sobrecarga de método.

**b) Polimorfismo de Substituição**

Ocorre quando uma subclasse substitui o método de sua superclasse. Isso é conhecido como sobrescrita de método (Tratado anteriormente 
na seção de Herança), utilizando a anotação `@Override`.

#

#### Polimorfismo de Sobrecarga

A sobrecarga permite que um método tenha diferentes assinaturas (número ou tipo de parâmetros). O compilador seleciona automaticamente 
a versão correta do método com base nos argumentos passados.

#

#### Polimorfismo de Substituição

A substituição de método ocorre quando uma subclasse implementa um método com a mesma assinatura da superclasse. O método da subclasse 
substitui o método da superclasse.

#

#### Exemplo:

```java
class Forma {
    void desenhar() {
        // Lógica para desenhar uma forma
    }
}

class Circulo extends Forma {
    @Override
    void desenhar() {
        // Lógica para desenhar um círculo
    }
}

class Quadrado extends Forma {
    @Override
    void desenhar() {
        // Lógica para desenhar um quadrado
    }
}
```

Neste exemplo, temos uma hierarquia de classes que ilustra o polimorfismo. A classe base `Forma` define 
um método chamado `desenhar()`, que tem uma implementação genérica para desenhar qualquer forma. As classes 
`Circulo` e `Quadrado` são subclasses da classe `Forma` e sobrescrevem o método `desenhar()` com lógicas específicas 
para desenhar um círculo e um quadrado, respectivamente.

Aqui está como esse exemplo funciona de forma mais detalhada:

1. A classe base `Forma`:
  * Ela possui um método `desenhar()` que fornece uma implementação genérica para desenhar uma forma qualquer.
2. A classe `Circulo`:
  * Esta classe estende a classe `Forma`.
  * Ela sobrescreve o método desenhar() com uma lógica específica para desenhar um círculo.
3. A classe `Quadrado`:
  * Esta classe também estende a classe `Forma`.
  * Ela sobrescreve o método `desenhar()` com uma lógica específica para desenhar um quadrado.
    
Agora, veremos como o polimorfismo entra em ação:

```java
public class Main {
    public static void main(String[] args) {
        Forma forma1 = new Circulo();
        Forma forma2 = new Quadrado();
        
        forma1.desenhar(); // Chamada ao método desenhar() da classe Circulo
        forma2.desenhar(); // Chamada ao método desenhar() da classe Quadrado
    }
}
```

Neste trecho, criamos instâncias das classes `Circulo` e `Quadrado` e as atribuímos a variáveis do tipo `Forma`. 
Quando chamamos o método `desenhar()` em cada uma dessas variáveis, o Java utiliza a implementação correta do 
método para cada tipo de forma. Isso demonstra o polimorfismo, onde objetos de diferentes classes são tratados 
de maneira uniforme através da classe base, permitindo a flexibilidade e a extensibilidade do código.

#

#### Dicas e Boas Práticas:
* Utilize interfaces e herança para promover polimorfismo.
* Utilize a anotação `@Override` ao substituir métodos.
* Entenda quando usar sobrecarga e substituição.

Para finalizarmos, verificamos nesta seção que o Polimorfismo é de extrema importância para a construção de
sistemas flexíveis e escaláveis. Ele nos traz diversos benefícios ao nosso código como reutilização de código,
escrita de código mais genérico, implementação de design patterns como [Strategy](https://github.com/Ivi-SCD/gof-design-patterns#strategy) 
e [Factory](https://github.com/Ivi-SCD/gof-design-patterns#factory) além de também facilitar a manutenção e 
extensão do sistema.
