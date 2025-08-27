#include <stdio.h>

int main(void)
{
    int height;
    do
    {
        printf("Height: ");
        if (scanf("%d", &height) != 1)
        {
            while (getchar() != '\n');
            height = 0; 
        }
    }
    while (height < 1);
    
    for (int i = 1; i <= height; i++)
    {
        for (int j = 0; j < height - i; j++)
        {
            printf(" ");
        }
        for (int k = 0; k < i; k++)
        {
            printf("#");
        }
        printf("\n");
    }
    
    return 0;
}
