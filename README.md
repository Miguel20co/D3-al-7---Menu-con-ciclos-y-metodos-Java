# D3-al-7---Menu-con-ciclos-y-metodos-Java

  # Python 
   
    def mostrar_menu():
        print("Menu principal")
        print("mostrar numeros(for)")
        print("sumar numeros(while)")
        print("validar contraseña")
        print("salir")
    
        opciones = int(input("selecionar opcion: "))
        return opciones

    def mostrarnumeros(n):
        for i in range(1,n + 1):
            print(i)
        
    def sumarnumeros():
        total = 0
        num_ingresado = -1
        print("ingresa los numeros, no colocar 0")
    
        while num_ingresado != 0:
            num_ingresado = int(input("numero: "))
            total = total + num_ingresado
        
        return total

    def validarcontraseña():
        clave = "2588"
    
        while True:
            intento = input("Escribe la clave: ")
        
            if intento == clave:
                print("Acceso concedido.")
                break
            
            else:
                print("Clave mala, intenta otra vez.")

    continuar = True

    while continuar:
        opcion_elegida = mostrar_menu()
    
        if opcion_elegida == 1:
            limite = int(input("¿cuantos numeros quieres ver?: "))
            mostrarnumeros(limite)
        
        elif opcion_elegida == 2:
            resultado = sumarnumeros()
            print("suma del total de numeros:", resultado)
        
        elif opcion_elegida == 3:
            validarcontraseña()
        
        elif opcion_elegida == 4:
            print("cerrando programa.")
            continuar = False




# Java

    import java.util.Scanner;

    public class ProgramaMenu {

      public static void main(String[] args) {
          Scanner sc = new Scanner(System.in);
          int opcionElegida; 

         do {
              opcionElegida = mostrarMenu(sc);

              if (opcionElegida == 1) {
                  System.out.print("¿Cuántos números quieres ver?: ");
                  int limite = sc.nextInt();
                  mostrarNumeros(limite);
              } 
              else if (opcionElegida == 2) {
                  int resultado = sumarNumeros(sc);
                  System.out.println("Suma del total de números: " + resultado);
              } 
              else if (opcionElegida == 3) {
                  validarContrasena(sc);
              } 
              else if (opcionElegida == 4) {
                  System.out.println("Cerrando programa.");
               } 
              else {
                  System.out.println("Opción no válida.");
              }

           } while (opcionElegida != 4);

          sc.close();
      }

      public static int mostrarMenu(Scanner sc) {
          System.out.println("Menu principal");
          System.out.println("1. Mostrar números (for)");
          System.out.println("2. Sumar números (while)");
          System.out.println("3. Validar contraseña");
          System.out.println("4. Salir");
          System.out.print("Seleccionar opción: ");
        
          return sc.nextInt();
      }

      public static void mostrarNumeros(int n) {
          for (int i = 1; i <= n; i++) {
             System.out.println(i);
          }
      }

      public static int sumarNumeros(Scanner sc) {
           int total = 0;
          int numIngresado = -1;
          System.out.println("Ingresa los números, el programa termina con 0:");

          while (numIngresado != 0) {
              System.out.print("Número: ");
              numIngresado = sc.nextInt();
              total += numIngresado;
          }
          return total;
      }

      public static void validarContrasena(Scanner sc) {
          String clave = "2588";
          sc.nextLine(); 

          while (true) {
              System.out.print("Escribe la clave: ");
              String intento = sc.nextLine();

              if (intento.equals(clave)) {
                  System.out.println("Acceso concedido.");
                  break;
              } else {
               System.out.println("Clave mala, intenta otra vez.");
              }
          }
      }
  }
   
