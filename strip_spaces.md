### 去除字符串中的空格。要求不申请额外的内存，时间复杂度为O(n)。

```c
#include <stdio.h>
#include <string.h>

int main()
{
    char str[] = "a f h flu ";
    int i = 0;
    int j = 0;
    int len = strlen(str);
    for(i=0;i<len;i++)
    {
        if (str[i] == ' ')
        {
            j = i + 1;
            while(j < len && str[j] == ' ')
            {
                j++;
            }
                        if(j==len)
            {
                break;
            }
            else
            {
                str[i] = str[j];
                str[j] = ' ';
            }

        }
    }
    str[i] = '\0';
    printf("%s\n", str);
    return 0;
}
```

时间复杂度应该不对，后面再优化看看。

