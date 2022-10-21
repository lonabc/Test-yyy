#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
 
int main()
{
	int  n = 0;
	float score = 0;
	printf("请输入成绩\n");
	scanf("%d", &n);
	switch (n)
	{
	case 80:case 81:case 82:case 83:case 84:case 85:case 86:case 87:case 88:case 89:case 90:case 91:case 92:case 93:case 94:case 95:case 96:case 97:case 98:case 99:case 100:
		score = n;
		printf("score =%f\n", score);
		printf("优秀");
		break;
	case 60:case 61:case 62:case 63:case 64:case 65:case 66:case 67:case 68:case 69:case 70:case 71:case 72:case 73:case 74:case 75:case 76:case 77:case 78:case 79:
		score = n;
		printf("score =%f\n", score);
		printf("合格");
		break;
	default:
		score = n;
		printf("score =%f\n",score );
		printf("不合格");

	}
}
-----------------------------------------
