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
    
    namespace Ejer02_prog02_u1
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
    
    namespace Ejer02_prog03_u1
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
        namespace Ejer02_prog06_u1
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
        namespace Ejer02_prog07_U1
        {
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
                    Console.ForegroundColor = ConsoleColor.White;
                    Console.Write("Nombre del alumno: "); Console.ForegroundColor = ConsoleColor.Cyan; Console.Write(nombre);
        
                    Console.SetCursorPosition(0, 1);
                    Console.ForegroundColor = ConsoleColor.White;
                    Console.Write("Grado y grupo    : "); Console.ForegroundColor = ConsoleColor.Cyan; Console.Write(grupo);
        
                    Console.SetCursorPosition(0, 2);
                    Console.ForegroundColor = ConsoleColor.White;
                    Console.Write("Materia          : "); Console.ForegroundColor = ConsoleColor.Cyan; Console.Write(materia);
        
                    Console.SetCursorPosition(0, 3);
                    Console.ForegroundColor= ConsoleColor.Blue;
                    Console.Write("──────────────────────────────────────────────────────────────────");
        
        
                    Console.SetCursorPosition(10, 4);
                    Console.ForegroundColor = ConsoleColor.Green;
                    Console.WriteLine("Unidad 1 ");
                    Console.SetCursorPosition(13, 5);
                    Console.ForegroundColor = ConsoleColor.Blue;
                    Console.WriteLine(+cal1);
        
                    Console.SetCursorPosition(20, 4);
                    Console.ForegroundColor = ConsoleColor.Green;
                    Console.WriteLine("Unidad 2  ");
                    Console.SetCursorPosition(23, 5);
                    Console.ForegroundColor = ConsoleColor.Blue;
                    Console.WriteLine(+cal2);
        
                    Console.SetCursorPosition(30, 4);
                    Console.ForegroundColor = ConsoleColor.Green;
                    Console.WriteLine("Unidad 3 ");
                    Console.SetCursorPosition(33, 5);
                    Console.ForegroundColor = ConsoleColor.Blue;
                    Console.WriteLine(+cal3);
        
                    Console.ForegroundColor = ConsoleColor.White;
        
                    Console.SetCursorPosition(0, 8);
                    Console.ForegroundColor = ConsoleColor.White;
                    Console.Write("Promedio de calificaciones:"); 
                    Console.ForegroundColor = ConsoleColor.Red;
                    Console.SetCursorPosition(29, 8);
                    Console.Write("{0:N1}",promedio);
        
                    Console.SetCursorPosition(0, 10);
                    Console.ForegroundColor = ConsoleColor.Blue;
                    Console.Write("──────────────────────────────────────────────────────────────────");
        
        
                    Console.ForegroundColor = ConsoleColor.White;
                    Console.SetCursorPosition(0, 12);
                    Console.ReadKey();
                }
            }
        }

Programa 8

    using System;
    using System.Linq;
    class Program
    namespace Ejer02_prog08_U1
    {
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
    }

Programa 9

    using System;
    
    namespace Ejer02_prog09_U1
    {
        internal class Program
        {
            static void Main(string[] args)
            {
                string NOM;
                byte K;
    
                Console.ForegroundColor = ConsoleColor.Magenta;
                Console.Write("DIGITE SU NOMBRE (Que sea mayor a 7 digitos) : ");
                NOM = Console.ReadLine();
    
                Console.WriteLine("LONGITUD : " + NOM.Length);
                if (NOM.Length > 7)
                {
    
                    Console.WriteLine("ESTA DENTRO : " + NOM.Contains("ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz"));
    
                    Console.ForegroundColor = ConsoleColor.Cyan;
                    Console.WriteLine("\nREEMPLAZO VOCAL A: " + NOM.Replace("A", "X"));
                    Console.WriteLine("REEMPLAZO VOCAL a: " + NOM.Replace("a", "x"));
                    Console.WriteLine("REEMPLAZO VOCAL E: " + NOM.Replace("E", "X"));
                    Console.WriteLine("REEMPLAZO VOCAL e: " + NOM.Replace("e", "x"));
                    Console.WriteLine("REEMPLAZO VOCAL I: " + NOM.Replace("I", "X"));
                    Console.WriteLine("REEMPLAZO VOCAL i: " + NOM.Replace("i", "x"));
                    Console.WriteLine("REEMPLAZO VOCAL O: " + NOM.Replace("O", "X"));
                    Console.WriteLine("REEMPLAZO VOCAL o: " + NOM.Replace("o", "x"));
                    Console.WriteLine("REEMPLAZO VOCAL U: " + NOM.Replace("U", "X"));
                    Console.WriteLine("REEMPLAZO VOCAL u: " + NOM.Replace("u", "x"));
    
                    Console.ForegroundColor = ConsoleColor.Red;
                    Console.WriteLine("\nEN MINUSCULAS : " + NOM.ToLower());
                    Console.WriteLine("EN MAYÚSCULAS : " + NOM.ToUpper());
    
                    Console.ForegroundColor = ConsoleColor.Green;
                    Console.WriteLine("\nREMOVER 4 LETRAS : " + NOM.Remove(3, 4));
                    Console.WriteLine("EXTRAER 4 LETRAS : " + NOM.Substring(3, 4));
    
                    Console.ForegroundColor = ConsoleColor.Yellow;
                    Console.WriteLine("\nIZQUIERDA 4 LETRAS : " + fIzquierda(NOM, 4));
                    Console.WriteLine("DERECHA 4 LETRAS : " + fDerecha(NOM, 4));
    
    
                    Console.Write("Pulse Enter:");
                    Console.ReadLine();
    
                    Console.WriteLine();
                    Console.WriteLine("DESDE LA IZQUIERDA");
                    for (K = 1; K <= NOM.Length; K++)
                    {
                        Console.WriteLine(fIzquierda(NOM, K));
                    }
    
                    Console.WriteLine();
                    Console.WriteLine("DESDE LA DERECHA");
                    for (K = 1; K <= NOM.Length; K++)
                    {
                        Console.WriteLine(fDerecha(NOM, K));
                    }
                }
                else
                {
                    Console.ForegroundColor = ConsoleColor.DarkRed;
                    Console.WriteLine("No cumple con los requisitos");
                    Console.ForegroundColor = ConsoleColor.White;
                }
            }
    
            //Funciones 
            public static string fIzquierda(string vCadena, int tam)
            {
                string result = vCadena.Substring(0, tam);
                return result;
            }
    
            public static string fDerecha(string vCadena, int tam)
            {
                int valor = vCadena.Length - tam;
                string result = vCadena.Substring(valor, tam);
                return result;
            }
        }
    }

