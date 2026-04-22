# currency-converter

code for the program in c++

#include <iostream>
#include <iomanip> // For formatting output

using namespace std;

int main() {
    double amount;
    int choice;
    
    // Exchange rates relative to 1 USD (as of April 2026)
    const double EUR_RATE = 0.94;
    const double GBP_RATE = 0.81;
    const double INR_RATE = 83.50;
    const double JPY_RATE = 153.20;

    cout << "--- Currency Converter (Base: USD) ---" << endl;
    cout << "1. USD to EUR" << endl;
    cout << "2. USD to GBP" << endl;
    cout << "3. USD to INR" << endl;
    cout << "4. USD to JPY" << endl;
    cout << "Select an option (1-4): ";
    cin >> choice;

    cout << "Enter amount in USD: ";
    cin >> amount;

    cout << fixed << setprecision(2); // Set precision for currency
    
    switch(choice) {
        case 1:
            cout << amount << " USD = " << amount * EUR_RATE << " EUR" << endl;
            break;
        case 2:
            cout << amount << " USD = " << amount * GBP_RATE << " GBP" << endl;
            break;
        case 3:
            cout << amount << " USD = " << amount * INR_RATE << " INR" << endl;
            break;
        case 4:
            cout << amount << " USD = " << amount * JPY_RATE << " JPY" << endl;
            break;
        default:
            cout << "Invalid selection!" << endl;
    }

    return 0;
}
