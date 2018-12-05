# Transpose-matrix
Asking the user for the size of the matrix and values and transpose it.
#include <stdio.h>
void transpose(int rows,int columns){
     int size [rows][columns];
     int i;
     int j;
     //asking the user to input all the values in the matrix 
     for(i=0; i<rows; ++i)
        for(j=0; j<columns; ++j)
        {
            printf("Enter element array rows %d columns %d: ",i+1, j+1);
            scanf("%d", &size[i][j]);
        }
     
        
    //display the matrix
    printf("\nEntered Matrix: \n");
    for(i=0; i<rows; ++i)
        for(j=0; j<columns; ++j)
        {
            printf("%d  ", size[i][j]);
            if (j == columns-1)
                printf("\n\n");
        }
        
    //do the transpose
    int transpose[columns][rows];
    for(i=0; i<rows; ++i)
        for(j=0; j<columns; ++j)
        {
            transpose[j][i] = size[i][j];
        }
        
        
    //display the transpose
    printf("\nTranspose of Matrix:\n");
    for(i=0; i<columns; ++i)
        for(j=0; j<rows; ++j)
        {
            printf("%d  ",transpose[i][j]);
                if(j==rows-1)
                    printf("\n\n");
        }
}
int main()
{
    int rows;
    int columns;
    printf ("please enter you rows : " );
    scanf("%d", &rows);
    printf("please enter you columns : " );
    scanf("%d",&columns);
    transpose(rows , columns);
}


