// my name is Abdul Rehman, Roll no=38//
#include <stdio.h>
int isprime(int num)
{
    if (num < 2)
        return 0;
    for (int y= 2; y * y <= num; y++)
	{
        if (num % y == 0)
            return 0;
    }
    return 1;
}
int main() {
    int input;
    while (1) {
        printf("PLEASE ENTER A NUMBER BETWEEN 2 and 100: ");
        scanf("%d", &input);
        if (input >= 2 && input <= 100) {
            int result = isprime(input);
            if (result == 1)
                printf("THE NUMBEER IS PRIME.\n");
            else
                printf("THE NUMBER IS NOT PRIME.\n");
            break;
        } else {
            printf(" THE NUMBER IS OUT OF RANGE . PRESS 1 to RETRY: ");
            int retry;
            scanf("%d", &retry);
            if (retry != 1)
               break;
        }
    }
    return 0;
}
