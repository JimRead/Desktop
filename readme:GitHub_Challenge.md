# GitHub Challenge
## Menu
static void Main(string[] args)
        {

            /*
             James Read
             1812
             Project & Portfolio 1
             GitHub Coding Challenge Menu
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
                    SwapName.NameSwap();

                }else if(userChoice == 2)
                {
                    //Backwards
                    Backwards.BackWards();

                }else if(userChoice == 3)
                {
                    //Age Convert
                    AgeConvert.ConvertAge();

                }else if(userChoice == 4)
                {
                    //Temp Convert
                    TempConvert.ConvertTemp();
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
## Swap Name
class SwapName
    {
        /*
         James Read
         1812
         Project & Portfolio
         GitHub Coding Challenge SwapName
         */

        public static void NameSwap() {

            Console.Clear();

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
            Console.WriteLine("\r\n\r\nExcellent! Your name ({0} {1}) reversed would be {1}, {0}.", firstName, lastName);
        }
## Backwards
class Backwards
    {

        /*
        James Read
        1812
        Project & Portfolio
        GitHub Coding Challenge Backwards
        */

        public static void BackWards()
        {
            Console.Clear();

            //prompt user for a sentence
            Console.WriteLine("\r\n\r\nWelcome to Backwards:\r\nTo begin, please enter a sentence containing at least 6 words...");

            //catch user response
            string userResponse = Console.ReadLine();

            //validate user response
            if (string.IsNullOrWhiteSpace(userResponse))
            {
                //Tell the user what is wrong
                Console.WriteLine("\r\nPlease do not leave this blank, enter a sentence containing at least 6 words and press return.");

                userResponse = Console.ReadLine();
            }

            //Output to user
            Console.WriteLine("\r\nThank you, you entered the sentence:\r\n{0}",userResponse);

            //call function
            string stringArray = ReverseString(userResponse);

            //final output to user
            Console.WriteLine("\r\nBackwards this sentence would read:\r\n{0}",stringArray);
        }

        public static string ReverseString(string _userResponse)
        {
            //convert string to a string array
            char[] stringArray = _userResponse.ToCharArray();

            //reverse the array
            Array.Reverse(stringArray);

            //return the result
            return new string(stringArray);
        }
    }
## Age Convert
class AgeConvert
    {

        /*
        James Read
        1812
        Project & Portfolio
        GitHub Coding Challenge AgeConvert
        */

        public static void ConvertAge()
        {
            Console.Clear();

            //welcome and prompt user for name
            Console.WriteLine("\r\nWelcome to AgeConvert:\r\nTo begin, please enter your name...");

            //catch user response
            string userName = Console.ReadLine();

            //validate user response
            if (string.IsNullOrWhiteSpace(userName))
            {
                //tell the user the problem
                Console.WriteLine("Please do not leave this blank, enter your name and press return.");

                //recatch user response
                userName = Console.ReadLine();
            }

            //prompt user for age
            Console.WriteLine("\r\nThank you {0}. Now I know this may be personal, but what's your age?", userName);

            //catch user response
            string ageString = Console.ReadLine();

            //declare variable
            double userAge;

            //validate user response
            while(!double.TryParse(ageString, out userAge))
            {
                //Tell the user the problem
                Console.WriteLine("You have enter something other than a number. Please enter your age and press return.");

                //recatch response
                ageString = Console.ReadLine();
            }

            //call functions
            double days = ConvertToDays(userAge);
            double hours = ConvertToHours(userAge);
            double minutes = ConvertToMinutes(userAge);
            double seconds = ConvertToSeconds(userAge);

            //final output to user
            Console.WriteLine("\r\n{0} years, fantastic! Next time someone asks, try answering with:\r\n{1} days or,\r\n{2} hours or,\r\n{3} minutes or,\r\n{4} seconds", userAge, days, hours, minutes, seconds);
        }

        public static double ConvertToDays(double _userAge)
        {
            //do the math
            double days = _userAge * 365;

            //return result
            return days;
        }

        public static double ConvertToHours(double _userAge)
        {
            //do the math
            double hours = _userAge * 365 * 24;

            //return result
            return hours;
        }

        public static double ConvertToMinutes(double _userAge)
        {
            //do the math
            double minutes = _userAge * 365 * 24 * 60;

            //return result
            return minutes;
        }

        public static double ConvertToSeconds(double _userAge)
        {
            //do the math
            double seconds = _userAge * 365 * 24 * 60 * 60;

            //return result
            return seconds;
        }
    }
## Temp Convert
class TempConvert
    {

        /*
       James Read
       1812
       Project & Portfolio
       GitHub Coding Challenge TempConvert
       */

        public static void ConvertTemp()
        {
            Console.Clear();

            //Welcome user and prompt for F or C
            Console.WriteLine("\r\nWelcome to TempConvert. Would you like to...\r\n1. Convert temperature from Fahreheit to Celsius\r\n2. Convert temperature from Celsius to Fahrenheit");

            //catch user response
            string tempString = Console.ReadLine();

            //declare variable
            int tempChoice;

            //validate user response
            while (!int.TryParse(tempString, out tempChoice) || tempChoice < 1 || tempChoice > 2)
            {
                //tell the user the problem
                Console.WriteLine("You have entered an invalid entry. Please type 1 to convert from Fahrenheit to Celsius or 2 to convert from Celsius to Fahrenheit.");

                //recatch user response
                tempString = Console.ReadLine();
            }

            //create conditional to do the math
            if (tempChoice == 1)
            {
                //Prompt user for temperature
                Console.WriteLine("\r\nOk, What temperature in Fahrenheit would you like to convert?");

                //catch user response
                string fahString = Console.ReadLine();

                //declare variables
                decimal fahTemp;
                decimal fahConv;

                //validate user response
                while (!decimal.TryParse(fahString, out fahTemp))
                {
                    //tell the user the problem
                    Console.WriteLine("You have entered an invalid entry. Please enter the temperature in Fahrenheit would you like to convert and press return.");

                    //recatch user response
                    fahString = Console.ReadLine();
                }

                //do the math
                fahConv = (fahTemp - 32) / 1.8m;

                //final output to user
                Console.WriteLine("\r\nExcellent! {0} degrees Fahrenheit would be {1} degrees Celsius.", fahTemp, fahConv);

            }
            else if (tempChoice == 2)
            {
                //Prompt user for temperature
                Console.WriteLine("\r\nOk, What temperature in Celsius would you like to convert?");

                //catch user response
                string celString = Console.ReadLine();

                //declare variables
                decimal celTemp;
                decimal celConv;

                //validate user response
                while (!decimal.TryParse(celString, out celTemp))
                {
                    //tell the user the problem
                    Console.WriteLine("You have entered an invalid entry. Please enter the temperature in Celsius would you like to convert and press return.");

                    //recatch user response
                    celString = Console.ReadLine();
                }

                //do the math
                celConv = celTemp * 1.8m + 32;

                //final output to user
                Console.WriteLine("\r\nExcellent! {0} degrees Celsius would be {1} degrees Fahrenheit.", celTemp, celConv);
            }
        }
    }    