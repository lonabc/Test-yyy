//改程序中的函数计算数组中的最大值，最小值，平均数
#include <stdio.h>
  float fun(int arr[], int sz,int  mine, int max,int gon)
  {
	  if (gon==1)
	  {
		  float sum = 0;
		  for (int i = 0; i < sz; i++)
		  {
			  sum = sum + arr[i];
		  }
		  float average = sum / sz;
		  return average;
	  }
	  else if (gon == 9)
	  {
		  mine = arr[0];
		  for (int i = 1; i < sz; i++)
		  {
			  if (arr[i] < mine)
			  {
				  int temp = mine;
				  mine = arr[i];
				  arr[i] = temp;
			  }
		  }
		  return mine;
	  }
	  else if (gon == 2)
	  {
		  max= arr[9];
		  for (int i = 1; i < sz; i++)
		  {
			  if (arr[i] > max)
			  {
				  int temp = max;
				  max = arr[i];
				  arr[i] = temp;
			  }
		  }
		  return max;
	  }

}
int main()
{
	float average;
	int gon = 1;
	int max = 0;
   int mine = 0;
   int arr[10];
   int sz = sizeof(arr) / sizeof(arr[0]);
   printf("开始输入数组\n");
   for(int i=0;i<sz;i++)
   { 
	   scanf("%d", &arr[i]);
   }
	if (gon == 1)
	{
		 
		 average = fun(arr, sz, mine, max, gon);
		 gon = 9;
	}

	 if (gon == 9)
	{
		mine= fun(arr, sz, mine, max, gon);
		gon =2;
		
	}

	 if (gon == 2)
	{
		max = fun(arr, sz, mine, max, gon);

	}
	printf("数组平均数为 =%.2f\n", average);
	printf("最小值为=%d\n", mine);
	printf("最大值为=%d\n", max);
    printf("\n殷传国");
   return 0;
}
-----------------------------------------
