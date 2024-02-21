# Construtor

Quando utilizamos a palavra `new` estamos construindo um objeto. Sempre que o `new` é chamado ele executa o construtor da classe.

- O construtor tem o mesmo nome da classe

- Construtor não é um método

```java
class Conta	{
    String titular;
    int	numero;
    double saldo;

    //	construtor
    Conta()	{
        System.out.println("Construindo	uma	conta.");
    }
}
```

## Necessidade de se ter um construtor

Dar a possiblidade ou obrigar o usuário de uma classe a passar os argumentos para o objeto durante a sua criação.

Um construtor com argumentos permite que o programador personalize a inicialização de um objeto.

O construtor com argumentos torna nosso código mais legível

Pattern `Factory`

## Métodos e atributos estáticos com Java

Métodos e atributos estáticos são úteis quando você deseja funcionalidades globais que não dependem de instâncias individuais da classe e quando precisa compartilhar dados ou comportamentos entre todas as instâncias

Exemplo prática do porquê que eu precisaria de mombros estático:

- Definir a URL do banco de dados
- Definir a configuração global de uma aplicação