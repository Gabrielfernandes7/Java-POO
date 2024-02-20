# Interface

- Diferença entre `herança` e `implementação`

As interfaces desempenham um papel fundamental para na criação de contratos entre as classes, permitindo que você defina um conjunto de métodos que as classes que implementam essa interface devem seguir.

As interfaces reduzem o acoplamento entre as classes, tornando o sistema mais fácil de manter e modificar.

```java
// Definição de uma interface
interface Veiculo {
    void acelerar();
    void frear();
}

// Classe que implementa a interface Veiculo
class Carro implements Veiculo {
    @Override
    public void acelerar() {
        System.out.println("O carro está acelerando.");
    }

    @Override
    public void frear() {
        System.out.println("O carro está freando.");
    }
}

// Classe que implementa a interface Veiculo de forma diferente
class Bicicleta implements Veiculo {
    @Override
    public void acelerar() {
        System.out.println("A bicicleta está pedalando.");
    }

    @Override
    public void frear() {
        System.out.println("A bicicleta está freando.");
    }
}
```
