import java.util.Scanner;

public class Libro {
    private String usuario;
    private double total = 100;
    private double cantidad;

    public Libro(String titular) {
        this.usuario = titular;
        this.cantidad = 0;
    }

    public Libro(String titular, double cantidad) {
        this.usuario = titular;
        this.cantidad = cantidad;
    }

    public String getTitular() {
        return usuario;
    }

    public void setTitular(String titular) {
        this.usuario = titular;
    }

    public double getTotal() {
        return total;
    }

    public void setTotal(double total) {
        this.total = total;
    }

    public double getCantidad() {
        return cantidad;
    }

    public void setCantidad(double cantidad) {
        this.cantidad = cantidad;
    }

    public void ingresar(double cantidad) {
        if (cantidad > 0) {
            total += cantidad;
            System.out.println("Se devolvieron" + cantidad + " libros. Libros disponibles: " + total);
        } else {
            System.out.println("No se puede ingresar una cantidad negativa.");
        }
    }

    public void retirar(double cantidad) {
        if (cantidad > 0) {
            if (total - cantidad < 0) {
                total = 0;
                System.out.println("Libros insuficientes, inventario vacio");
            } else {
                total -= cantidad;
                System.out.println("Se retiraron " + cantidad + " libros. Libros disponibles: " + total);
            }
        } else {
            System.out.println("No se puede retirar una cantidad negativa de libros.");
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Bienvenido a la libreria, Por favor ingrese el nombre del usuario: ");
        String nombreTitular = scanner.nextLine();

        Libro cuenta = new Libro(nombreTitular);

        while (true) {
            System.out.println("\nSeleccione una opción:");
            System.out.println("1. Devolver libro");
            System.out.println("2. Tomar Libro");
            System.out.println("3. Salir");
            System.out.print("Opción: ");
            int opcion = scanner.nextInt();

            if (opcion == 3) {
                System.out.println("Operación finalizada. Libros disponibles: " + cuenta.getTotal());
                break;
            }

            System.out.print("Ingrese la cantidad: ");
            double cantidad = scanner.nextDouble();

            if (opcion == 1) {
                cuenta.ingresar(cantidad);
            } else if (opcion == 2) {
                cuenta.retirar(cantidad);
            } else {
                System.out.println("Opción inválida.");
            }
        }

        scanner.close();
    }
}
