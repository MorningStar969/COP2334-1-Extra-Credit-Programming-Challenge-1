# COP2334-1-Extra-Credit-Programming-Challenge-1
This is a GitHub repository link for the first Programming Challenge from Module 15.

// Employee and ProductionWorker Classes

// This program is used to jot down the employee or production worker's information such as name, number, hire date, shift, and pay rate.

#include <iostream> // This is used to include the input and output stream.
#include <string> // This is used to include the string.
using namespace std; // This is used to avoid the use of std:: in the program.

class Employee; // This is used to declare the class Employee.
class ProductionWorker; // This is used to declare the class ProductionWorker.

class Employee { // This is the class for the employee.
private: // This is the private access specifier.
  string name; // This is the name of the employee.
  int number; // This is the number of the employee.
  string hireDate; // This is the hire date of the employee.
public: // This is the public access specifier.
  Employee(string n, int num, string date) { // This is the constructor for the class Employee.
    name = n; // This is used to set the name of the employee.
    number = num; // This is used to set the number of the employee.
    hireDate = date; // This is used to set the hire date of the employee.
  }
  string getName() { // This is the getName function.
    return name; // This is used to return the name of the employee.
  }
  int getNumber() { // This is the getNumber function.
    return number; // This is used to return the number of the employee.
  }
  string getHireDate() { // This is the getHireDate function.
    return hireDate; // This is used to return the hire date of the employee.
  }
  void setName(string n) { // This is the setName function.
    name = n; // This is used to set the name of the employee.
  }
  void setNumber(int num) { // This is the setNumber function.
    number = num; // This is used to set the number of the employee.
  }
  void setHireDate(string date) { // This is the setHireDate function.
    hireDate = date; // This is used to set the hire date of the employee.
  }
}; 

class ProductionWorker : public Employee { // This is the class for the production worker.
private: // This is the private access specifier.
  int shift; // This is the shift of the production worker.
  double hourlyPayRate; // This is the hourly pay rate of the production worker.
public: // This is the public access specifier.
  ProductionWorker(string n, int num, string date, int s, double pay) : Employee(n, num, date) { // This is the constructor for the class ProductionWorker.
    shift = s; // This is used to set the shift of the production worker.
    hourlyPayRate = pay; // This is used to set the hourly pay rate of the production worker.
  }
  int getShift() { // This is the getShift function.
    return shift; // This is used to return the shift of the production worker.
  }
  double getHourlyPayRate() { // This is the getHourlyPayRate function.
    return hourlyPayRate; // This is used to return the hourly pay rate of the production worker.
  }
  void setShift(int s) { // This is the setShift function.
    shift = s; // This is used to set the shift of the production worker.
  }
  void setHourlyPayRate(double pay) { // This is the setHourlyPayRate function.
    hourlyPayRate = pay; // This is used to set the hourly pay rate of the production worker.
  }
};

int main() { // This is the main function.
  ProductionWorker worker("Joe Santagato", 4682, "08/04/2010", 2, 18.30); // This is used to create an object of the class ProductionWorker.
  cout << "Name: " << worker.getName() << endl; // This is used to print the name of the production worker.
  cout << "Number: " << worker.getNumber() << endl; // This is used to print the number of the production worker.
  cout << "Hire Date: " << worker.getHireDate() << endl; // This is used to print the hire date of the production worker.
  cout << "Shift: " << worker.getShift() << endl; // This is used to print the shift of the production worker.
  cout << "Hourly Pay Rate: " << worker.getHourlyPayRate() << endl; // This is used to print the hourly pay rate of the production worker.
  return 0; // This is used to return 0 for the main function.
}
