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
                while (tot_digitos == 0 || tot_digitos != 3 || !esnumero);
    
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

Programa 5

    using System;
    
    namespace Ejer02_prog05_U1
    {
        internal class Program
        {
            static void Main(string[] args)
            {
                int dig, mon10, mon5, bille50, bille100;
                string valor;
    
                Console.WriteLine("Ingrese la cantidad de dinero a separar: ");
                valor = Console.ReadLine();
                
                dig = int.Parse(valor);
    
                bille100 = dig / 100;
                dig %= 100;
    
                bille50 = dig / 50;
                dig %= 50;
    
                mon10 = dig / 10;
                dig %= 10;
    
                mon5 = dig / 5;
                dig %= 5;
    
                Console.WriteLine("Billetes de 100: " + bille100);
                Console.WriteLine("Billetes de 50: " + bille50);
                Console.WriteLine("Monedas de 10: " + mon10);
                Console.WriteLine("Monedas de 5: " + mon5);
    
            }
        }
    }

Programa 6

        using System;
        namespace ejer02_prog03_u1
        {
            class Program
            {
                static void Main(string[] args)
                {
                    Console.WriteLine(String.Format("Hoy es {0:dddd}", DateTime.Now));
                }
            }
        }

Programa 7

    using System;
    
    class Program
    {
        static void Main()
        {
            string nombre;
            string grupo;
            string materia;
            double cal1, cal2, cal3;
            double promedio;
    
            Console.Write("Nombre del alumno: ");
            nombre = Console.ReadLine();
    
            Console.Write("Grado y grupo: ");
            grupo = Console.ReadLine();
    
            Console.Write("Materia: ");
            materia = Console.ReadLine();
    
            Console.BackgroundColor = ConsoleColor.Gray;
            Console.ForegroundColor = ConsoleColor.Black;
            Console.Write("Calificación de la Unidad 1: ");
            cal1 = double.Parse(Console.ReadLine());
    
            Console.Write("Calificación de la Unidad 2: ");
            cal2 = double.Parse(Console.ReadLine());
    
            Console.Write("Calificación de la Unidad 3: ");
            cal3 = double.Parse(Console.ReadLine());
    
            promedio = (cal1 + cal2 + cal3) / 3.0;
    
            Console.BackgroundColor = ConsoleColor.Black;
            Console.ForegroundColor = ConsoleColor.White;
    
            Console.Clear();
    
            Console.SetCursorPosition(0, 0);
            Console.ForegroundColor = ConsoleColor.Blue;
            Console.WriteLine("Nombre del alumno: " + nombre);
    
            Console.SetCursorPosition(0, 1);
            Console.ForegroundColor = ConsoleColor.Green;
            Console.WriteLine("Grado y grupo: " + grupo);
    
            Console.SetCursorPosition(0, 2);
            Console.ForegroundColor = ConsoleColor.Yellow;
            Console.WriteLine("Materia: " + materia);
    
            Console.BackgroundColor = ConsoleColor.Gray;
            Console.ForegroundColor = ConsoleColor.Black;
    
            Console.SetCursorPosition(0, 4);
            Console.WriteLine("Calificación de la unidad 1: " + cal1);
    
            Console.SetCursorPosition(0, 5);
            Console.WriteLine("Calificación de la unidad 2: " + cal2);
    
            Console.SetCursorPosition(0, 6);
            Console.WriteLine("Calificación de la unidad 3: " + cal3);
    
            Console.BackgroundColor = ConsoleColor.Black;
            Console.ForegroundColor = ConsoleColor.White;
    
            Console.SetCursorPosition(0, 8);
            Console.ForegroundColor = ConsoleColor.Cyan;
            Console.WriteLine("Promedio de calificaciones: " + promedio); 
    
            Console.ForegroundColor = ConsoleColor.White;
    
            Console.ReadKey();
        }
    }

Programa 8

    using System;
    using System.Linq;
    class Program
    {
        static void Main()
        {
            Console.Write("Ingrese cualquier caracter: ");
            char caracter = Console.ReadKey().KeyChar;
    
            if (char.IsDigit(caracter))
            {
                Console.WriteLine("\nEs una cifra numérica.");
            }
            else if ("AEIOUaeiou".Contains(caracter))
            {
                Console.WriteLine("\nEs una vocal.");
            }
            else if (char.IsLetter(caracter))
            {
                Console.WriteLine("\nEs una consonante.");
            }
            else
            {
                Console.WriteLine("\nCaracter no valido");
            }
        }
    }
