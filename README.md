# Ejercicios-de-java-temporal
En este repositorio están los ejercicios de java


Ejercicio 1:
import java.util.Scanner;
public class ejerciciossergio1 {  
  public static void main(String[] args) {
    //x=llantas
    //x<5, entonces el precio es de $100
    //x=>5 y <10 , entonces el precio es de $75
    //x>10, entonces el precio es de $50
    
    int llantas;
    int precio;
    

    Scanner user= new Scanner(System.in);
    System.out.println("Cuantas llantas va a comprar: ");
    llantas= user.nextInt();

    if (llantas<5){
     precio= (llantas * 100 );
      System.out.println("Cada llanta tiene un valor de $100, estonces su compra es : " +precio);
    }
    else if ((llantas>=5)&&(llantas<=10)) {
      precio= (llantas * 75);
      System.out.println("Cada llanta tiene un valor de $75; entonces su compra es: " +precio);
    }
    else if (llantas>10) {
    precio= (llantas * 50);
    System.out.println("Cada llanta tiene un valor de $50; entonces su compra es: " +precio);
}
}
}

Link:https://www.programiz.com/online-compiler/3Q1JFe0LYjbkt


Ejercicio 2

import java.util.Scanner;

public class ejercicio2 {

  public static void main(String[] args) {
    
    //proveedor ofrece 10% de descuento sobre el producto sin iva, si tiene un valor de 500 mil o superior
    //el provedor ofrece 15% de descuento sobre el producto si su producto es igual o superior a 500 mil y es de la marca Nosy
    //definir cuanto seria el valor del producto con el 19% del iva incluido

    int producto;
    double descuento;
    double Valortotalconiva;
    double Valortotal;
    double ValorFinal;
    String Nosy;

    Scanner cliente = new Scanner(System.in);
    System.out.println("Cuanto es el valor del producto: ");
    producto= cliente.nextInt();
    Scanner Marca = new Scanner(System.in);
    System.out.println("Si el producto es de la marca Nosy, escribe nosy: ");
    Nosy= Marca.nextLine();

    if((producto>=500 ) && Nosy.equals("nosy")){
    descuento=(producto * 0.15);
    Valortotal=(producto-descuento);
    Valortotalconiva=(Valortotal+(Valortotal*0.19));
    System.out.println("El valor de su producto es de: " + Valortotalconiva );
    }else if(producto>=500){
    descuento=(producto * 0.10);
    Valortotal=(producto-descuento);
    Valortotalconiva=(Valortotal+(Valortotal*0.19));
    System.out.println("El valor de su producto es de: " + Valortotalconiva );
   }
  }
}

Link:https://www.programiz.com/online-compiler/9zoHpdeiD21tY

Ejercicio 3

import java.util.Scanner;
public class Ejercicio3 {
    public static void main(String[] args) {
    
    //Fruteria ofrece descuento segun los kilos comprados
    //De 0-2 kilos ofrece 0% de descuento
    //De 2.1-5 ofrece 10% de descuento
    //De 5.1-10 ofrce 15% de descuento
    //DE 10.1 en adelante ofrece 20% de desceunto
    double fruta;
    double Descuento=0;
    double Valortotal=0;
    double valorkilo=7500;
    double valorSubtotal=0;
    Scanner cliente = new Scanner(System.in);
    System.out.println("Cuantos kilos de fruta va a llevar?: ");
    fruta = cliente.nextDouble();
    
    if(fruta>0 && fruta<2){
     Descuento=(0);
    }
    else if(fruta>2 && fruta<5){
     Descuento=(0.10);
    }
    else if(fruta>5 && fruta<10){
     Descuento=(0.15);
    }
    else if(fruta>10){
     Descuento=(0.20);
    }
    valorSubtotal=(fruta*valorkilo);
    Valortotal=valorSubtotal-(valorSubtotal*Descuento);
    System.out.println("El valor de la fruta es: "+ Valortotal);
  }
}

Link:https://www.programiz.com/online-compiler/3kNqHb56MAqtg

Ejercicio 4

import java.util.Scanner;
public class Ejercicio4{
  public static void main(String[] args) {

//Un obrero necesita calcular su salario semanal
//si trabaja 40 horas o menos se le pagan $5000 por hora
//si trabaja mas de 40 horas se le paga $5000 por cada una de las primeras 40 horas y aumenta el 20% por cada hora extra

int Horas;
int Salario;
double Salariototal;
Scanner trabajador= new Scanner(System.in);
System.out.println("Cuantas horas trabaja a la semana?: ");
Horas= trabajador.nextInt();

if(Horas<=40){
 Salario=(5000*Horas);
 System.out.println("Su salario en la semana es de :" +Salario);
}
 else if(Horas>40){
 Salario=(5000*Horas);
 Salariototal=(Salario +(Salario*0.20));
 System.out.println("Su salario con horas extra incluidas es de: " +Salariototal);
 }
}
}

Link:https://www.programiz.com/online-compiler/4uymDOPujHgCJ

Ejercicio 5

import java.util.Scanner;
public class Ejercicio5 {
  public static void main(String[] args) {
  
 //una tienda esta ofeciendo descuento a sus clientes por el numero de equipos que compra.
 //si compra menos de cinco computadores tendra un 10% de descuento
 //Si compra cinco o mas  computadoras pero, menos de diez tendra un 20% de descuento
 //si compra diez o mas de diez computadoras tendra un 40% de descuento
 
 int computadoras;
 int preciodelacompu;
 double Descuento;
 double valordelacompra;
 Scanner cliente= new Scanner(System.in);
 System.out.println("Cuantas computadoras va a comprar?: ");
 computadoras= cliente.nextInt();
 
 if(computadoras<5){
 preciodelacompu=(computadoras*500);
 Descuento=(preciodelacompu*0.10);
 valordelacompra=(preciodelacompu-Descuento);
 System.out.println("El valor de su compra incluido con el 10% de descuento es de: " +valordelacompra);
 }
if(computadoras>=5 && computadoras<10){
 preciodelacompu=(computadoras*500);
 Descuento=(preciodelacompu*0.20);
 valordelacompra=(preciodelacompu-Descuento);
 System.out.println("El valor de su compra incluido con el 20% de descuento es de: " +valordelacompra);
}
if(computadoras>=10){
 preciodelacompu=(computadoras*500);
 Descuento=(preciodelacompu*0.40);
 valordelacompra=(preciodelacompu-Descuento);
 System.out.println("El valor de su compra incluido con el 40% de descuento es de: " +valordelacompra);
 
 System.out.println("Gracias por su compra!!");
}
}
}
Link:https://www.programiz.com/online-compiler/7zoHpbi8B2X9p
