#include <string>
#include <iostream>
#include <sstream>

class Date {
	int day, month, year;

public:
	Date();

	// d is the day (1-31)
	// m is the month (1-12)
	// y is the year (>1)
	Date(int d, int m, int y);

	// returns the number of days from the date of the object to date d
	int operator - (Date d);
	// returns a date days ahead of the date of the object
	Date operator + (int d);

	// returns a string representation of the date of the object
	std::string toString();

private:
	// returns the number of days from 1 Jan 1800 to the date;
	int daysTo1_1_1800();

	// constructs a date representing d days after Jan 1, 1800
	Date(int d);
};
