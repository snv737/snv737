using System;
namespace factorialExample{
    class programm{
        static void Main(string[] args){
            int number,fact=1,i;
            Console.Write("enter any number");
              number = int.Parse(Console.ReadLine());
              for(i=1;i<=number;i++)
              {
                  fact=fact*i;
              }
              Console.WriteLine($"factorial of {number} is {fact}");
              Console.ReadKey();
              
        }
    }
}




using System;

class Program
{
    static void Main()
    {
        // Input from user
        Console.Write("Enter a number: ");
        double number = Convert.ToDouble(Console.ReadLine());

        // Calculate the cube
        double cube = Math.Pow(number, 3);

        // Output the result
        Console.WriteLine("The cube of {0} is {1}", number, cube);
    }
}




using System;

namespace FibonacciExample
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.Write("Enter the number of Fibonacci terms: ");
            int number = int.Parse(Console.ReadLine());

            int n1 = 0, n2 = 1, n3;

            Console.Write(n1 + " " + n2 + " ");  // print first two terms

            for (int i = 2; i < number; i++)
            {
                n3 = n1 + n2;
                Console.Write(n3 + " ");
                n1 = n2;
                n2 = n3;
            }

            Console.ReadKey();
        }
    }
}




using System;

namespace MoneyConversion
{
    class Program
    {
        static void Main(string[] args)
        {
            // Hardcoded conversion rate (e.g., 1 USD = 74.50 INR)
            double conversionRate = 74.50;

            // Get the amount in USD
            Console.Write("Enter the amount in USD: ");
            double amountInUSD = double.Parse(Console.ReadLine());

            // Convert to INR
            double amountInINR = amountInUSD * conversionRate;

            // Display the result
            Console.WriteLine($"{amountInUSD} USD is equivalent to {amountInINR} INR.");
            
            Console.ReadKey();
        }
    }
}
