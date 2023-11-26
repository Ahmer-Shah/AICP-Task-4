# AICP-Task-4
#include <iostream>
#include <cmath>

class Hexagon {
private:
    double side_length;

public:
    Hexagon(double length) : side_length(length) {}

    double calcArea() 
	{
        return 1.5 * 1.732 * side_length;
    }

    double calcPeri() 
	{
        return 6 * side_length;
    }

    double calcAngleSum() 
	{
        return 6 * 120;
    }

    void display() 
	{
        std::cout << "Hexagon:" << std::endl;
        std::cout << "Area: " << calcArea() << std::endl;
        std::cout << "Perimeter: " << calcPeri() << std::endl;
        std::cout << "Sum of Angles: " << calcAngleSum() << std::endl;
    }
};

class Square {
private:
    double side_length;

public:
    Square(double length) : side_length(length) {}

    double calcAreaSquare() 
	{
        return std::pow(side_length, 2);
    }

    double calcPeriSquare() 
	{
        return 4 * side_length;
    }

    void display() 
	{
        std::cout << "Square:" << std::endl;
        std::cout << "Area: " << calcAreaSquare() << std::endl;
        std::cout << "Perimeter: " << calcPeriSquare() << std::endl;
    }
};

int main() 
{
    int last_digit = 2;

    double hexagon_side_length = last_digit;
    double square_side_length = last_digit + 1;

    Hexagon hexagon(hexagon_side_length);
    Square square(square_side_length);

    char choice;
    do {
        std::cout << "\nMenu:" << std::endl;
        std::cout << "1. Hexagon" << std::endl;
        std::cout << "2. Square" << std::endl;
        std::cout << "3. Exit" << std::endl;

        std::cout << "Enter your choice (1/2/3): ";
        std::cin >> choice;

        switch (choice) 
		{
            case '1':
                hexagon.display();
                break;
            case '2':
                square.display();
                break;
            case '3':
                std::cout << "Exiting the program." << std::endl;
                break;
            default:
                std::cout << "Invalid choice. Exiting." << std::endl;
                break;
        }
    } while (choice != '3');

    return 0;
}
