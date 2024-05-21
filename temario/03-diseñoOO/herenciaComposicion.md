# Herencia vs Composición

## Herencia sobre composición

Supongamos una jerarquía de formas geométricas donde todas las formas comparten ciertas propiedades y comportamientos, como calcular el área o el perímetro.

<div align=center>

![](/images/modelosUML/modelosUML/herenciaSobreComposicion.svg)

</div>

En este ejemplo, la herencia es claramente ventajosa porque todas las formas geométricas comparten un conjunto común de comportamientos que pueden ser implementados o sobrescritos según sea necesario: la estructura jerárquica facilita la reutilización del código y logra un diseño más limpio y comprensible.


```java
abstract class Shape {
    public abstract double getArea();
    public abstract double getPerimeter();
}

class Rectangle extends Shape {
    private double width;
    private double height;

    public Rectangle(double width, double height) {
        this.width = width;
        this.height = height;
    }

    @Override
    public double getArea() {
        return width * height;
    }

    @Override
    public double getPerimeter() {
        return 2 * (width + height);
    }
}

class Circle extends Shape {
    private double radius;

    public Circle(double radius) {
        this.radius = radius;
    }

    @Override
    public double getArea() {
        return Math.PI * radius * radius;
    }

    @Override
    public double getPerimeter() {
        return 2 * Math.PI * radius;
    }
}

public class Main {
    public static void main(String[] args) {
        Shape rectangle = new Rectangle(5, 10);
        Shape circle = new Circle(7);

        System.out.println("Rectangle area: " + rectangle.getArea());
        System.out.println("Rectangle perimeter: " + rectangle.getPerimeter());
        System.out.println("Circle area: " + circle.getArea());
        System.out.println("Circle perimeter: " + circle.getPerimeter());
    }
}
```

## Composición sobre herencia

Supongamos que tenemos vehículos que pueden tener diferentes tipos de motores (gasolina, eléctrico, híbrido) y diferentes tipos de transmisión (manual, automática).

<div align=center>

![](/images/modelosUML/modelosUML/composicionSobreHerencia.svg)

</div>

En este caso concreto la composición permite una estructura más simple y flexible al combinar comportamientos mediante la inclusión de objetos, en lugar de heredar de múltiples clases base. Si usamos herencia para modelar este sistema, tendríamos que crear múltiples clases para cada combinación posible de motor y transmisión, lo que resultaría en una jerarquía de clases muy compleja y difícil de mantener.

```java
interface Engine {
    void start();
}

class GasolineEngine implements Engine {
    public void start() {
        System.out.println("Gasoline engine starting...");
    }
}

class ElectricEngine implements Engine {
    public void start() {
        System.out.println("Electric engine starting...");
    }
}

interface Transmission {
    void changeGear();
}

class ManualTransmission implements Transmission {
    public void changeGear() {
        System.out.println("Changing gear manually...");
    }
}

class AutomaticTransmission implements Transmission {
    public void changeGear() {
        System.out.println("Changing gear automatically...");
    }
}

class Vehicle {
    private Engine engine;
    private Transmission transmission;

    public Vehicle(Engine engine, Transmission transmission) {
        this.engine = engine;
        this.transmission = transmission;
    }

    public void start() {
        engine.start();
    }

    public void changeGear() {
        transmission.changeGear();
    }
}

public class Main {
    public static void main(String[] args) {
        Engine gasolineEngine = new GasolineEngine();
        Transmission manualTransmission = new ManualTransmission();
        Vehicle car1 = new Vehicle(gasolineEngine, manualTransmission);
        
        Engine electricEngine = new ElectricEngine();
        Transmission automaticTransmission = new AutomaticTransmission();
        Vehicle car2 = new Vehicle(electricEngine, automaticTransmission);
        
        car1.start();
        car1.changeGear();
        
        car2.start();
        car2.changeGear();
    }
}

```