# PRODIGY_TrackCode_Task1
#include <iostream>
using namespace std;

void convertTemperature(double temp, char unit) {
    if (unit == 'C') {
        double fahrenheit = (temp * 9/5) + 32;
        double kelvin = temp + 273.15;
        cout << temp << " °C = " << fahrenheit << " °F = " << kelvin << " K\n";
    } else if (unit == 'F') {
        double celsius = (temp - 32) * 5/9;
        double kelvin = celsius + 273.15;
        cout << temp << " °F = " << celsius << " °C = " << kelvin << " K\n";
    } else if (unit == 'K') {
        double celsius = temp - 273.15;
        double fahrenheit = (celsius * 9/5) + 32;
        cout << temp << " K = " << celsius << " °C = " << fahrenheit << " °F\n";
    } else {
        cout << "Invalid unit entered. Please use 'C', 'F', or 'K'.\n";
    }
}

int main() {
    double temp;
    char unit;
    cout << "Enter temperature value: ";
    cin >> temp;
    cout << "Enter the unit (C for Celsius, F for Fahrenheit, K for Kelvin): ";
    cin >> unit;
    convertTemperature(temp, unit);
    return 0;
}
