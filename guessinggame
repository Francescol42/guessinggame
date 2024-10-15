
#include <iostream>
#include <random>
using namespace std;

int main()
{
    random_device myEngine;
    uniform_int_distribution <int> randomInt(0, 1000);
    char decision;
    int guess = 1;
    bool continuing = true;
    int i = 1;
    int number = randomInt(myEngine);
    while (guess != 0) {
        cout << "Guess a number between 1 and 1000 or 0 to quit: ";
        cin >> guess;
        if (guess > number) {
            cout << "Your guess is TOO BIG." << endl;
        }
        else if (guess < number && guess != 0) {
            cout << "Your guess is TOO SMALL." << endl;
        }
        else if (guess == number) {
            cout << "\nGOOD JOB! That's correct! You used " << i << " guesses.\n\n";
            cout << "Would you like to play again (Y/N): ";
            cin >> decision;
            if (decision == 'n' || decision == 'N')
                break;
            else if (decision == 'y' || decision == 'Y') {
                number = randomInt(myEngine);
                i = 0;
            }
        }
        else if (guess == 0) {
                break;
        }
        i++;
        
    }
    return 0;
}
