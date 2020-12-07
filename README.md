# Number-Guessing-Game
#My second  C program

// number guessing game
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
int main()
{
    int number,guess,nguessess=1;
    srand(time(0));
    number=rand()%100+1;
    printf("the number is %d \n",number);
    do{
        printf("Guess the number between 1 to 100\n");
        scanf("%d",&guess);
        if(guess>number)
        {
            printf("\n lower number please!");
        }
        else if(guess<number)
        {
             printf("\n Higher number please!");
        }
        else
        {
             printf("you guessed it in %d attempt\n",nguessess);
        }
        nguessess++;
    }while(guess!=number);
    return 0;
}
