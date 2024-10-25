import java.util.Scanner;

public class CensoFamiliar {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Solicitar la cantidad de familias
        System.out.print("Ingrese la cantidad de familias: ");
        int cantidadFamilias = sc.nextInt();

        // Declaración de los arreglos
        double[] agua = new double[cantidadFamilias];
        double[] luz = new double[cantidadFamilias];
        double[] gas = new double[cantidadFamilias];
        int[] estratos = new int[cantidadFamilias];
        
        // Entrada de datos para cada familia
        for (int i = 0; i < cantidadFamilias; i++) {
            System.out.println("\nFamilia #" + (i + 1));
            System.out.print("Ingrese el valor del agua: ");
            agua[i] = sc.nextDouble();
            System.out.print("Ingrese el valor de la luz: ");
            luz[i] = sc.nextDouble();
            System.out.print("Ingrese el valor del gas: ");
            gas[i] = sc.nextDouble();
            System.out.print("Ingrese el estrato (1, 2 o 3+): ");
            estratos[i] = sc.nextInt();
        }

        // Cálculo de los descuentos y totales
        System.out.println("\n--- Totales a pagar por cada familia ---");
        for (int i = 0; i < cantidadFamilias; i++) {
            double descuentoAgua = calcularDescuento(agua[i], estratos[i]);
            double descuentoLuz = calcularDescuento(luz[i], estratos[i]);
            double descuentoGas = calcularDescuento(gas[i], estratos[i]);

            System.out.println("\nFamilia #" + (i + 1));
            System.out.printf("Total a pagar por Agua: %.2f\n", descuentoAgua);
            System.out.printf("Total a pagar por Luz: %.2f\n", descuentoLuz);
            System.out.printf("Total a pagar por Gas: %.2f\n", descuentoGas);
        }

        sc.close();
    }

    // Método para calcular el descuento según el estrato
    public static double calcularDescuento(double valor, int estrato) {
        double descuento;
        if (estrato == 1) {
            descuento = 0.20;
        } else if (estrato == 2) {
            descuento = 0.15;
        } else {
            descuento = 0.09;
        }
        return valor * (1 - descuento);
    }
}
