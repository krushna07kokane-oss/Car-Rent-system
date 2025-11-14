# Car-Rent-system
#include <stdio.h>

int rentPerDay; 

int calculateRent(int days) {
    if (days == 0)
        return 0;  
    else
        return rentPerDay + calculateRent(days - 1);  
}

int main() {
    int days, totalRent;

    printf("Enter number of days you want to rent the car: ");
    scanf("%d", &days);

    printf("Enter rent per day: ");
    scanf("%d", &rentPerDay);

    totalRent = calculateRent(days);

    printf("\nTotal rent for %d days = ₹%d\n", days, totalRent);

    return 0;
}
