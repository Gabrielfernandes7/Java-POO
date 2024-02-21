# Polimorfismo

É um conceito na POO que permite que permite que os objetos de diferentes classes
sejam tratados de maneira uniforme. Isso é possível devido a capacidade das subclasses
de herdar comportamentos da superclasse e substituir ou estender esses comportamentos.

```java
class Animal {
    void fazerSom() {
        System.out.println("Animal faz algum som");
    }
}

class Cachorro extends Animal {
    @Override
    void fazerSom() {
        System.out.println("Cachorro late: Woof Woof!");
    }
}

class Gato extends Animal {
    @Override
    void fazerSom() {
        System.out.println("Gato mia: Meow Meow!");
    }
}

public class ExemploPolimorfismo {
    public static void main(String[] args) {
        Animal meuAnimal;

        meuAnimal = new Cachorro();
        meuAnimal.fazerSom(); // Chama o método fazerSom() da classe Cachorro

        meuAnimal = new Gato();
        meuAnimal.fazerSom(); // Chama o método fazerSom() da classe Gato
    }
}
```

## Polimorfismo de sobrecarga

É quando uma classe possui vários métodos com o mesmo nome

```java
class Calculadora {
    int somar(int a, int b) {
        return a + b;
    }

    double somar(double a, double b) {
        return a + b;
    }
}

public class ExemploPolimorfismoSobrecarga {
    public static void main(String[] args) {
        Calculadora calc = new Calculadora();

        int resultadoInt = calc.somar(5, 10);
        System.out.println("Soma de inteiros: " + resultadoInt);

        double resultadoDouble = calc.somar(3.5, 2.5);
        System.out.println("Soma de doubles: " + resultadoDouble);
    }
}
```

O java define qual método chamar com base no argumento passado.
