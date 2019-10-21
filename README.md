# text
软件基础作业
实现一个命令行文本计数统计程序。能正确统计导入的纯英文txt文本中的字符数，单词数，句子数。
通过读取导入，实现计算文本中的各种元素的个数操作

读取文本运行结果
Life was like a box of chocolates,you never know what you are gonna get.
Stupid is as stupid does.
Miracles happen every day.
Death is just a part of life,something we are all destined to do.
Jenny and I was like peas and carrots.
A man can be destroyed but not defeated.
Love means never having to say you are sorry.
行的数量为7行 单词的数量为55个 字符的数量为319个 句子的数量为7个
请按任意键继续. . .


读取空项目运行结果
error
请按任意键继续. . .


代码如下
#include <stdio.h>
int main()
{
FILE *p;
int hang=1,zifu=0,danci=0,zq;
int juzi=0;
p=fopen("C:\\Users\\Lenovo\\Desktop\\lc.txt","r");
if (p == NULL)
{
printf("error\n");
return 0;
}
zq=fgetc(p);
zifu++;
while(zq!=EOF)
{
printf("%c",zq);
if(zq=='\n')
{
hang++;
}
else if(zq==' ')
{
danci++;
}
else if(zq=='.')
{
juzi++;
}
zifu++;
zq=fgetc(p);
}
printf("\n行的数量为%d行 单词的数量为%d个 字符的数量为%d个 句子的数量为%d个\n",hang,danci,zifu,juzi);
}


基本完成要求，但创新部分没有做到，单元测试也没有做到，后续会进行改进。
