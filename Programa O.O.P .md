Programa 1

    using System;
    
    namespace ejer02_prog01_u1
    {
        internal class Program
        {
    
            static void Main(string[] args)
            {
                int num, dec, uni, tot_digitos;
                string valor;
                Boolean esnumero;
                do
                {
                    Console.WriteLine("Ingrese un numero de dos cifras =>");
                    valor = Console.ReadLine();
                    tot_digitos = valor.Length;
                    esnumero = int.TryParse(valor, out num);
                }
                while (tot_digitos == 0 || tot_digitos >= 3 || !esnumero);
    
                num = int.Parse(valor);
                dec = num / 10;
                uni = num % 10;
    
                Console.WriteLine("El numero invertido es: " + uni + dec );
                Console.ReadLine();
            }
        }
    }

Programa 2

    using System;
    
    namespace ejer02_prog02_u1
    {
        internal class Program
        {
    
            static void Main(string[] args)
            {
                int num, dec, uni, tot_digitos, cen;
                string valor;
                Boolean esnumero;
                do
                {
                    Console.WriteLine("Ingrese un numero de tres cifras =>");
                    valor = Console.ReadLine();
                    tot_digitos = valor.Length;
                    esnumero = int.TryParse(valor, out num);
                }
                while (tot_digitos == 0 || tot_digitos >= 4 || !esnumero);
    
                num = int.Parse(valor);
                cen = num / 100;
                dec = (num / 10) % 10;
                uni = num % 10;
    
                Console.WriteLine("El numero invertido es: " + uni + dec + cen);
                Console.ReadLine();
            }
        }
    }

Programa 3

    using System;
    
    namespace ejer02_prog03_u1
    {
        class Program
        {
            static void Main()
            {
                const double precioRefresco = 25.0;
                const double precioPapas = 20.0;
                const double precioHamburguesa = 40.0;
    
                double total = 0.0;
    
                byte cantidadRefrescos = 0;
                byte cantidadPapas = 0;
                byte cantidadHamburguesas = 0;
    
                byte cantidad;
                double precio = 0.0;
                string item = "";
    
                Console.WriteLine("Bienvenido a 'Zombie_burger'");
                Console.WriteLine("Desea ordenar algo? (Si/No)");
                string resp = Console.ReadLine();
    
                while (resp == "Si")
                {
                    Console.WriteLine("\nMenu");
                    Console.WriteLine("1 - Refresco - 25$");
                    Console.WriteLine("2 - Papas - 20$");
                    Console.WriteLine("3 - Hamburguesa - 40$");
                    Console.WriteLine("4 - Terminar el pedido");
    
                    string opcion = Console.ReadLine();
    
                    if (opcion == "4")
                    {
                        break;
                    }
    
                    switch (opcion)
                    {
                        case "1":
                            Console.Write("Indique la cantidad de refrescos: ");
                            cantidad = byte.Parse(Console.ReadLine());
                            cantidadRefrescos += cantidad;
                            precio = cantidad * precioRefresco;
                            item = "Refresco";
                            break;
    
                        case "2":
                            Console.Write("Indique la cantidad de papas: ");
                            cantidad = byte.Parse(Console.ReadLine());
                            cantidadPapas += cantidad;
                            precio = cantidad * precioPapas;
                            item = "Papas";
                            break;
    
                        case "3":
                            Console.Write("Indique la cantidad de hamburguesas: ");
                            cantidad = byte.Parse(Console.ReadLine());
                            cantidadHamburguesas += cantidad;
                            precio = cantidad * precioHamburguesa;
                            item = "Hamburguesa";
                            break;
                        default:
                            Console.WriteLine("Opción no válida. Por favor, elija una opción válida.");
                            continue;
                    }
    
                    total += precio;
                    Console.WriteLine("Pedido: " + item);
                    Console.WriteLine("Cantidad: " + cantidad);
                    Console.WriteLine("Precio: $" + precio);
                }
    
                Console.Write("\n¿Es para llevar o para comer aquí? (llevar/comer): ");
                string modo = Console.ReadLine();
    
                if (modo == "llevar")
                {
                    Console.Write("\nPor favor, indique su dirección: ");
                    string direccion = Console.ReadLine();
                    Console.WriteLine("\nPedido para llevar a la dirección:" + direccion);
                }
    
                if (modo == "comer")
                {
                    Console.WriteLine("\nPedido para comer aquí mismo, disfrute su comida.");
                }
    
                Console.WriteLine("Total a pagar: $ " + total);
            }
        }
    }

Programa 4

        using System;
        using System.Collections.Generic;
        using System.Linq;
        using System.Text;
        using System.Threading.Tasks;
        
        namespace Ejer02_prog04_U1
        {
            internal class Program
            {
                static void Main(string[] args)
                {
                    double BASE, ALTURA, RESUL;
                    string linea;
                    Console.Write("DIGITE LA BASE: "); linea = Console.ReadLine();
                    BASE = double.Parse(linea);
                    Console.Write("DIGITE LA ALTURA:"); linea = Console.ReadLine();
                    ALTURA = double.Parse(linea);
                    RESUL = (BASE * ALTURA) / 2;
                    Console.WriteLine("AREA TRIANGULO:" + string.Format("{0:####.00}", RESUL));
                    Console.WriteLine("AREA TRIANGULO:" + string.Format("{0:c}", RESUL));
                    Console.WriteLine("AREA TRIANGULO:" + string.Format("{0:f}", RESUL));
                    Console.WriteLine("AREA TRIANGULO:" + string.Format("{0:g}", RESUL));
                    Console.WriteLine();
                    Console.WriteLine("HOY ES: " + string.Format("Hoy es {0:F}", DateTime.Now));
                    Console.WriteLine("HOY ES: " + string.Format("Hoy es {0:dddd}{0:d/MM/yyy}", DateTime.Now));
                    Console.Write("Pulse una Tecla:"); Console.ReadLine();
                }
            }
        }

