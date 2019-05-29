# Recta


using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Unittest
{
    class Program
    {
        public static int ValidateMenuSelection()
        {
            string userInput = "";
            bool validMenuSelect = false;

            while (validMenuSelect == false)
            {


                Console.WriteLine("1:Get length of the rectangle");
                Console.WriteLine("2:change  length of the rectangle");
                Console.WriteLine("3:Get width of the rectangle");
                Console.WriteLine("4:Change width  of the rectangle");
                Console.WriteLine("5:Get perimeter of the rectangle");
                Console.WriteLine("6:Get Area of the rectangle");
                Console.WriteLine("7:Exit");
                Console.WriteLine("Please select an option from the given menu and enter number :\n");
                userInput = Console.ReadLine();

                if (userInput != "1" &&
                    userInput != "2" &&
                    userInput != "3" &&
                    userInput != "4" &&
                    userInput != "5" &&
                    userInput != "6" &&
                    userInput != "7")

                {
                    Console.WriteLine("Incorrect option please try again \n");

                }
                else
                {
                    validMenuSelect = true;
                }
            }
            Console.WriteLine();
            return int.Parse(userInput);

        }

        public static int ValidateUserInput(string rectside)
        {
            int number = 1;
            bool isValid = false;

            while (isValid == false)
            {
                Console.WriteLine($"please enter your {rectside} of your rectangle");
                string userInput = Console.ReadLine();
                Console.WriteLine();

                bool result =  int.TryParse(userInput, out number);
                if (result == false)
                {
                    Console.WriteLine("value  not valid  , try again \n");
                }

                else if (number < 0 )
                {
                    Console.WriteLine("Number should be greater than zero");
                
            }
                else
                {
                    isValid = true;
                }
        }
            return number; 
    }

        static void Main(String [] args)
       
        {
            Rectangle  c  = new Rectangle();
            bool validrectangleSelect = false;
            string rectangleSelection;
            int selection;

            while (validrectangleSelect == false)
            {
                Console.WriteLine("1 = Create a default \n");
                Console.WriteLine("2 = create custom rectangle\n");
                Console.WriteLine("Choose a menu item to begin:");
                rectangleSelection = Console.ReadLine();
                Console.WriteLine();

                if (rectangleSelection != "1" && rectangleSelection != "2")
                {
                    Console.WriteLine("That's not a valid selection, please try again \n");
                }
                else if (int.Parse(rectangleSelection) == 1)
                {
                    validrectangleSelect = true;
                    
                }
                
                
                  
             
            }


            selection = ValidateMenuSelection();

            while (selection != 7)
            {
                int  result;

                switch (selection)
                {
                    case 1:
                        Console.WriteLine($"length  is: {c.Getlength()}\n");
                        break;
                    case 2:
                        result = ValidateUserInput("length");
                        c.Setlength(result);
                        break;
                    case 3:
                        Console.WriteLine($"width is: {c.Getwidth()}\n");
                        break;
                    case 4:
                        result = ValidateUserInput("width");
                        c.Setwidth(result);
                        break;
                    case 5:
                        Console.WriteLine($"The result of {c.Getlength()*2} + {c.Getwidth()*2} is: {c.GetPerimeter()}\n");
                        break;      
                    case 6:
                        Console.WriteLine($"The result of {c.Getlength()} * {c.Getwidth()} is: {c.GetArea()}\n");
                        break;
                    
                    
                }

                selection = ValidateMenuSelection();

            }

        }
    }
}



        
