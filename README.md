# l2p
Lista de Programação 2 em C
# l2p
Lista de Programação 2 em C


-----------------------QUESTÃO 1----------------------------
#include <stdio.h>
int mdc(int x, int y){
  int r=(x%y);
  if (r==0)
    return y;
  else
    return mdc(y,r);
}
int main() {
  int x ,y;
  printf("digite os dois números:");
  scanf("%d %d",&x,&y);
  int res = mdc(x,y);
  printf("o mdc é: %d",res);
  return 0;
  }

------------------------------------------------------------

-----------------------QUESTÃO 2----------------------------
#include <stdio.h>
int primo(int n) {
 if (n == 2) {
 return 1;
 } else if (n<2 || (n%2)==0) {
 return 0;
 } else {
 int lim = (int ) sqrt(n);
 for (int i=3; i<= lim; i+=2) {
 if (n% i == 0) {
 return 0;
 }
 }
 return 1;
 }
}
int main() {
  int n,i;
  printf("digite um numero");
  scanf("%d",&n);
  i=0;
  while (i<=n){
    int aux = primo(i);
    if (aux==1)
      printf("o numero:%d é primo\n",i);
    i++;

      
  }
  }
----------------------------------------------------------------
