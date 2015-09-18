#include <iostream>
#include <conio.h>
#include <string.h>
#include <stdio.h>
using namespace std;

struct Struct
{
	char name[64];
	int yr;
	int cb;
	int cpb;
}s;

void Menu(int);
void inp(Struct s);
void out(Struct s);
void srch(Struct s);
FILE *f;

int main(){
	char c;
m:	cout<<"w - write;\n"
          "r - read;\n"
          "s - search;\n"
          "e - exit.\n"<<endl; 
	cin>>c;
	switch(c)
				{
				case 'w':inp(s);break;
				case 'r':out(s);break;
				case 'e': exit(0);fclose(f); break;
				case 's': srch(s);break;
				default: goto m; break;
				}
	getch();
	system("cls");
	goto m;
    	return 0;
}
void inp(Struct s)
{   
      system("cls");
    cout<<"Enter information--> ";
	    f=fopen("text.txt","a+");
	cout<<"Book's name(space = ' _ '): ";
 cin>>s.name;
	cout<<"Release year: ";
	cin>>s.yr;
	cout<<"Count books: ";
	cin>>s.cb;
	cout<<"Count publ books: ";
	cin>>s.cpb;
	   fwrite(&s,sizeof(Struct),1,f);
	  fclose(f);
}
void out(Struct s)
{
	f=fopen("text.txt","ab+");
	int c, k = 0;
	 system("cls");
	 	while((c=fread(&s,sizeof(Struct),1,f))!=NULL){ 
		cout<<"Book's name: "<<s.name<<endl;
		cout<<"Release year: "<<s.yr<<endl;
		cout<<"Count books: "<<s.cb<<endl;
		cout<<"Count publ books: "<<s.cpb<<endl;
		cout<<endl;
         k++;
	}
	cout<<"Count books="<<k;