Programa 10 

    using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Ejer02_prog10_U1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            double valor1, valor2, valor3, res;
            int mul;
            string linea;

            Console.ForegroundColor = ConsoleColor.Cyan;
            Console.Write("Ingresa el valor 1: "); linea = (Console.ReadLine());
            valor1 = double.Parse(linea);
            mul = 0;
            while (mul < 10)
            {
                mul = mul + 1;
                res = valor1 * mul;
                Console.WriteLine($"{valor1} x {mul} = {res} ");
                continue;
            }

            Console.SetCursorPosition(25, 0);
            Console.ForegroundColor = ConsoleColor.Red;
            Console.Write("Ingresa el valor 2: "); linea = (Console.ReadLine());
            valor2 = double.Parse(linea);
            mul = 0;
            for (mul = 1; mul <= 10; mul++)
            {
                Console.SetCursorPosition(25, 1 + mul);
                res = valor2 * mul;
                Console.WriteLine($"{valor2} x {mul} = {res} ");
            }

            Console.SetCursorPosition(50, 0);
            Console.ForegroundColor = ConsoleColor.Yellow;
            Console.Write("Ingresa el valor 3: "); linea = (Console.ReadLine());
            valor3 = double.Parse(linea);
            while (true)
            {
                mul = 0;
                Console.SetCursorPosition(50, 1);
                Console.WriteLine("Menu de Opciones: ");
                Console.SetCursorPosition(50, 2);
                Console.WriteLine("1) Imprimir tabla");
                Console.SetCursorPosition(50, 3);
                Console.WriteLine("0) Cerrar Menu");
                Console.SetCursorPosition(50, 4);
                Console.Write("Seleccione una opcion: ");
                string opcion = Console.ReadLine();

                if (opcion == "0")
                {
                    Console.ForegroundColor = ConsoleColor.White;
                    break;
                }

                switch (opcion)
                {
                    case "1":

                        mul = mul + 1;
                        res = valor3 * mul;
                        Console.SetCursorPosition(50, 5);
                        Console.WriteLine($"{valor3} x {mul} = {res} ");

                        mul = mul + 1;
                        res = valor3 * mul;
                        Console.SetCursorPosition(50, 6);
                        Console.WriteLine($"{valor3} x {mul} = {res} ");

                        mul = mul + 1;
                        res = valor3 * mul;
                        Console.SetCursorPosition(50, 7);
                        Console.WriteLine($"{valor3} x {mul} = {res} ");

                        mul = mul + 1;
                        res = valor3 * mul;
                        Console.SetCursorPosition(50, 8);
                        Console.WriteLine($"{valor3} x {mul} = {res} ");

                        mul = mul + 1;
                        res = valor3 * mul;
                        Console.SetCursorPosition(50, 9);
                        Console.WriteLine($"{valor3} x {mul} = {res} ");

                        mul = mul + 1;
                        res = valor3 * mul;
                        Console.SetCursorPosition(50, 10);
                        Console.WriteLine($"{valor3} x {mul} = {res} ");

                        mul = mul + 1;
                        res = valor3 * mul;
                        Console.SetCursorPosition(50, 11);
                        Console.WriteLine($"{valor3} x {mul} = {res} ");

                        mul = mul + 1;
                        res = valor3 * mul;
                        Console.SetCursorPosition(50, 12);
                        Console.WriteLine($"{valor3} x {mul} = {res} ");

                        mul = mul + 1;
                        res = valor3 * mul;
                        Console.SetCursorPosition(50, 13);
                        Console.WriteLine($"{valor3} x {mul} = {res} ");

                        mul = mul + 1;
                        res = valor3 * mul;
                        Console.SetCursorPosition(50, 14);
                        Console.WriteLine($"{valor3} x {mul} = {res} ");

                        break;

                    default:
                        Console.SetCursorPosition(0, 16);
                        Console.WriteLine("Opción no válida. Por favor, elija una opción válida.");
                        continue;

                }
            }

