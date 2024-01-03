/*
Name: Noman Ahmed Tonmoy
ID: 20230104051
Lab Group: B1
*/
#include<stdio.h>

int main()
{
    int n, option=10, i=0, flag=1;
    int v, j=0, search, f=0;
    printf("Enter array size: ");
    scanf("%d", &n);

    int array[n];
//Initializing array's values to 0.
    for(i=0; i<n; i++)
        array[i]=0;

    i=0;

    while(flag)
    {
        printf("What do you want to do? Press\n1. Insert 2. Delete 3. Search 4. Print 5. Quit\n");
        scanf("%d", &option);

        switch(option)
        {
            case 1 ://Insert
                    printf("Insert a value: ");
                    scanf("%d", &array[i]);
                    printf("\n");

                    i++;
                    break;

            case 2 ://Delete
                    printf("Which value you want to delete: ");
                    scanf("%d", &v);
                    for(j=0; j<i-1; j++)
                        if(array[j]==v)
                          {for(;j<n-1; j++)
                                array[j]=array[j+1];
                          }
                          i--;
                          printf("\n");

                                break;

            case 3 ://Search
                    f=0;
                    printf("Search which value: ");
                    scanf("%d", &search);
                    for(j=0; j<n; j++)
                        {if(array[j]== search)
                            {printf("%d exists in the list\n", search);
                             f=1;
                            }
                        }
                        if(f==0)
                            printf("%d doesn't exist in list\n" , search);

                            printf("\n");

                        break;


            case 4 ://Print
                    printf("List: ");
                    for(j=0; j<i; j++)
                            printf("%d ", array[j]);

                            printf("\n\n");

                    break;

            case 5 ://Quit
                    flag=0;
                    break;

            default: printf("Invalid!!\n");
        }


    }

    return 0;
}
