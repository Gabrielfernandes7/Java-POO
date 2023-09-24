# Abstração

Processo de simplificar objetos complexos, identidicando as características relevantes.

Criação de classes abstratas

```java
abstract class Forma {
    abstract double calcularArea();
}

class Retangulo extends Forma {
    private double comprimento;
    private double largura;

    public Retangulo(double comprimento, double largura) {
        this.comprimento = comprimento;
        this.largura = largura;
    }

    @Override
    double calcularArea() {
        return comprimento * largura;
    }
}

class Circulo extends Forma {
    private double raio;

    public Circulo(double raio) {
        this.raio = raio;
    }

    @Override
    double calcularArea() {
        return Math.PI * raio * raio;
    }
}

public class ExemploAbstracao {
    public static void main(String[] args) {
        Forma forma1 = new Retangulo(5, 3);
        Forma forma2 = new Circulo(4);

        System.out.println("Área do Retângulo: " + forma1.calcularArea());
        System.out.println("Área do Círculo: " + forma2.calcularArea());
    }
}
```
