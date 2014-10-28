bubble-sort
===========

sort an array of integers

#include <stdio.h>
#include <stdlib.h>

int main(void)
{
	int i;
	int j;
	int key;
	int arr[10] = { 0 };
	int count = 1;
	
	for (i = 0; i < 10; i++) //get input
	{
		printf("Enter element %d of 10: ", count);
		scanf("%d", &arr[i]);
		count++;
	}

	printf("\n");

	for (i = 0; i < 10; i++) //print unsorted array
	{
		printf("%d ", arr[i]);
	}

	printf("\n"); 

	i = 0; 
	j = 1; 
	while(i != 10) //sort array
	{
		if (arr[i]>arr[j])
		{
			key = arr[j]; //save second item
			arr[j] = arr[i]; //move first item over one spot
			arr[i] = key; //move saved second item one spot down
			i = 0;
			j = 1;
		}
		else
		{
			i++;
			j++;
		}
	}

	printf("\n");

	for (i = 0; i < 10; i++) //print sorted array
	{
		printf("%d ", arr[i]);
	}

	printf("\n");

	return 0;
}
