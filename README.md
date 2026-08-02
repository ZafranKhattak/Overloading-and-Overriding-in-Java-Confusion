# Overloading-and-Overriding-in-Java-Confusion

* 1. Static Method Overloading ✅ Allowed
# Overloading means:
* Same method name
* Different parameter list
* Usually in the same class
* Example
* class Test {

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
