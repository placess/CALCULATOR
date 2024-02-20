using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Qual operação deseja fazer:");
            Console.WriteLine("1- Adição");
            Console.WriteLine("2- Subtração");
            Console.WriteLine("3- Multiplicação");
            Console.WriteLine("4- Divisão");

            int operacao = int.Parse(Console.ReadLine());

            Console.WriteLine("Digite o primeiro número: ");
            int num1 = int.Parse(Console.ReadLine());

            Console.WriteLine("Digite o segundo número: ");
            int num2 = int.Parse(Console.ReadLine());

            int resultado = 0;

            switch (operacao)
            {
                case 1:
                    {
                        resultado = Adicao(num1, num2);
                        break;
                    }

                case 2:
                    {
                        resultado = subtracao(num1, num2);
                        break;
                    }

                case 3:
                    {
                        resultado = multiplicao(num1, num2);
                        break;
                    }

                case 4:
                    {
                        resultado = divisao(num1, num2);
                        break;
                    }

                    default:
                    
                        Console.WriteLine("Numero invalido, digite outro numero.");
                    break;
                    
            }

            Console.WriteLine("O resultado da operação é: (0) e (1) é: (2)", num1, num2, resultado);
        }

        //--------------------------------------------------------------------------------

        public static int Adicao(int numero1, int numero2)
            {
                int result = numero1 + numero2;
                return result;
            }

        public static int subtracao(int numero1, int numero2)
        {
            int result = numero1 - numero2;
            return result;
        }

        public static int multiplicao(int numero1, int numero2)
        {
            int result = numero1 * numero2;
            return result;
        }

        public static int divisao(int numero1, int numero2)
        {
            int result = numero1 / numero2;
            return result;
        }
    }
}