Menu de Opciones

            using System;
            using System.Linq;
            using System.Runtime.Remoting.Messaging;
            using System.Security.Cryptography;
            using System.Threading;
            
            namespace prog03_u1
            {
                class Program
                {
                    static void Main(string[] args)
                    {
                        do
                        {
                            string resp;
                            DateTime dat = DateTime.Now;
            
                            Console.ForegroundColor = ConsoleColor.Green;
                            Console.BackgroundColor = ConsoleColor.Blue;
                            pintarVentana(0, 0, 3, 119);
                            pintarVentana(27, 0, 29, 119);
                            Console.ForegroundColor = ConsoleColor.Green;
                            Console.BackgroundColor = ConsoleColor.Green;
                            pintarVentana(4, 0, 26, 20);
                            Console.ForegroundColor = ConsoleColor.White;
                            Console.SetCursorPosition(5, 4);
                            Console.Write("M E N U");
                            Console.ForegroundColor = ConsoleColor.Black;
                            Console.SetCursorPosition(2, 6);
                            Console.Write("1.- Dos cifras");
                            Console.SetCursorPosition(2, 7);
                            Console.Write("2.- Tres cifras");
                            Console.SetCursorPosition(2, 8);
                            Console.Write("3.- ZombieBurger");
                            Console.SetCursorPosition(2, 9);
                            Console.Write("4.- Base*Altura");
                            Console.SetCursorPosition(2, 10);
                            Console.Write("5.- Billetes");
                            Console.SetCursorPosition(2, 11);
                            Console.Write("6.- Dia");
                            Console.SetCursorPosition(2, 12);
                            Console.Write("7.- Calificaciones");
                            Console.SetCursorPosition(2, 13);
                            Console.Write("8.- Digito");
                            Console.SetCursorPosition(2, 14);
                            Console.Write("9.- Nombre");
                            Console.SetCursorPosition(2, 15);
                            Console.Write("10.-Tablas");
                            Console.SetCursorPosition(2, 26);
                            Console.Write("<0> para salir");
                            Console.SetCursorPosition(50, 1);
                            Console.ForegroundColor = ConsoleColor.DarkRed;
                            Console.BackgroundColor = ConsoleColor.Blue;
                            Console.SetCursorPosition(40, 0);
                            Console.WriteLine("CENTRO DE BACHILLERATO TECNOLOGIGO Idustrial y de servicios NO.103");
                            Console.SetCursorPosition(85, 3);
                            Console.WriteLine("Hora: {0:d} at {0:t}", dat);
                            Console.SetCursorPosition(40, 27);
                            Console.WriteLine("Hecho por: Franco Cruz Carlos Alexander");
                            Console.SetCursorPosition(40, 28);
                            Console.WriteLine("           Rojas Osti Oscar Manuel");
                            Console.ForegroundColor = ConsoleColor.Black;
                            Console.BackgroundColor = ConsoleColor.Green;
                            Console.SetCursorPosition(2, 18);
                            Console.Write("Su opción es => ");
                            resp = Console.ReadLine();
            
                            if (resp == "0")
                            {
                                Console.ForegroundColor = ConsoleColor.DarkRed;
                                Console.BackgroundColor = ConsoleColor.Blue;
                                Console.SetCursorPosition(2, 28);
                                Console.Write("Presiona <Enter> para terminar... ");
                                string opcion = Console.ReadLine();
                                while (Console.ReadKey().Key != ConsoleKey.Enter) { }
                                break;
                                // pintarVentana(1, 0, 6, 79);
                            }
            
                            switch (resp)
                            {
                                case "1":
                                    Console.ForegroundColor = ConsoleColor.White;
                                    Console.BackgroundColor = ConsoleColor.Black;
                                    programa01();
                                    break;
            
                                case "2":
                                    Console.ForegroundColor = ConsoleColor.White;
                                    Console.BackgroundColor = ConsoleColor.Black;
                                    programa02();
                                    break;
            
                                case "3":
                                    Console.ForegroundColor = ConsoleColor.White;
                                    Console.BackgroundColor = ConsoleColor.Black;
                                    programa03();
                                    break;
            
                                case "4":
                                    Console.ForegroundColor = ConsoleColor.White;
                                    Console.BackgroundColor = ConsoleColor.Black;
                                    programa04();
                                    break;
            
                                case "5":
                                    Console.ForegroundColor = ConsoleColor.White;
                                    Console.BackgroundColor = ConsoleColor.Black;
                                    programa05();
                                    break;
            
                                case "6":
                                    Console.ForegroundColor = ConsoleColor.White;
                                    Console.BackgroundColor = ConsoleColor.Black;
                                    programa06();
                                    break;
            
                                case "7":
                                    Console.ForegroundColor = ConsoleColor.White;
                                    Console.BackgroundColor = ConsoleColor.Black;
                                    programa07();
                                    break;
            
                                case "8":
                                    Console.ForegroundColor = ConsoleColor.White;
                                    Console.BackgroundColor = ConsoleColor.Black;
                                    programa08();
                                    break;
            
                                case "9":
                                    Console.ForegroundColor = ConsoleColor.White;
                                    Console.BackgroundColor = ConsoleColor.Black;
                                    programa09();
                                    break;
            
                                case "10":
                                    Console.ForegroundColor = ConsoleColor.White;
                                    Console.BackgroundColor = ConsoleColor.Black;
                                    programa10();
                                    break;
            
                                default:
                                    Console.SetCursorPosition(40, 6);
                                    Console.WriteLine("!!Opción no válida. Por favor, elija una opción válida.");
                                    Thread.Sleep(2000);
                                    Console.ForegroundColor = ConsoleColor.White;
                                    Console.BackgroundColor = ConsoleColor.Black;
                                    Console.SetCursorPosition(40, 6);
                                    Console.WriteLine("                                                              ");
                                    continue;
                            }
                            Console.Clear();
                        }
                        while (true);
            
                        //Funciones
                        void programa01()
                        {
                            int num, dec, uni, tot_digitos;
                            string valor;
                            Boolean esnumero;
                            do
                            {
                                Console.SetCursorPosition(22, 4);
                                Console.Write("Ingrese un numero de dos cifras => ");
                                valor = Console.ReadLine();
                                tot_digitos = valor.Length;
                                esnumero = int.TryParse(valor, out num);
                                if (tot_digitos >= 3)
                                {
                                    Console.SetCursorPosition(22, 5);
                                    Console.Write("Igrese de Nuevo el numero");
                                }
                            }
                            while (tot_digitos == 0 || tot_digitos >= 3 || !esnumero);
            
                            num = int.Parse(valor);
                            dec = num / 10;
                            uni = num % 10;
                            Console.SetCursorPosition(22, 6);
                            Console.WriteLine("El numero invertido es: " + uni + dec);
            
                            Console.SetCursorPosition(22, 26);
                            Console.Write("Pulse una Tecla:"); Console.ReadLine();
                        }
            
                        void programa02()
                        {
                            int num, dec, uni, tot_digitos, cen;
                            string valor;
                            Boolean esnumero;
                            do
                            {
                                Console.SetCursorPosition(22, 4);
                                Console.Write("Ingrese un numero de tres cifras =>");
                                valor = Console.ReadLine();
                                tot_digitos = valor.Length;
                                esnumero = int.TryParse(valor, out num);
                                if (tot_digitos >= 4)
                                {
                                    Console.SetCursorPosition(22, 5);
                                    Console.Write("Borre e ingrese de Nuevo el numero");
                                }
                                if (tot_digitos < 3)
                                {
                                    Console.SetCursorPosition(22, 5);
                                    Console.Write("Borre e ingrese de Nuevo el numero");
                                }
                            }
                            while (tot_digitos == 0 || tot_digitos != 3 || !esnumero);
            
                            num = int.Parse(valor);
                            cen = num / 100;
                            dec = (num / 10) % 10;
                            uni = num % 10;
            
                            Console.SetCursorPosition(22, 6);
                            Console.WriteLine("El numero invertido es: " + uni + dec + cen);
            
                            Console.SetCursorPosition(22, 26);
                            Console.Write("Pulse una Tecla:"); Console.ReadLine();
                        }
            
                        void programa03()
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
            
            
            
                            Console.SetCursorPosition(22, 4);
                            Console.WriteLine("Bienvenido a 'Zombie_burger'");
                            Console.SetCursorPosition(22, 5);
                            Console.Write("Desea ordenar algo? (Si/No)");
                            string respue = Console.ReadLine();
            
                            while (respue == "Si")
                            {
                                Console.SetCursorPosition(22, 6);
                                Console.WriteLine("Menu");
                                Console.SetCursorPosition(22, 7);
                                Console.WriteLine("1 - Refresco - 25$");
                                Console.SetCursorPosition(22, 8);
                                Console.WriteLine("2 - Papas - 20$");
                                Console.SetCursorPosition(22, 9);
                                Console.WriteLine("3 - Hamburguesa - 40$");
                                Console.SetCursorPosition(22, 10);
                                Console.Write("4 - Terminar el pedido");
                                Console.SetCursorPosition(22, 11);
                                Console.Write("Elige una opcion =>");
            
                                string opcion = Console.ReadLine();
            
                                if (opcion == "4")
                                {
                                    break;
                                }
            
                                switch (opcion)
                                {
                                    case "1":
                                        Console.BackgroundColor = ConsoleColor.Black;
                                        Console.SetCursorPosition(22, 12);
                                        Console.Write("Indique la cantidad de refrescos:                                  ");
                                        Console.SetCursorPosition(55, 12);
                                        cantidad = byte.Parse(Console.ReadLine());
                                        cantidadRefrescos += cantidad;
                                        precio = cantidad * precioRefresco;
                                        item = "Refresco";
                                        break;
            
                                    case "2":
                                        Console.BackgroundColor = ConsoleColor.Black;
                                        Console.SetCursorPosition(22, 12);
                                        Console.WriteLine("Indique la cantidad de papas:                                  ");
                                        Console.SetCursorPosition(51, 12);
                                        cantidad = byte.Parse(Console.ReadLine());
                                        cantidadPapas += cantidad;
                                        precio = cantidad * precioPapas;
                                        item = "Papas";
                                        break;
            
                                    case "3":
                                        Console.BackgroundColor = ConsoleColor.Black;
                                        Console.SetCursorPosition(22, 12);
                                        Console.Write("Indique la cantidad de hamburguesas:                                  ");
                                        Console.SetCursorPosition(58, 12);
                                        cantidad = byte.Parse(Console.ReadLine());
                                        cantidadHamburguesas += cantidad;
                                        precio = cantidad * precioHamburguesa;
                                        item = "Hamburguesa";
                                        break;
                                    default:
                                        Console.BackgroundColor = ConsoleColor.Black;
                                        Console.SetCursorPosition(22, 12);
                                        Console.WriteLine("Opción no válida. Por favor, elija una opción válida.");
                                        continue;
                                }
            
                                total += precio;
                                Console.SetCursorPosition(22, 13);
                                Console.WriteLine($"Pedido:{item}           ");
                                Console.SetCursorPosition(22, 14);
                                Console.WriteLine("Cantidad: " + cantidad);
                                Console.SetCursorPosition(22, 15);
                                Console.WriteLine("Precio: $" + precio);
                            }
            
                            Console.SetCursorPosition(22, 16);
                            Console.Write("¿Es para llevar o para comer aquí? (llevar/comer): ");
                            string modo = Console.ReadLine();
            
                            if (modo == "llevar")
                            {
                                Console.SetCursorPosition(22, 17);
                                Console.Write("Por favor, indique su dirección: ");
                                string direccion = Console.ReadLine();
                                Console.SetCursorPosition(22, 18);
                                Console.WriteLine("Pedido para llevar a la dirección:" + direccion);
                            }
            
                            if (modo == "comer")
                            {
                                Console.SetCursorPosition(22, 17);
                                Console.WriteLine("Pedido para comer aquí mismo, disfrute su comida.");
                            }
                            Console.SetCursorPosition(22, 19);
                            Console.WriteLine("Total a pagar: $ " + total);
            
                            Console.SetCursorPosition(22, 26);
                            Console.Write("Pulse una Tecla:"); Console.ReadLine();
                        }
            
                        void programa04()
                        {
            
                            double BASE, ALTURA, RESUL;
                            string linea;
                            Console.SetCursorPosition(22, 4);
                            Console.Write("DIGITE LA BASE: "); linea = Console.ReadLine();
                            BASE = double.Parse(linea);
                            Console.SetCursorPosition(22, 5);
                            Console.Write("DIGITE LA ALTURA:"); linea = Console.ReadLine();
                            ALTURA = double.Parse(linea);
                            RESUL = (BASE * ALTURA) / 2;
                            Console.SetCursorPosition(22, 6);
                            Console.WriteLine("AREA TRIANGULO:" + string.Format("{0:####.00}", RESUL));
                            Console.SetCursorPosition(22, 7);
                            Console.WriteLine("AREA TRIANGULO:" + string.Format("{0:c}", RESUL));
                            Console.SetCursorPosition(22, 8);
                            Console.WriteLine("AREA TRIANGULO:" + string.Format("{0:f}", RESUL));
                            Console.SetCursorPosition(22, 9);
                            Console.WriteLine("AREA TRIANGULO:" + string.Format("{0:g}", RESUL));
                            Console.SetCursorPosition(22, 10);
                            Console.WriteLine();
                            Console.SetCursorPosition(22, 11);
                            Console.WriteLine("HOY ES: " + string.Format("Hoy es {0:F}", DateTime.Now));
                            Console.SetCursorPosition(22, 12);
                            Console.WriteLine("HOY ES: " + string.Format("Hoy es {0:dddd}{0:d/MM/yyy}", DateTime.Now));
                            Console.SetCursorPosition(22, 26);
                            Console.Write("Pulse una Tecla:"); Console.ReadLine();
                        }
            
                        void programa05()
                        {
                            int dig, mon10, mon5, mon1, bille50, bille100;
                            string valor;
            
                            Console.SetCursorPosition(22, 4);
                            Console.Write("Ingrese la cantidad de dinero a separar: ");
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
            
                            mon1 = dig / 1;
                            dig %= 1;
            
                            Console.SetCursorPosition(22, 6);
                            Console.WriteLine("Billetes de 100: " + bille100);
                            Console.SetCursorPosition(22, 7);
                            Console.WriteLine("Billetes de 50: " + bille50);
                            Console.SetCursorPosition(22, 8);
                            Console.WriteLine("Monedas de 10: " + mon10);
                            Console.SetCursorPosition(22, 9);
                            Console.WriteLine("Monedas de 5: " + mon5);
                            Console.SetCursorPosition(22, 10);
                            Console.WriteLine("Monedas de 1: " + mon1);
            
                            Console.SetCursorPosition(22, 26);
                            Console.Write("Pulse una Tecla:"); Console.ReadLine();
                        }
            
                        void programa06()
                        {
                            Console.SetCursorPosition(22, 4);
                            Console.WriteLine(String.Format("Hoy es {0:dddd}", DateTime.Now));
            
                            Console.SetCursorPosition(22, 26);
                            Console.Write("Pulse una Tecla:"); Console.ReadLine();
                        }
            
                        void programa07()
                        {
                            string nombre;
                            string grupo;
                            string materia;
                            double cal1, cal2, cal3;
                            double promedio;
            
                            Console.SetCursorPosition(22, 4);
                            Console.Write("Nombre del alumno: ");
                            nombre = Console.ReadLine();
            
                            Console.SetCursorPosition(22, 5);
                            Console.Write("Grado y grupo: ");
                            grupo = Console.ReadLine();
            
                            Console.SetCursorPosition(22, 6);
                            Console.Write("Materia: ");
                            materia = Console.ReadLine();
            
                            Console.BackgroundColor = ConsoleColor.Gray;
                            Console.ForegroundColor = ConsoleColor.Black;
                            Console.SetCursorPosition(22, 7);
                            Console.Write("Calificación de la Unidad 1: ");
                            cal1 = double.Parse(Console.ReadLine());
            
                            Console.SetCursorPosition(22, 8);
                            Console.Write("Calificación de la Unidad 2: ");
                            cal2 = double.Parse(Console.ReadLine());
            
                            Console.SetCursorPosition(22, 9);
                            Console.Write("Calificación de la Unidad 3: ");
                            cal3 = double.Parse(Console.ReadLine());
            
                            promedio = (cal1 + cal2 + cal3) / 3.0;
            
                            Console.BackgroundColor = ConsoleColor.Black;
                            Console.ForegroundColor = ConsoleColor.White;
            
            
                            Console.SetCursorPosition(22, 11);
                            Console.ForegroundColor = ConsoleColor.White;
                            Console.Write("Nombre del alumno: "); Console.ForegroundColor = ConsoleColor.Cyan; Console.Write(nombre);
            
                            Console.SetCursorPosition(22, 12);
                            Console.ForegroundColor = ConsoleColor.White;
                            Console.Write("Grado y grupo    : "); Console.ForegroundColor = ConsoleColor.Cyan; Console.Write(grupo);
            
                            Console.SetCursorPosition(22, 13);
                            Console.ForegroundColor = ConsoleColor.White;
                            Console.Write("Materia          : "); Console.ForegroundColor = ConsoleColor.Cyan; Console.Write(materia);
            
                            Console.SetCursorPosition(22, 14);
                            Console.ForegroundColor = ConsoleColor.Blue;
                            Console.Write("──────────────────────────────────────────────────────────────────");
            
            
                            Console.SetCursorPosition(32, 16);
                            Console.ForegroundColor = ConsoleColor.Green;
                            Console.WriteLine("Unidad 1 ");
                            Console.SetCursorPosition(35, 17);
                            Console.ForegroundColor = ConsoleColor.Blue;
                            Console.WriteLine(+cal1);
            
                            Console.SetCursorPosition(42, 16);
                            Console.ForegroundColor = ConsoleColor.Green;
                            Console.WriteLine("Unidad 2  ");
                            Console.SetCursorPosition(45, 17);
                            Console.ForegroundColor = ConsoleColor.Blue;
                            Console.WriteLine(+cal2);
            
                            Console.SetCursorPosition(52, 16);
                            Console.ForegroundColor = ConsoleColor.Green;
                            Console.WriteLine("Unidad 3 ");
                            Console.SetCursorPosition(55, 17);
                            Console.ForegroundColor = ConsoleColor.Blue;
                            Console.WriteLine(+cal3);
            
                            Console.ForegroundColor = ConsoleColor.White;
            
                            Console.SetCursorPosition(22, 19);
                            Console.ForegroundColor = ConsoleColor.White;
                            Console.Write("Promedio de calificaciones:");
                            Console.ForegroundColor = ConsoleColor.Red;
                            Console.SetCursorPosition(51, 19);
                            Console.Write("{0:N1}", promedio);
            
                            Console.SetCursorPosition(22, 21);
                            Console.ForegroundColor = ConsoleColor.Blue;
                            Console.Write("──────────────────────────────────────────────────────────────────");
            
            
                            Console.ForegroundColor = ConsoleColor.White;
                            Console.SetCursorPosition(22, 26);
                            Console.Write("Pulse una Tecla:"); Console.ReadLine();
                        }
            
                        void programa08()
                        {
                            Console.SetCursorPosition(22, 4);
                            Console.Write("Ingrese cualquier caracter: ");
                            char caracter = Console.ReadKey().KeyChar;
            
                            if (char.IsDigit(caracter))
                            {
                                Console.SetCursorPosition(22, 6);
                                Console.WriteLine("Es una cifra numérica.");
                            }
                            else if ("AEIOUaeiou".Contains(caracter))
                            {
                                Console.SetCursorPosition(22, 6);
                                Console.WriteLine("Es una vocal.");
                            }
                            else if (char.IsLetter(caracter))
                            {
                                Console.SetCursorPosition(22, 6);
                                Console.WriteLine("Es una consonante.");
                            }
                            else
                            {
                                Console.SetCursorPosition(22, 6);
                                Console.WriteLine("Caracter no valido");
                            }
                            Console.SetCursorPosition(22, 26);
                            Console.Write("Pulse una Tecla:"); Console.ReadLine();
            
                        }
            
                        void programa09()
                        {
                            string NOM;
                            byte K;
            
                            Console.ForegroundColor = ConsoleColor.Magenta;
                            Console.SetCursorPosition(22, 4);
                            Console.Write("DIGITE SU NOMBRE (Que sea mayor a 7 digitos) : ");
                            NOM = Console.ReadLine();
            
                            Console.SetCursorPosition(22, 5);
                            Console.WriteLine("LONGITUD : " + NOM.Length);
                            if (NOM.Length > 7)
                            {
                                Console.SetCursorPosition(22, 6);
                                Console.WriteLine("ESTA DENTRO : " + NOM.Contains("ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz"));
            
                                Console.ForegroundColor = ConsoleColor.Cyan;
                                Console.SetCursorPosition(22, 8);
                                Console.WriteLine("REEMPLAZO VOCAL A: " + NOM.Replace("A", "X"));
                                Console.SetCursorPosition(22, 9);
                                Console.WriteLine("REEMPLAZO VOCAL a: " + NOM.Replace("a", "x"));
                                Console.SetCursorPosition(22, 10);
                                Console.WriteLine("REEMPLAZO VOCAL E: " + NOM.Replace("E", "X"));
                                Console.SetCursorPosition(22, 11);
                                Console.WriteLine("REEMPLAZO VOCAL e: " + NOM.Replace("e", "x"));
                                Console.SetCursorPosition(22, 12);
                                Console.WriteLine("REEMPLAZO VOCAL I: " + NOM.Replace("I", "X"));
                                Console.SetCursorPosition(22, 13);
                                Console.WriteLine("REEMPLAZO VOCAL i: " + NOM.Replace("i", "x"));
                                Console.SetCursorPosition(22, 14);
                                Console.WriteLine("REEMPLAZO VOCAL O: " + NOM.Replace("O", "X"));
                                Console.SetCursorPosition(22, 15);
                                Console.WriteLine("REEMPLAZO VOCAL o: " + NOM.Replace("o", "x"));
                                Console.SetCursorPosition(22, 16);
                                Console.WriteLine("REEMPLAZO VOCAL U: " + NOM.Replace("U", "X"));
                                Console.SetCursorPosition(22, 17);
                                Console.WriteLine("REEMPLAZO VOCAL u: " + NOM.Replace("u", "x"));
            
                                Console.ForegroundColor = ConsoleColor.Red;
                                Console.SetCursorPosition(22, 19);
                                Console.WriteLine("EN MINUSCULAS : " + NOM.ToLower());
                                Console.SetCursorPosition(22, 20);
                                Console.WriteLine("EN MAYÚSCULAS : " + NOM.ToUpper());
            
                                Console.ForegroundColor = ConsoleColor.Green;
                                Console.SetCursorPosition(22, 21);
                                Console.WriteLine("REMOVER 4 LETRAS : " + NOM.Remove(3, 4));
                                Console.SetCursorPosition(22, 22);
                                Console.WriteLine("EXTRAER 4 LETRAS : " + NOM.Substring(3, 4));
            
                                Console.ForegroundColor = ConsoleColor.Yellow;
                                Console.SetCursorPosition(22, 24);
                                Console.WriteLine("IZQUIERDA 4 LETRAS : " + fIzquierda(NOM, 4));
                                Console.SetCursorPosition(22, 25);
                                Console.WriteLine("DERECHA 4 LETRAS : " + fDerecha(NOM, 4));
            
                                Console.SetCursorPosition(90, 4);
                                Console.Write("Pulse Enter:");
                                Console.ReadLine();
            
                                Console.WriteLine();
                                Console.SetCursorPosition(60, 6);
                                Console.WriteLine("DESDE LA IZQUIERDA");
                                for (K = 1; K <= NOM.Length; K++)
                                {
                                    Console.SetCursorPosition(60, 7+K);
                                    Console.WriteLine(fIzquierda(NOM, K));
                                }
            
                                Console.WriteLine();
                                Console.SetCursorPosition(80, 6);
                                Console.WriteLine("DESDE LA DERECHA");
                                for (K = 1; K <= NOM.Length; K++)
                                {
                                    Console.SetCursorPosition(80, 7 + K);
                                    Console.WriteLine(fDerecha(NOM, K));
                                }
                            }
                            else
                            {
                                Console.ForegroundColor = ConsoleColor.DarkRed;
                                Console.SetCursorPosition(22,8);
                                Console.WriteLine("No cumple con los requisitos");
                                Console.ForegroundColor = ConsoleColor.White;
                            }
                            Console.ForegroundColor = ConsoleColor.White;
                            Console.SetCursorPosition(22, 26);
                            Console.Write("Pulse una Tecla:"); Console.ReadLine();
                        }
            
            
                        void programa10()
                        {
                            double valor1, valor2, valor3, res;
                            int mul;
                            string linea;
            
                            Console.ForegroundColor = ConsoleColor.Cyan;
                            Console.SetCursorPosition(22, 4);
                            Console.Write("Ingresa el valor 1: "); linea = (Console.ReadLine());
                            valor1 = double.Parse(linea);
                            mul = 0;
                            while (mul < 10)
                            {
                                mul = mul + 1;
                                res = valor1 * mul;
                                Console.SetCursorPosition(22, 5 + mul);
                                Console.WriteLine($"{valor1} x {mul} = {res} ");
                                continue;
                            }
            
                            Console.SetCursorPosition(45, 4);
                            Console.ForegroundColor = ConsoleColor.Red;
                            Console.Write("Ingresa el valor 2: "); linea = (Console.ReadLine());
                            valor2 = double.Parse(linea);
                            mul = 0;
                            for (mul = 1; mul <= 10; mul++)
                            {
                                Console.SetCursorPosition(45, 5 + mul);
                                res = valor2 * mul;
                                Console.WriteLine($"{valor2} x {mul} = {res} ");
                            }
            
                            Console.SetCursorPosition(67, 4);
                            Console.ForegroundColor = ConsoleColor.Yellow;
                            Console.Write("Ingresa el valor 3: "); linea = (Console.ReadLine());
                            valor3 = double.Parse(linea);
                            while (true)
                            {
                                mul = 0;
                                Console.SetCursorPosition(67, 5);
                                Console.WriteLine("Menu de Opciones: ");
                                Console.SetCursorPosition(67, 6);
                                Console.WriteLine("1) Imprimir tabla");
                                Console.SetCursorPosition(67, 7);
                                Console.WriteLine("0) Cerrar Menu");
                                Console.SetCursorPosition(67, 8);
                                Console.Write("Seleccione una opcion: ");
                                string opcion = Console.ReadLine();
            
                                if (opcion == "0")
                                {
                                    Console.ForegroundColor = ConsoleColor.White;
                                    break;
                                }
            
                                switch (opcion)
                                {
                                    case "1":
            
                                        mul = mul + 1;
                                        res = valor3 * mul;
                                        Console.SetCursorPosition(67, 9);
                                        Console.WriteLine($"{valor3} x {mul} = {res} ");
            
                                        mul = mul + 1;
                                        res = valor3 * mul;
                                        Console.SetCursorPosition(67, 10);
                                        Console.WriteLine($"{valor3} x {mul} = {res} ");
            
                                        mul = mul + 1;
                                        res = valor3 * mul;
                                        Console.SetCursorPosition(67, 11);
                                        Console.WriteLine($"{valor3} x {mul} = {res} ");
            
                                        mul = mul + 1;
                                        res = valor3 * mul;
                                        Console.SetCursorPosition(67, 12);
                                        Console.WriteLine($"{valor3} x {mul} = {res} ");
            
                                        mul = mul + 1;
                                        res = valor3 * mul;
                                        Console.SetCursorPosition(67, 13);
                                        Console.WriteLine($"{valor3} x {mul} = {res} ");
            
                                        mul = mul + 1;
                                        res = valor3 * mul;
                                        Console.SetCursorPosition(67, 14);
                                        Console.WriteLine($"{valor3} x {mul} = {res} ");
            
                                        mul = mul + 1;
                                        res = valor3 * mul;
                                        Console.SetCursorPosition(67, 15);
                                        Console.WriteLine($"{valor3} x {mul} = {res} ");
            
                                        mul = mul + 1;
                                        res = valor3 * mul;
                                        Console.SetCursorPosition(67, 16);
                                        Console.WriteLine($"{valor3} x {mul} = {res} ");
            
                                        mul = mul + 1;
                                        res = valor3 * mul;
                                        Console.SetCursorPosition(67, 17);
                                        Console.WriteLine($"{valor3} x {mul} = {res} ");
            
                                        mul = mul + 1;
                                        res = valor3 * mul;
                                        Console.SetCursorPosition(67, 18);
                                        Console.WriteLine($"{valor3} x {mul} = {res} ");
            
                                        break;
            
                                    default:
                                        Console.SetCursorPosition(22, 20);
                                        Console.WriteLine("Opción no válida. Por favor, elija una opción válida.");
                                        continue;
            
                                }
                                Console.ForegroundColor = ConsoleColor.White;
                                Console.SetCursorPosition(22, 26);
                                Console.Write("Pulse una Tecla:"); Console.ReadLine();
                            }
            
                        }
            
                        
            
                        void pintarVentana(int p1, int p2, int p3, int p4)
                        {
                            for (int r = p1; r <= p3; r++) // renglones
                            {
                                for (int s = p2; s <= p4; s++) //columnas
                                {
                                    Console.SetCursorPosition(s, r);
                                    Console.Write(" ");
                                }
                            }
                        }
                        Console.SetCursorPosition(0, 28);
                    }
            
                    //Funciones del Programa 9
                    public static string fIzquierda(string vCadena, int tam)
                    {
                        string result = vCadena.Substring(0, tam);
                        return result;
                    }
            
                    public static string fDerecha(string vCadena, int tam)
                    {
                        int valor = vCadena.Length - tam;
                        string result = vCadena.Substring(valor, tam);
                        return result;
                    }
                }
            }

            Console.SetCursorPosition(0, 20);
        }
    }
    }
