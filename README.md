# stone_paper_scissor
// In this game you have to choose one thing either stone,paper or scissor and the P.C. itself chooses one without revealing to you after that result of the game is declared as per the info. given..

in the battle of stone and paper-> paper wins
in the battle of stone and scissor-> scissor wins
in the battle of scissor and paper-> scissor wins

-->So take the code given below run it into your IDE and enjoy the game.

# CODE.

#include<stdio.h>
#include<stdlib.h>
#include<time.h>
void game(char y,char c){
int a;

// 0-for draw , 1- for your win, 2- for computer win or your lose.

if(y==c){
    a=0;
}if(y=='s'&&c=='w'){
    a=1;
}else if(y=='s'&&c=='g'){
    a=2;
}else if(y=='w'&&c=='s'){
    a=2;
}else if(y=='w'&&c=='g'){
    a=1;
}else if(y=='g'&&c=='w'){
    a=2;
}else if(y=='g'&&c=='s'){
    a=1;
}printf("You chose %c and computer chose %c\n",y,c);
if(a==0){
    printf("Game draw!\n");
}else if(a==1){
    printf("You won!\n");
}else{
    printf("You lose!\n");
}
}
int main()
{char you,cmp;int sel,num;
do{fflush(stdin);
printf("\nLet's begin the  'SNAKE WATER GUN' game  \n\nfollw the instructions given below\n\n");
printf("Enter 's' for snake, 'w' for water, 'g' for gun\n ");
scanf("%c",&you);
srand(time(0));
num =rand()%10;
if(num<=3){
    cmp='s';
}
if(3<num&&num<=6){
    cmp='w';
}
if(6<num&&num<=9){
    cmp='g';
}
game(you,cmp);
printf("if you want to play the game again then press 1 otherwise 0\n");
scanf("%d",&sel);
}while(sel==1);
printf("Hope you enjoyed the game.\n**HAVE A NICE DAY**");
return 0;
}


