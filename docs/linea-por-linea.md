import java.util.Scanner; // abro escanner 

public class Main { // creo una clase principal publica para trabajar la solucion
    
    public static void main(String[] args) {  // clase publica
        
        Scanner scanner = new Scanner(System.in); 
        
        System.out.print("Ingrese el total de la compra: "); // codigo para ingreso por teclado del total de la compra
       
        int valor = scanner.nextInt();  // defino una variable valor al valor ingresado por escaner
        
        System.out.println("El total de la compra es: " + valor + " (sin despacho)"); // imprime el valor de la compra sin despacho segun lo ingresado por teclado
        
        System.out.print("Ingrese kilometros de distancia para despacho: "); // se solicita ingreso por teclado de kilometros para despacho
        
        int km = scanner.nextInt(); // se define variable km para cantidad de kilometros ingresado por teclado
        
        if (valor >50000 && km <= 20) { // condicional if para caso de compras superiores a 50mil pesos en un radio de menos de 20 km para despacho
            int costoDespacho = 0; // se define variable costoDespacho para asignar valor al despacho gratuito en este caso
            int total = valor + costoDespacho; // calculo de valor de compra mas costo de despacho
            System.out.println("Despacho gratis dentro de 20 km"); // se imprime el mensaje despacho gratis
        System.out.println("Total a pagar: " + total);
        } // se imprime el valor total a pagar
        else if (valor >= 25000 && valor <= 49999) { // condicion para caso de que la compra es te entre 25000 y 49990
            int costoDespacho = 150 * km; // se define variable costoDespacho para asignar valor al despacho de 150 pesos 
            int total = valor + costoDespacho;  // calculo de valor de compra mas costo de despacho
            System.out.println("El valor a pagar es: " + total);
        } // imprime el valor a pagar considerando gastos de despacho
        
        else if (valor  <25000) { // condicion para calcular valor en caso de compras inferiores a 25000
            int costoDespacho = 300 * km; // se define variable costoDespacho para asignar valor al despacho de 300 pesos 
            int total = valor + costoDespacho; // calculo de valor de compra mas costo de despacho
            System.out.println("El valor a pagar es: " + total);
        } // imprime el valor a pagar considerando gastos de despacho
        
        else if (km >20){ // condicional para compras en las que los kilometros sean mayores a 20 km
            System.out.println("La opción de despacho a domicilio no se encuentra disponible"); // imprime el resultado del caso
            return; // retrurn para detener el programa
        }
    }}