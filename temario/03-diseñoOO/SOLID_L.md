# Sustitución de Liskov

Los objetos de una clase derivada deben poder reemplazar a los objetos de la clase base sin afectar la corrección del programa. En otras palabras, si una clase S hereda de una clase T, entonces un objeto de la clase T debe poder ser reemplazado por un objeto de la clase S sin alterar las propiedades deseables del programa.

<div align="center">

![](/images/modelosUML/modelosUML/liskovEIT.svg)

| |Base|a|b|
|-|:-:|:-:|:-:|
*parámetros*|[0..30]|[-300..300]|[0..3]
*resultados*|[0..70]|[0..7]|[-70..70]

</div>

```java
public class Base {
    public int m(int x) {
        assert x >= 0 && x <= 30 : "Input out of range";
        return x * 2;
    }
}

public class SustituibleDerivada extends Base {
    @Override
    public int m(int x) {
        assert x >= -300 && x <= 300 : "Input out of range";
        return Math.abs(x) / 100;
    }
}

public class InsustituibleDerivada extends Base {
    @Override
    public int m(int x) {
        assert x >= 0 && x <= 3 : "Input out of range";
        return x * -20;
    }
}

public class Cliente {
    public static void main(String[] args) {
        Base base = new Base();
        SustituibleDerivada sustituible = new SustituibleDerivada();
        InsustituibleDerivada insustituible = new InsustituibleDerivada();

        System.out.println("Base m(15): " + base.m(15));

        System.out.println("SustituibleDerivada m(15): " + sustituible.m(15));
        System.out.println("SustituibleDerivada m(-100): " + sustituible.m(-100));

        try {
            System.out.println("InsustituibleDerivada m(15): " + insustituible.m(15));
        } catch (AssertionError e) {
            System.out.println("InsustituibleDerivada m(15): Error - " + e.getMessage());
        }

        System.out.println("InsustituibleDerivada m(2): " + insustituible.m(2));
    }
}

```

|Se cumple cuando se redefine un método en una derivada reemplazando su precondición por una más débil y su postcondicion por una más fuerte|
|-|
Barbara Liskov, *Principio de Sustitución*
|La manera más sencilla para detectar violaciones en el principio de sustitución de Liskov es observando si los métodos sobrescritos en una clase hija tienen el comportamiento esperado.|
Una forma muy común de violación del LSP suele ser cuando los métodos sobreescritos de una clase hija devuelven un null o lanzan una excepción
