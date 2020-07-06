# 2D array character

- print 2d char array

```c
#include <stdio.h>
#include <string.h>

int main(void) {
   const int ROW = 20;
   const int COL = 20;
   int size;
   char arr[ROW][COL];
   char ch;
   
   scanf("%d", &size);
   for(int i = 0; i < size; i++){
      scanf("%s", arr[i]);
      //arr[row] 在这里可以直接储存 每一个 word
      printf("%s\n", arr[i]);
      //打印出每一个 word
   }
   printf("\n");
   
   scanf(" %c", &ch);
   for(int i = 0; i < ROW; i++){
      for(int j = 0; j < COL; j++){
         if(arr[i][j] == ch){
            printf("%s\n", arr[i]);
            break;//size drizzle contains two 'z'
         }
      }
   }
   return 0;
}

/* 
input: 4 hello zoo sleep drizzle z
 */


 /* output:
hello
zoo
sleep
drizzle

zoo
drizzle
  */
```