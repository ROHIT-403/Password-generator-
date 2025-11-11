# Password-generator-
Create recncent password 
#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() {
    int length;
    string chars = "0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz!@#$%^&*()";
    cout << "Enter password length: ";
    cin >> length;

    srand(time(0));  // Seed random number generator
    string password = "";
    for (int i = 0; i < length; i++)
        password += chars[rand() % chars.size()];

    cout << "\nGenerated Password: " << password << endl;
    return 0;
}
