# Herança

É um conceito fundamental da POO que permite uma classe herde métodos
e atributos de outra classe.

```java
// classe pai
class Animal {
    protected String nome;
    
    public void fazerBarulho() {
        // Executa método fazerBarulho
    }
}

// Classe filho
// Classe cachorro herda de Animal
class Cachorro extends Animal {
    @Override
    public void fazerBarulho() {
        // Latir
    }
}
```

## Modificador de acesso `protected`

Quando queremos que as classes filhas possam ter acesso a superclasse,
mas ainda queremos manter um determinado nível de encapsulamento.

Restringe o acesso a outras classes fora da hierarquia.

- Observação: quanto maior o uso de herança maior o nível de acoplamento entre as classes. Por exemplo, vamos imaginar que queremos modificar um atributo na classe-pai, mas essa mudança afetaria todas as classes filhas, logo, se não for do nosso interesse essa mudança em todas as classes, significa que temos um problema. Esse problema podemos resolver com a ajuda das [interfaces](/docs/interfaces/interfaces.md).