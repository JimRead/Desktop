# ReadJames_GitHubChallenge
##Menu
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ReadJames_GitHubChallenge
{
    class Program
    {
        static void Main(string[] args)
        {

            /*
             James Read
             November 23, 2018
             DVP1 1812
             GitHub Coding Challenge
             */

            Console.Clear();

            //declare variables
            int[] menuArray = new int[] { 1, 2, 3, 4, 5, 0 };
            int userChoice;

            //loop to cycle through
            do
            {
                //menu
                Console.WriteLine("\r\nWelcome to the Project & Portfolio Coding Challenge!\r\n\r\nCoding Challenge Menu:\r\nPlease enter the number for the challenge you want to run...\r\n\r\n[1] Swap Name\r\n[2] Backwards\r\n[3] Age Convert\r\n[4] Temp Convert\r\n[5] Big Blue Fish\r\n\r\n[0] Exit\r\n\r\nMake your selection:");

                //catch user response
                string userString = Console.ReadLine();

                //validate user response
                while (!(int.TryParse(userString, out userChoice)) || userChoice < 0 || userChoice > 5)
                {
                    //Tell the user the problem
                    Console.WriteLine("\r\nYou have entered an invalid entry. Please enter the number for the challenge you want to run.");

                    //recatch user response
                    userString = Console.ReadLine();
                }

                //conditional to determine which choice user made
                if(userChoice == 1)
                {
                    //Swap Name
                }else if(userChoice == 2)
                {
                    //Backwards
                }else if(userChoice == 3)
                {
                    //Age Convert
                }else if(userChoice == 4)
                {
                    //Temp Convert
                }else if(userChoice == 5)
                {
                    //Big Blue Fish
                }else if(userChoice == 0)
                {
                    //Exit
                    break;
                }
            } while (userChoice != 0);
        }
    }
}
