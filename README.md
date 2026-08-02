# Overloading-and-Overriding-in-Java-Confusion


# Overloading means:
* Same method name
* Different parameter list
* Usually in the same class
* Example
* Static Method Overloading ✅ Allowed

class Test {

    static void show() {
        System.out.println("No parameter");
    }

    static void show(int x) {
        System.out.println("One int parameter");
    }

    static void show(String name) {
        System.out.println("One String parameter");
    }

    public static void main(String[] args) {
        show();
        show(10);
        show("Zafran");
    }
}

* Output:
* No parameter
* One int parameter
* One String parameter

# 2. Static Method Overriding ❌ Not Allowed
* Static methods belong to the class, not the object.
* If a child class declares a static method with the same signature as the parent, it is method hiding, not overriding.

class Parent
{

    static void show() {
        System.out.println("Parent");
    }
}

class Child extends Parent {

    static void show() {
        System.out.println("Child");
    }
}

public class Main {

    public static void main(String[] args) {

        Parent p = new Child();
        p.show();
    }
}
* OUTPUT
* Parent
