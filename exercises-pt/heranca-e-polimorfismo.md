# Herança e Polimorfismo

1. Crie uma classe `Animal` com um método `emitirSom()` que imprime "Som do animal". Crie classes `Cachorro` e `Gato` que herdam de Animal, e sobrescrevam o método `emitirSom()` para imprimir o som correspondente.

2. Crie uma classe `FormaGeometrica` com um método `calcularÁrea` que retorna 0. Crie classes `Círculo` e `Quadrado` que herdam de `FormaGeometrica`, e implementem o método `calcularÁrea` de acordo com a forma.

3. Crie uma classe `Veículo` com um método `acelerar()` que imprime "Veículo acelerando". Crie as classes `Carro` e `Moto` que herdam de Veículo, e sobrescrevam o método `acelerar()` para imprimir mensagens específicas.

4. Crie uma classe `Funcionário` com atributos `nome` e `salário`. Crie uma classe `Gerente` que herda de `Funcionário` e adiciona um atributo `setor`. Sobrescreva o método `toString()` em ambas as classes para exibir os detalhes.

5. Crie uma hierarquia de classes para modelar um sistema de transporte público. Comece com uma classe base `Transporte` e crie classes `Ônibus`, `Metrô` e `Trem` que herdam dela. Cada classe deve ter métodos e atributos relevantes para o tipo de transporte, e você deve usar o conceito de polimorfismo para criar um array de objetos Transporte que pode conter instâncias de todas as subclasses.