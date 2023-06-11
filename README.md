# Interface

## Aim:
To write a C# program using interface concept.
## Algorithm:
## Step 1:
Declare an interface named "bank" with "deposit" and "withd" methods.
## Step 2:
Implement the "bank" interface in the "Program" class with "amount" and "amt" variables.
## Step 3:
Implement the "deposit" method to add the amount to "amt" and return the updated balance.
## Step 4:
Implement the "withd" method to subtract the amount from "amt" and return the updated balance.
## Step 5:
In the "Main" method, get the user's option and display the current balance.
## Step 6:
Determine the chosen option and display it.
## Step 7:
If option is 1, get the withdrawal amount, update balance, and display it.
## Step 8:
If option is 2, get the deposit amount, update balance, and display it.

## Program:
```
Developed By: Mirudhula D
Register NO.: 212221230060
```
```
using System;

namespace System
{
    public interface bank
    {
        public int deposit(int amount);
        public int withd(int amount);
    }

    public class Program : bank
    {
        public int amount, amt = 30000;

        public int deposit(int amount)
        {
            this.amount = amount;
            return amt + amount;
        }

        public int withd(int amount)
        {
            this.amount = amount;
            return amt - amount;
        }

        public static void Main(string[] args)
        {
            Program b = new Program();
            Console.WriteLine("Enter the option \n 1. WITHDRAWAL \n 2. DEPOSIT");
            int a = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("\nAccount Balance: " + b.amt);

            string optionChosen = a == 1 ? "1. WITHDRAWAL" : "2. DEPOSIT";
            Console.WriteLine("Option chosen: " + optionChosen);

            if (a == 1)
            {
                Console.WriteLine("Enter the amount to be withdrawn:");
                b.amount = Convert.ToInt32(Console.ReadLine());
                int c = b.withd(b.amount);
                Console.WriteLine("Bank Balance: " + c);
            }
            else if (a == 2)
            {
                Console.WriteLine("Enter the amount to be deposited:");
                b.amount = Convert.ToInt32(Console.ReadLine());
                int d = b.deposit(b.amount);
                Console.WriteLine("Bank Balance: " + d);
            }
        }
    }
}
```
## Output:
## WITHDRAWING:
![91](https://github.com/MIRUDHULA-DHANARAJ/Interface/assets/94828147/d786176f-b5d7-4806-8487-3242ff56e232)
## DEPOSITING:
![92](https://github.com/MIRUDHULA-DHANARAJ/Interface/assets/94828147/5ff55cc5-2f68-4b1b-b1dc-35e89738c085)
## Result:
Thus a C# program using interface concept is written and executed successfully.
