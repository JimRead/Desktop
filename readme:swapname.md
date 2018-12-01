# Swap Name
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ReadJames_GitHubChallenge
{
    class SwapName
    {
        /*
         James Read
         1812
         Project & Portfolio
         GitHub Coding Challenge SwapName
         */

        public static void NameSwap() {

            //Prompt user for first name
            Console.WriteLine("\r\n\r\nWelcome to Swap Name:\r\nTo begin, please enter your first name...");

            //catch user response
            string firstName = Console.ReadLine();

            //validate user response
            if (string.IsNullOrWhiteSpace(firstName))
            {
                //Tell the user what is wrong
                Console.WriteLine("Please do not leave this blank, enter you first name and press return.");

                firstName = Console.ReadLine();
            }

            //Prompt user for first name
            Console.WriteLine("\r\n\r\nThank you {0}, now I will need your last name...",firstName);

            //catch user response
            string lastName = Console.ReadLine();

            //validate user response
            if (string.IsNullOrWhiteSpace(lastName))
            {
                //Tell the user what is wrong
                Console.WriteLine("Please do not leave this blank, enter you last name and press return.");

                lastName = Console.ReadLine();
            }

            //Output to user
            Console.WriteLine("\r\n\r\nExcellent! Your name ({0} {1}) reversed would be {1}, {0}.\r\n\r\nPress any key to return to the main menu:", firstName, lastName);
        }
    }
}
