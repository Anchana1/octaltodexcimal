# octaltodexcimal
------------------cprogram-------------------
#include <stdio.h>
#include <math.h>
int convertDecimalToOctal(int dn);
int main() {
    int decimalNumber;
    printf("Enter a decimal number: ");
    scanf("%d", &decimalNumber);
    printf("%d in decimal = %d in octal", decimalNumber, convertDecimalToOctal(decimalNumber));
    return 0;
}
int convertDecimalToOctal(int dn) {
    int on = 0, i = 1;
     while (dn != 0) {
        on += (dn % 8) * i;
        dn /= 8;
        i *= 10;
    }
    return on;
}
