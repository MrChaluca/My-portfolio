// My-portfolio
// This is a program that to count vowels
#include <iostream>
#include <string>
using namespace std;

int main()
{
    // Declare variables
    string txt;
    int v, ca = 0, ce = 0, ci = 0, co = 0, cu = 0, repeat = 1;

    // Main loop
    do
    {
        // Display menu
        cout << "---  (MENU) ---\n " << "1-(--Count vowels--)\n" << " 0-(-EXIT-)\n";
        cin >> v;

        // Switch based on user input
        switch (v)
        {
            // Case 1: Count vowels
            case 1:
            {
                // Prompt user to enter a sentence
                cout << "Write a sentence:\n";

                // Clear input buffer and get line of text
                cin.ignore();
                getline(cin, txt);

                // Iterate through each character in the string
                for (int i = 0; i < txt.size(); i++)
                {
                    // Check each character for vowels
                    switch (txt[i])
                    {
                        // If the character is a vowel, increment the corresponding counter
                        case 'A':
                        case 'Ã':
                        case 'Á':
                        case 'À':
                        case 'a':
                        case 'ã':
                        case 'á':
                        case 'à':
                            ca = ca + 1;
                            break;
                        case 'E':
                        case 'e':
                        case 'é':
                        case 'è':
                        case 'É':
                        case 'È':
                            ce = ce + 1;
                            break;
                        case 'I':
                        case 'i':
                        case 'Í':
                        case 'Ì':
                        case 'í':
                        case 'ì':
                            ci = ci + 1;
                            break;
                        case 'O':
                        case 'o':
                        case 'õ':
                        case 'Õ':
                        case 'Ó':
                        case 'Ò':
                        case 'ó':
                        case 'ò':
                            co = co + 1;
                            break;
                        case 'U':
                        case 'u':
                        case 'Ú':
                        case 'Ù':
                        case 'ú':
                        case 'ù':
                            cu = cu + 1;
                            break;
                    }
                }

                // Display the count of each vowel
                cout << "This sentence has:\n" << ca << " a\n" << ce << " e\n" << ci << " i\n" << co << " o\n" << cu << " u\n";
                
                // Reset counters
                ca = 0;
                ce = 0;
                ci = 0;
                co = 0;
                cu = 0;
                
                break;
            }
            
            // Case 0: Exit program
            case 0:
            {
                // Set repeat flag to 0 to exit loop
                repeat = v;
                break;
            }
            
            // Default case: Display error message
            default:
                cout << "Error";
                break;
        }
    } while (repeat != 0);

    return 0;
}
