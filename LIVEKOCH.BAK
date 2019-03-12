#include<fstream.h>
#include<conio.h>
#include<stdio.h>
#include<string.h>
#include<dos.h>
class hotel
{
int hcode;
char name[50];
int price;
char exp[20];
float rate;
char a[100];
char com[500];
public:
void getinfo()
{
char o;
cout<<"Enter location code:"<<endl;
cin>>hcode;
cout<<"Enter hotels name:"<<endl;
gets(name);
cout<<"Enter price:"<<endl;
cin>>price;
cout<<"How was your experience with the hotel\n(*)EXCELLENT\n(*)VERY GOOD\n(*)GOOD\n(*)BAD\n(*)POOR\n"<<endl;
gets(exp);
cout<<"Do u want to comment about the hotel..??";
cin>>o;
if(o=='y')
{
cout<<"Enter your name:";
gets(a);
cout<<"Enter your comment: ";
gets(com);
}
}
float rating()
{
if(strcmpi(exp,"excellent")==0)
{
rate=5.0;
return rate;
}
else if(strcmpi(exp,"VERY GOOD")==0)
{
rate=4.0;
return rate;
}
else if(strcmpi(exp,"good")==0)
{
rate=3.0;
return rate;
}
else if(strcmpi(exp,"bad")==0)
{
rate=2.0;
return rate;
}
else if(strcmpi(exp,"poor")==0)
{
rate=1.0;
return rate;
}
else rate=0.0;
return rate;
}
char *retname()
{
return name;
}
void disp()
{
float p;
cout<<"HOTEL CODE:";
cout<<hcode<<endl;
cout<<"HOTEL NAME:";
puts(name);
cout<<"LOCATED AT:";
if(hcode==1)
cout<<"FORT KOCHI\n";
else if(hcode==2)
cout<<"KALOOR\n";
else if(hcode==3)
cout<<"KAKKANAD\n";
else if(hcode==4)
cout<<"MATTANCHERY\n";
else if(hcode==5)
cout<<"PALARIVATTOM\n";
else if(hcode==6)
cout<<"ALUVA\n";
else if(hcode==7)
cout<<"EDAPALLY\n";
else if(hcode==8)
cout<<"VYTILLA\n";
else if(hcode==9)
cout<<"THEVARA\n";
else if(hcode==10)
cout<<"THRIPUNITHURA\n"<<endl;
cout<<"HOTEL PRICE:"<<price<<endl;
p=rating();
cout<<"HOTEL RATING:"<<p<<endl;
cout<<".........COMMENTS........"<<endl;
puts(a);
cout<<"-->";
puts(com);
cout<<"_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_*_"<<endl;
}
int retcode()
{
return hcode;
}
}s;
void append()
{
fstream f;
f.open("hotel.dat",ios::app|ios::binary);
s.getinfo();
f.write((char *)&s,sizeof(s));
f.close();
}
void search()
{
int z;
fstream f;
f.open("hotel.dat",ios::in|ios::binary);
cout<<"Enter location code:";
cin>>z;
while(f.read((char *)&s,sizeof(s)))
{
if(z==s.retcode())
{
s.disp();
}
}
}
void del()
{
char x[50];
fstream f,t;
f.open("hotel.dat",ios::in|ios::binary);
t.open("temp.dat",ios::out|ios::binary);
cout<<"Enter the name of hotel to be deleted:";
gets(x);
while(f.read((char *)&s,sizeof(s)))
{ char nx[30];
strcpy(nx,s.retname());
if(strcmpi(x,nx)!=0)
t.write((char *)&s,sizeof(s));
}
f.close();t.close();
remove("hotel.dat");
rename("temp.dat","hotel.dat");
}
void main()
{
clrscr();
char y;
int n,ch;
fstream f;
cout<<"------------------------\n";
cout<<"|LOCATION     |  CODE   |\n";
cout<<"------------------------\n";
cout<<"|Fort kochi   |   1     |\n";
cout<<"|Kaloor       |   2     |\n";
cout<<"|Kakkanad     |   3     |\n";
cout<<"|Mattanchery  |   4     |\n";
cout<<"|Palarivattom |   5     |\n";
cout<<"|Aluva        |   6     |\n";
cout<<"|Edapally     |   7     |\n";
cout<<"|Vytilla      |   8     |\n";
cout<<"|Thevara      |   9     |\n";
cout<<"|Thripunithara|   10    |\n";
cout<<"-------------------------\n";
cout<<"Enter number of hotels:";
cin>>n;
f.open("hotel.dat",ios::out|ios::binary);
for(int i=0;i<n;++i)
{
s.getinfo();
f.write((char *)&s,sizeof(s));
}
f.close();
clrscr();
cout<<"L       I V    V EEEEEE....K   K  O O O  CCCCCCC H    H I\n";
delay(1000);
cout<<"L       I V    V E         K  K  O     O C       H    H I\n";
delay(1000);
cout<<"L       I V    V E         K K   O     O C       H    H I\n";
delay(1000);
cout<<"L       I V    V EEEEEE....KK    O     O C       HHHHHH I\n";
delay(1000);
cout<<"L       I V    V E         K K   O     O C       H    H I\n";
delay(1000);
cout<<"L       I  V  V  E         K  K  O     O C       H    H I\n";
delay(1000);
cout<<"LLLLLLL I   VV   EEEEEE....K   K  O O O  CCCCCCC H    H I\n\n";
delay(750);
cout<<"\tWelcome to the best hotel finder app in kochi..!!\n";
do
{
cout<<"\t\t-->1)Add hotels\n";
delay(750);
cout<<"\t\t-->2)Search hotels\n";
delay(750);
cout<<"\t\t-->3)Delete hotels\n";
delay(750);
cout<<"\t\t-->4)Display hotels\n";
cin>>ch;
if(ch==1)
{
cout<<"------------------------\n";
cout<<"|LOCATION     |  CODE   |\n";
cout<<"------------------------\n";
cout<<"|Fort kochi   |   1     |\n";
cout<<"|Kaloor       |   2     |\n";
cout<<"|Kakkanad     |   3     |\n";
cout<<"|Mattanchery  |   4     |\n";
cout<<"|Palarivattom |   5     |\n";
cout<<"|Aluva        |   6     |\n";
cout<<"|Edapally     |   7     |\n";
cout<<"|Vytilla      |   8     |\n";
cout<<"|Thevara      |   9     |\n";
cout<<"|Thripunithara|   10    |\n";
cout<<"-------------------------\n";
append();
}
else if(ch==2)
{
cout<<"------------------------\n";
cout<<"|LOCATION     |  CODE   |\n";
cout<<"------------------------\n";
cout<<"|Fort kochi   |   1     |\n";
cout<<"|Kaloor       |   2     |\n";
cout<<"|Kakkanad     |   3     |\n";
cout<<"|Mattanchery  |   4     |\n";
cout<<"|Palarivattom |   5     |\n";
cout<<"|Aluva        |   6     |\n";
cout<<"|Edapally     |   7     |\n";
cout<<"|Vytilla      |   8     |\n";
cout<<"|Thevara      |   9     |\n";
cout<<"|Thripunithara|   10    |\n";
cout<<"-------------------------\n";
cout<<"COMING SOON TO MORE PLACES..!!!"<<endl;
search();
}
else if(ch==3)
{
del();
}
else if(ch==4)
{
fstream f;
f.open("hotel.dat",ios::in|ios::binary);
while(f.read((char *)&s,sizeof(s)))
s.disp();
f.close();
}
cout<<"Do u want to continue..??";
cin>>y;
}
while(y=='y');
getch();
}

























