# Encapsulamento e Modificadores de Acesso

1. Crie uma classe `Cachorro` com o atributo `nome` (privado) e métodos `getNome` e `setNome` para acessar e definir o nome do cachorro.

2. Crie uma classe `Estudante` com o atributo `nota` (privado). Crie um método `verificarAprovacao()` que retorna "Aprovado" se a nota for maior ou igual a 6, e "Reprovado" caso contrário.

3. Crie uma classe `Funcionário` com o atributo `salário` (privado). Adicione um método `aumentarSalário` que recebe um valor percentual de aumento e ajusta o salário do funcionário.

4. Crie uma classe `ContaBancária` com o atributo `saldo` (privado). Crie um método `sacar()` que permite retirar uma quantia do saldo, mas só se o saldo for suficiente.

5. Crie uma classe `RegistroDeVendas` que mantém um registro privado de vendas mensais. Crie um método `adicionarVenda()` que aceita o valor da venda e o mês, adicionando essas informações ao registro. Crie um método `calcularTotalVendas()` que retorna o total de vendas de todos os meses. Garanta que o registro de vendas não possa ser acessado diretamente de fora da classe.