# 1SI16CS411_SIT_CSE_OOP_LAB

#include <iostream>
#include <iomanip>
using namespace std;


class Complex
{
	private:
		int iRealp;
		int iImagp;

	public:
		void getData(void);
		friend void addComplex(Complex , Complex);

};


void Complex :: getData(void)
{
	cout << "Enter real and imaginary parts of the Complex Number" << endl;
	cin >> iRealp >> iImagp;
}

void addComplex(Complex a, Complex b)
{
	Complex sum;
	sum.iRealp = a.iRealp + b.iRealp;
 	sum.iImagp = a.iImagp + b.iImagp;

	cout << "\nSum is" << sum.iRealp << "+i" << sum.iImagp << endl;
}
int main(void)
{
	Complex c1,c2;

	c1.getData();
	c2.getData();

	addComplex(c1,c2);

	cin.get();
	return 0;
}

