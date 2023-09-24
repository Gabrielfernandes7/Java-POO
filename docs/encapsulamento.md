# Encapsulamento

O encapsulamento é um conceito fundamental POO que permite controlar o acesso aos atributos de uma classe. 

## Benefícios do `Encapsulamento`

Encapsular é fundamental para que o seu sistema seja suscetível a mudanças, pois não precisamos mudar uma regra de negócio em vários lugares, mas sim em um único lugar, já que a regra está encapsulada.

- Controlar o acesso dos seus métodos e atributos por meio dos modificadores `public` e `private`.

- Escrever métodos de acesso a atributos do tipo Getters e Setters

- Escrever construtores para suas classes

- Utilizar variáveis para seus métodos estáticos

## Exemplo de Encapsulamento de atributos

Aqui está um exemplo simples de como aplicar encapsulamento em Java:

```java
public class Produto {
    private String nome;
    private double preco;

    // Contrutor
    public Produto(String nome, double preco) {
        this.nome = nome;
        this.preco = preco;
    }

    // Métodos getters e setters para acessar e modificar os atributos encapsulados...
    public void setNome(String nome) {
        this.nome = nome;
    }

    public String getNome() {
        return nome;
    }
}
```

No arquivo main:

```java
public class Produto {
    public static void main(String[] args) {

        // referência Produto para o objeto produto1
        Produto produto1 = new Produto();

        // chamado os métodos de acesso
        produto1.setNome("Manteiga");
        System.out.println("O produto é: " + produto1.getNome());
    }
}
```

## Exemplo de Encapsulamento em métodos

```java
class Cliente	{
    private	String	nome;
    private	String	endereco;
    private	String	cpf;
    private int	idade;

    public voidmudaCPF(String cpf) {
        validaCPF(cpf);
        this.cpf = cpf;
    }

    private	void validaCPF(String cpf) {
        /*
            método não precisa ser chamado em "manualmente", 
            já que automáticamente ele validará o cpf dentro da própria 
            classe, dessa forma evitando repetições na hora de chamar 
            o método
        */
    }
}
```