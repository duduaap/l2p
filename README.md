# l2p
Lista de Programação 2 em C
-------------------------QUESTÃO 1------------------------------

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
  
----------------------------------------------------------------
-------------------------QUESTÃO 2------------------------------

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
-------------------------QUESTÃO 3------------------------------
#include <stdio.h>
int mdc(int x, int y){
  int r=(x%y);
  if (r==0)
    return y;
  else
    return mdc(y,r);
}
int main() {
  int x ,y , z;
  printf("digite os três números:");
  scanf("%d %d %d",&x,&y,&z);
  int res =mdc( mdc(x,y),z);
  printf("o mdc é: %d",res);
  return 0;
  }
----------------------------------------------------------------
-------------------------QUESTÃO 4------------------------------
#include <stdio.h>
#define Pi 3.14
int main() {
  int r;
  printf("Entre o Valor do Ráio da Esféra:");
  scanf("%d",&r);
  float a = 4*Pi*r*r;
  float v = (4/3)*Pi*r*r*r;
  printf("Área da Esféra:\n\t%f\n Volume da Esféra:\n\t%f",a,v);
  return 0;
  }
----------------------------------------------------------------
-------------------------QUESTÃO 5------------------------------
5) O	 que	 faz	a	função	misterio()?	Ela	está	 correta?	Antes	 da	 chamada	 da	 função,	 temos	a	 seguinte	
linha	de	comando:
...
int i=6, j=10;
misterio(&i, &j);
...
void misterio(int *p, int *q){
 int *temp;
 *temp = *p;
 *p = *q;
 *q
 // A função está invertendo os ponteiros, o i vai resultar em 10 e o j em 6
----------------------------------------------------------------
-------------------------QUESTÃO 6------------------------------
#include <stdio.h>
#include <math.h>
double delta(double a, double b, double c){
  double d=b*b - 4*a*c;
  return d;
}
int raizes(double a, double b, double c, double *px1, double *px2){
  double x1,x2;
  x1=-b+sqrt(b*b - 4*a*c);
  x2=-b-sqrt(b*b - 4*a*c);
  *px1=x1;
  *px2=x2;
  return(x1);
}
int main() {
  double a,b,c,d,aux, x1,x2,*px1,*px2;
  printf("Digite os valores de A, B e C");
  scanf("%f%f%f",&a,&b,&c);
  d=delta(a,b,c);
  x1 = 0;
  x2 = 0;
 
  if (d==0){
    x1=x2=(-b/2*a); 
    *px1 = x1;
    *px2 = x2;
  }
  else
    aux = raizes(a,b,c,&x1,&x2);
  printf("x1= %d \nx2= %d",*px1,*px2);    
  return 0;
  }
