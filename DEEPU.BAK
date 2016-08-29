#include<iostream.h>
#include<conio.h>
#include<stdlib.h>
#include<stdio.h>
#include<fstream.h>
#include<graphics.h>
#include<dos.h>
#include<string.h>


int i,n1,n2,n3,n4,n5,n6,n7;
////////////////////////////////////////////////////////////////
struct fabric
{
char fab[20],supplier[50],add[30];
float demand,comt;
};

struct purshare
{
char sname[20],cname[20],cad[20];
float per;
};

struct designer
{
char desiname[30],addesigner[30];
float charge,age;
};

struct shop
{
char dress[30],desig[30],featur[50];
int code,stock;
float price;
};

struct shows
{
int showno,tickets;
char date[15];
char celebrity[30],season[30];
float cost;
};

///////////////////////////////////////////////////////////////////
void ad_shop()
{       shop s[20];
	fstream sfile;
	sfile.open("SHOP.dat",ios::app|ios::binary);
	cout<<"Enter number of records : ";
	cin>>n4;
	for(i=0;i<n4;i++)
	{     cout<<"Enter dress code : ";
	      cin>>s[i].code;
	      cout<<"Enter dress type : ";
	      gets(s[i].dress);
	      cout<<"Enter designer name : ";
	      gets(s[i].desig);
	      cout<<"Enter price : ";
	      cin>>s[i].price;
	      cout<<"Enter its features : ";
	      gets(s[i].featur);
	      cout<<"Enter stock : ";
	      cin>>s[i].stock;
	      sfile.write((char*)&s[i],sizeof(s[i]));
	}
	sfile.close();
}

void ad_shows()
{       shows h[20];
	fstream hfile;
	hfile.open("SHOWS.dat",ios::app|ios::binary);
	cout<<"Enter number of records : ";
	cin>>n5;
	for(i=0;i<n5;i++)
		{
	 cout<<"Enter show number : ";
	      cin>>h[i].showno;
	      cout<<"Enter show date : ";
	      gets(h[i].date);
	      cout<<"Enter season : ";
	      gets(h[i].season);
	      cout<<"Enter celebrity name : ";
	      gets(h[i].celebrity);
	      cout<<"Enter total number of tickets : ";
	      cin>>h[i].tickets;
	      cout<<"Enter cost per ticket : ";
	      cin>>h[i].cost;
	      hfile.write((char*)&h[i],sizeof(h[i]));
	}
	hfile.close();
}

void ad_fabric()
{       fabric f[20];
	fstream ffile;
	ffile.open("FABRIC.dat",ios::app|ios::binary);
	cout<<"Enter number of records : ";
	cin>>n2;
	for(i=1;i<=n2;i++)
	{	cout<<"Enter name of fabric : ";
		gets(f[i].fab);
		cout<<endl<<"Enter name of supplier of fabric : ";
		gets(f[i].supplier);
		cout<<endl<<"Enter the address of supplier : ";
		gets(f[i].add);
		cout<<"Enter the % demand of the fabric : ";
		cin>>f[i].demand;
		cout<<endl<<"Enter the cost of fabric per metres : ";
		cin>>f[i].comt;
		ffile.write((char*)&f[i],sizeof(f[i]));
	}
	ffile.close();
}

void ad_desig()
{       designer d[20];
	fstream dfile;
	dfile.open("DESIGNER.dat",ios::app|ios::binary);
	cout<<"Enter number of records : ";
	cin>>n3;
	for(int b=1;b<=n3;b++)
	{     cout<<endl<<"Enter the name of designer : ";
	      gets(d[b].desiname);
	      cout<<"Enter designer's age : ";
	      cin>>d[b].age;
	      cout<<"Enter the address of designer : ";
	      gets(d[b].addesigner);
	      cout<<"Enter the designer's average charge per dress : ";
	      cin>>d[b].charge;
	      dfile.write((char*)&d[b],sizeof(d[b]));
	}
	dfile.close();
	dfile.clear();
}
///////////////////////////////////////////////////////////////////////
int password()
{
	clrscr();
	char pass[20],pass2[20],ch;
	int c=0;

	int i;
	x:
	i=0;
	ch=' ';
	cout<<"\n Enter password : ";
	while(i<20&&ch!=13)
	{
		ch=getch();
		if(ch==8)
		{
			cout<<"\b \b";
			i--;
		}
		else if(ch!=13)
		{
		pass[i]=ch;
		i++;
		cout<<"*";
		}

	}
	pass[i]='\0';
	ifstream f1("passwrd.txt");
	f1.getline(pass2,20);
	f1.close();

	if(strcmp(pass,pass2)==0)
	{	cout<<"\n Password confirmed";return(1); }
	else
	{
		c++;
		if(c<3)
		{
		  cout<<"\n Rejected, Re-enter your password";
		  goto x;
		}
		else
		{ cout<<"\n Sorry! Invalid Password\n";
		  cout<<" You can't access the grant.";
		  return(0);
		}
	}
}
///////////////////////////////////////////////////////////////////////
void changepass()
{ clrscr();
  char pass[20];
  ofstream k("Passwrd.txt");
  ofstream temp("temp.txt");
  char ch;

	int i;

	i=0;
	ch=' ';
	cout<<"\n Enter new password(not more than 20 charaters) : \n";
	while(i<20&&ch!=13)
	{
		ch=getch();

		if(ch==8)
		{
			cout<<"\b \b";
			i--;
		}
		else if(ch!=13)
		{
		pass[i]=ch;
		i++;
		cout<<"*";
		}

	}
	pass[i]='\0';
  temp<<pass;
  remove("Passwrd.txt");
  rename("temp.txt","Passwrd.txt");
  k.close();
  temp.close();
  cout<<endl<<"\nPassword successfully changed.\n";
  delay(500);
  cout<<"\nPress any key to continue...\n";
  getch();
  clrscr();
}
///////////////////////////////////////////////////////////////////////
void welcome()
{
	textbackground(BLACK);
	textcolor(LIGHTMAGENTA);
	sound(256);
	gotoxy(40,4);cout<<"";
	gotoxy(39,5);cout<<"";
	gotoxy(38,6);cout<<"";
	gotoxy(42,6);cout<<"";
	gotoxy(38,7);cout<<"";
	gotoxy(38,8);cout<<"";
	gotoxy(38,9);cout<<"";
	gotoxy(40,9);cout<<"";
	gotoxy(36,10);cout<<"";
	gotoxy(36,11);cout<<"";
	gotoxy(38,11);cout<<"";
	gotoxy(38,12);cout<<"";
	gotoxy(38,13);cout<<"";
	gotoxy(38,14);cout<<"";
	gotoxy(37,15);cout<<"";
	gotoxy(35,16);cout<<"";
	gotoxy(35,17);cout<<"";
	gotoxy(35,18);cout<<"";
	delay(1500);
	clrscr();

	for(int a=2;a<=79;a++)
	{    gotoxy(a,1);
	     cout<<"#";
	     gotoxy(a,25);
	     cout<<"#";
	     delay(40);
	}
	sound(400);
	gotoxy(28,7);
	cprintf("N");
	delay(200);
	gotoxy(32,6);
	cprintf("E");
	delay(200);
	gotoxy(36,5);
	cprintf("W");
	delay(200);
	gotoxy(38,5);
	cprintf("-");
	delay(200);
	gotoxy(40,5);
	cprintf("E");
	delay(200);
	gotoxy(44,6);
	cprintf("R");
	delay(200);
	gotoxy(48,7);
	cprintf("A");
	delay(200);
	gotoxy(26,9);
	cprintf("F A S H I O N    H O U S E");
	delay(300);
	gotoxy(20,11);
	cprintf("A PROJECT ON FASHION INDUSTRY MANAGEMENT");
	delay(300);
	gotoxy(33,15);
	cprintf("PREPARED BY");
	sound(350);
	gotoxy(30,17);
	cprintf("DEEPANSHU AGARWAL");
	delay(100);
	gotoxy(33,20);
	cprintf("CLASS XII-A");
	nosound();
	gotoxy(26,23);
	cout<<"PRESS ANY KEY TO CONTINUE....";
	getch();
}


//////////////////////////////////////////////////////////////
int amenu()
{       int n1;
	gotoxy(32,4);
	cprintf(" MAIN MENU ");
	sound(200);
	for(int d=15;d<=63;d++)
	{       gotoxy(d,6);
		cout<<"%";
		delay(30);
	}
	sound(400);
	for(int e=6;e<=20;e++)
	{	gotoxy(15,e);
		cout<<"%";
		delay(30);
	}
	sound(300);
	for(int q=6;q<=20;q++)
	{	gotoxy(63,q);
		cout<<"%";
		delay(30);
	}
	sound(400);
	for(int c=15;c<=63;c++)
	{	gotoxy(c,21);
		cout<<"%";
		delay(30);
	}
	sound(200);
	delay(100);
	sound(400);
	delay(100);
	gotoxy(20,9);
	cout<<"1.               ADD INFORMATION";
	gotoxy(20,12);
	cout<<"2.               FABRIC/DESIGNER DETAILS";
	gotoxy(20,15);
	cout<<"3.               CHANGE PASSWORD";
	gotoxy(20,18);
	cout<<"4.               QUIT";
	nosound();
	delay(500);
	gotoxy(29,24);
	cout<<"ENTER YOUR CHOICE :";
	cin>>n1;
	delay(200);
	return(n1);
}
////////////////////////////////////////////////////////////////////
int cmenu()
{       int n1;
	gotoxy(27,4);
	cprintf(" CUSTOMER'S MAIN MENU ");
	sound(200);
	for(int d=15;d<=63;d++)
	{       gotoxy(d,6);
		cout<<"%";
		delay(30);
	}
	sound(400);
	for(int e=6;e<=20;e++)
	{	gotoxy(15,e);
		cout<<"%";
		delay(30);
	}
	sound(300);
	for(int q=6;q<=20;q++)
	{	gotoxy(63,q);
		cout<<"%";
		delay(30);
	}
	sound(400);
	for(int c=16;c<=63;c++)
	{	gotoxy(c,20);
		cout<<"%";
		delay(30);
	}
	sound(200);
	delay(100);
	sound(400);
	delay(100);
	gotoxy(20,9);
	cout<<"1.               FABRIC/DESIGNER DETAILS";
	gotoxy(20,11);
	cout<<"2.               GO SHOPPING";
	gotoxy(20,13);
	cout<<"3.               BUY SHARES";
	gotoxy(20,15);
	cout<<"4.               FASHION SHOWS";
	gotoxy(20,17);
	cout<<"5.               QUIT";
	nosound();
	delay(500);
	gotoxy(29,24);
	cout<<"ENTER YOUR CHOICE :";
	cin>>n1;
	delay(200);
	return(n1);
}

////////////////////////////////////////////////////////////////////

void addinfo()
{
  ag:   int ch;
	clrscr();
	gotoxy(30,4);
	cprintf("ADD INFORMATION MENU");
	gotoxy(1,8);
	cout<<"1.         ADD DESIGNERS                2.         ADD FABRICS"<<endl<<endl;
	cout<<"3.         ADD SHOPPING                 4.         ADD FASHION SHOWS"<<endl<<endl;
	cout<<"5.        GO BACK TO MAIN MENU          6.         QUIT"<<endl<<endl;
	cout<<"ENTER YOUR CHOICE : ";
	cin>>ch;
  aa:   switch(ch)
	{	case 1:ad_desig();
			break;
		case 2:ad_fabric();
			break;
		case 3:ad_shop();
			break;
		case 4:ad_shows();
			break;
		case 5:clrscr();
			break;
		case 6:exit(0);
		default:cout<<"Wrong choice!!!!\n";
			cout<<"Enter choice from 1 to 6.\n";
			cin>>ch;
			goto aa;
	}
	if(ch>=1 && ch<=4)
	{ cout<<"Information is added."<<endl;
	  cout<<"Press any key to continue...";
	  getch();
	  clrscr();
	  goto ag;
	}
	if(ch==5)
	{ clrscr();}
}
/////////////////////////////////////////////////////////////////

void desifab()
{       clrscr();
	designer d;
	fabric f;
	fstream dfile,ffile;
	dfile.open("DESIGNER.dat",ios::in|ios::binary);
	dfile.seekg(ios::beg);
	ffile.open("FABRIC.dat",ios::in|ios::binary);
	ffile.seekg(0);
	gotoxy(33,3);
	cout<<"DESIGNER LIST";
	gotoxy(8,6);
	cout<<"DESIGNER";
	gotoxy(25,6);
	cout<<"AGE";
	gotoxy(40,6);
	cout<<"ADDRESS";
	gotoxy(65,6);
	cout<<"CHARGE";
	int w=8;
	while(dfile)
	{
		dfile.read((char*)&d,sizeof(d));
		if(dfile.eof())
		break;
		gotoxy(7,w);
		cout<<d.desiname;
		gotoxy(23,w);
		cout<<d.age<<" yrs.";
		gotoxy(37,w);
		cout<<d.addesigner;
		gotoxy(63,w);
		cout<<"Rs. "<<d.charge;
		w+=2;
	}
	gotoxy(29,22);
	cout<<"PRESS ANY KEY TO CONTINUE..."<<endl;
	getch();
	clrscr();
	gotoxy(35,3);
	cout<<"FABRIC LIST";
	gotoxy(6,6);
	cout<<"FABRIC";
	gotoxy(17,6);
	cout<<"SUPPLIER";
	gotoxy(30,6);
	cout<<"SUPPLIER'S ADDRESS";
	gotoxy(52,6);
	cout<<"% DEMAND";
	gotoxy(65,6);
	cout<<"COST/MTS.";
	int v=8;
	while(ffile)
	{
		ffile.read((char*)&f,sizeof(f));
		if(ffile.eof())
		break;
		gotoxy(6,v);
		cout<<f.fab;
		gotoxy(17,v);
		cout<<f.supplier;
		gotoxy(30,v);
		cout<<f.add;
		gotoxy(53,v);
		cout<<f.demand<<"%";
		gotoxy(64,v);
		cout<<"Rs. "<<f.comt;
		v+=2;
	}
	gotoxy(29,22);
	cout<<"PRESS ANY KEY TO CONTINUE..."<<endl;
	getch();
	dfile.close();
	dfile.clear();
	ffile.close();
	ffile.clear();
	clrscr();
}

//////////////////////////////////////////////////////////////////////

void shopping()
{       clrscr();
	shop s[20];
	fstream sfile;
	sfile.open("SHOP.dat",ios::in|ios::binary);
	sfile.seekg(0);
	gotoxy(20,3);
	cprintf("<<===: WELCOME TO WORLD OF SHOPPING :===>>");
	gotoxy(4,5);
	cout<<"CODE NO.";
	gotoxy(14,5);
	cout<<"DRESS TYPE";
	gotoxy(28,5);
	cout<<"DESIGNER";
	gotoxy(46,5);
	cout<<"PRICE";
	gotoxy(46,6);
	cout<<"(Rs.)";
	gotoxy(56,5);
	cout<<"FEATURES";
	gotoxy(73,5);
	cout<<"STOCK";
	int v=7;
	for(int a=0;a<20;a++)
	{
		sfile.read((char*)&s[a],sizeof(s[a]));
		if(sfile.eof())
		break;
		gotoxy(4,v);
		cout<<s[a].code;
		gotoxy(14,v);
		cout<<s[a].dress;
		gotoxy(28,v);
		cout<<s[a].desig;
		gotoxy(46,v);
		cout<<s[a].price;
		gotoxy(56,v);
		cout<<s[a].featur;
		gotoxy(73,v);
		cout<<s[a].stock;
		v+=2;
	}
	gotoxy(1,23);
	cout<<"DO YOU WANT TO BUY A DRESS ?(Y/N)"<<endl;
	char c,c1;
	fflush(stdin);
	cin>>c;
	int code1,stock1,cc[20],q,pp[20],quant[20],cod[20];
	q=0;
	code1=0;
	int x=0,sum=0;
	if((c=='Y')||(c=='y'))
	{resume:cout<<"Enter code of dress : ";
		cin>>code1;
		cout<<"Enter quantity of dresses(<=5) : ";
		cin>>stock1;
		quant[x]=stock1;
		cod[x]=code1;
		x++;
		for(int z=0;z<a;z++)
		{	if(code1==s[z].code)
			{	s[z].stock-=1;
				pp[q]=(stock1*s[z].price);
				cc[q]=s[z].code;sum+=pp[q];
				q++;
			}
		}
		cout<<"DO YOU WANT TO BUY MORE(Y/N)"<<endl;
		cin>>c1;
		if((c1=='Y')||(c1=='y'))
		{	goto resume;
		}
		else
		{goto e;
		}
	}
	else
	{ clrscr();
	return;
	}
      e:clrscr();
	char ad[30],na[30];
	cout<<"Enter your name : ";
	gets(na);
	cout<<"Enter your address : ";
	gets(ad);
	gotoxy(30,4);
	cout<<"----: BILL :----";
	gotoxy(33,6);
	cout<<"NEW  ERA";
	gotoxy(2,8);
	cout<<"Name                       : "<<na;
	gotoxy(2,10);
	cout<<"Address                    : "<<ad;
	gotoxy(2,14);
	cout<<"S.No.";
	gotoxy(7,14);
	cout<<"Description";
	gotoxy(29,14);
	cout<<"Code";
	gotoxy(37,14);
	cout<<"Quantity";
	gotoxy(47,14);
	cout<<"Rate(Rs.)";
	gotoxy(59,14);
	cout<<"Cost(Rs.)";
	gotoxy(2,20);
	cout<<"_____________________________________________________________";
	gotoxy(2,22);
	cout<<"Total                                         :  ";

	int y=16,g;
	for(int b=0;b<q;b++)
	{ for(g=0;g<a;g++)
	  {if(cod[b]==s[g].code)
	   { gotoxy(2,y);
	     cout<<b+1;
	     gotoxy(29,y);
	     cout<<cod[b];
	     gotoxy(59,y);
	     cout<<pp[b];
	     y+=2;
	   }
	  }
	}
	y=16;gotoxy(59,16);cout<<pp[0];
	for(b=0;b<q;b++)
	{ for(g=0;g<a;g++)
	  {if(cod[b]==s[g].code)
	   { gotoxy(7,y);
	     cout<<s[g].featur<<" "<<s[g].dress;
	     gotoxy(37,y);
	     cout<<quant[b];
	     gotoxy(47,y);
	     cout<<s[g].price;
	     y+=2;
	   }
	  }
	}
	gotoxy(59,22);
	cout<<"Rs."<<sum;
	gotoxy(27,24);
	cout<<"----: THANK YOU :----";
	getch();
	sfile.close();
	sfile.clear();
	clrscr();
}

/////////////////////////////////////////////////////////////////

void fashow()
{       clrscr();
	shows h[20];
	fstream hfile;
	hfile.open("SHOWS.dat",ios::in|ios::binary);
	hfile.seekg(0);
	gotoxy(19,3);
	cprintf("<<===: WELCOME TO FASHION SHOWS LIST :===>>");
	gotoxy(4,5);
	cout<<"SHOW NO.";
	gotoxy(14,5);
	cout<<"DATE";
	gotoxy(28,5);
	cout<<"SEASON";
	gotoxy(38,5);
	cout<<"CELEBRITY";
	gotoxy(58,5);
	cout<<"TOTAL";
	gotoxy(57,6);
	cout<<"TICKETS";
	gotoxy(69,5);
	cout<<"COST/TICKET";
	gotoxy(72,6);
	cout<<"(Rs.)";
	int v=7;
	for(int a=0;a<20;a++)
	{
		hfile.read((char*)&h[a],sizeof(h[a]));
		if(hfile.eof())
		break;
		gotoxy(4,v);
		cout<<h[a].showno;
		gotoxy(14,v);
		cout<<h[a].date;
		gotoxy(28,v);
		cout<<h[a].season;
		gotoxy(38,v);
		cout<<h[a].celebrity;
		gotoxy(58,v);
		cout<<h[a].tickets;
		gotoxy(69,v);
		cout<<h[a].cost;
		v+=2;
	}
	gotoxy(1,23);
	cout<<"DO YOU WANT TO BUY A TICKET ?(Y/N)"<<endl;
	char c;
	fflush(stdin);
	cin>>c;
	int s1,t1,b;
	long int cost1;
	cost1=0;
	if((c=='Y')||(c=='y'))
	{	cout<<"Enter the show number : ";
		cin>>s1;
		cout<<"Enter number of tickets you want to buy : ";
		cin>>t1;
		for(b=0;b<20;b++)
		{	if(s1==h[b].showno)
			{     	h[b].tickets-=t1;
				cost1+=(h[b].cost*t1);
			}
		}
		cout<<endl<<endl<<"Total amount to be paid : "<<cost1;
		cout<<endl<<endl<<"WE HOPE THAT YOU WILL ENJOY THE SHOW"<<endl;
	}
	if((c=='N')||(c=='n'))
	{	goto ee;
	}
     ee:getch();
	hfile.close();
	hfile.clear();
	clrscr();
}

//////////////////////////////////////////////////////////////////

void buyshare()
{en:	clrscr();
	gotoxy(28,4);
	cout<<"---->> SHARES MENU <<----";
	gotoxy(28,8);
	cout<<"1 ................... GENERAL INFO";
	gotoxy(28,13);
	cout<<"2 ................... BUY SHARES";
	gotoxy(28,18);
	cout<<"3 ................... EXIT";
	for(int s=8;s<=15;s++)
	{ 	gotoxy(s,6);
		cout<<"-";
		delay(50);
		gotoxy(s,11);
		cout<<"_";
		delay(50);
	}
	for(s=7;s<=11;s++)
	{	gotoxy(8,s);
		cout<<"|";
		delay(50);
		gotoxy(15,s);
		cout<<"|";
		delay(50);
	}
	for(s=8;s<=15;s++)
	{ 	gotoxy(s,13);
		cout<<"-";
		delay(50);
		gotoxy(s,18);
		cout<<"_";
		delay(50);
	}
	for(s=14;s<=18;s++)
	{	gotoxy(8,s);
		cout<<"|";
		delay(50);
		gotoxy(15,s);
		cout<<"|";
		delay(50);
		gotoxy(16,s);
		cout<<"|";
		delay(50);
		gotoxy(17,s);
		cout<<"|";
		delay(50);
	}
	gotoxy(10,9);
	cout<<"INFO";
	gotoxy(10,15);
	cout<<"$";
	gotoxy(13,17);
	cout<<"$";
	gotoxy(34,22);
	cout<<"ENTER YOUR CHOICE : ";
	int q;
	double amount;
	cin>>q;
	if(q==1)
	{	clrscr();
		purshare sh;
		fstream shfile;
		shfile.open("SHARES1.dat",ios::in|ios::binary);
		shfile.seekg(0);
		gotoxy(35,3);
		cout<<"---- INFO ----";
		gotoxy(7,5);
		cout<<"MAJOR SHAREHOLDER  :  MR. D.C CHDDRATH (51%) ";
		gotoxy(7,7);
		cout<<"TURNOVER PER YEAR  :  Rs.900 Crores.";
		gotoxy(7,9);
		cout<<"MAJOR INVESTER     : FLEX INDUSTRIES ";
		gotoxy(7,11);
		cout<<"SHAREHOLDERS :- ";
		gotoxy(7,13);
		cout<<"NAME";
		gotoxy(29,13);
		cout<<"COMPANY";
		gotoxy(45,13);
		cout<<"ADDRESS";
		gotoxy(65,13);
		cout<<"SHARES";
		int w=14;
		while(shfile)
		{  shfile.read((char*)&sh,sizeof(sh));
		   if(shfile.eof())
		   break;
		   gotoxy(7,w);
		   cout<<sh.sname;
		   gotoxy(29,w);
		   cout<<sh.cname;
		   gotoxy(45,w);
		   cout<<sh.cad;
		   gotoxy(65,w);
		   cout<<sh.per<<" %";
		   w+=1;
		}

		gotoxy(29,22);
		cout<<"PRESS ANY KEY TO CONTINUE..."<<endl;
		getch();
		clrscr();
		goto en;
	}
	if(q==2)
	{   clrscr();
	    purshare sh;
	    fstream shfile;
	    shfile.open("SHARES1.dat",ios::app|ios::binary);
	    gotoxy(35,4);
	    cout<<"----SHARES----";
	    cout<<endl<<endl<<"COST PER SHARE : Rs.1200"<<endl;
	    cout<<"Enter number of records : ";
	    int rec;
	    cin>>rec;
	    for(int i=0;i<rec;i++)
	    {	cout<<"Enter your name : ";
		gets(sh.sname);
		cout<<"Enter name of your company : ";
		gets(sh.cname);
		cout<<"Enter address of your company : ";
		gets(sh.cad);
		cout<<"Enter % of share you want to buy : ";
		cin>>sh.per;
		shfile.write((char*)&sh,sizeof(sh));
		amount=(sh.per*1200)+1000;
		cout<<"\nTotal amount to be paid (inclusive of all taxes) : "<<amount;
		cout<<endl<<endl;
		cout<<"PLEASE DEPOSIT THE AMOUNT WITHIN 4 DAYS IN ICICI BANK";
		cout<<endl<<endl<<"THANK YOU...........\n";
	    }

	    shfile.close();
	    shfile.clear();
	    cout<<"\nPress any key to continue.\n";getch();
	    clrscr();goto en;
	}
	if(q==3)
	{ clrscr();
	}

	clrscr();
}
void end1()
{       clrscr();
	delay(300);
	for(int k=2;k<=79;k++)
	{       gotoxy(k,2);
		cout<<"#";
		gotoxy(k,24);
		cout<<"#";
	}
	for(k=3;k<=23;k++)
	{	gotoxy(2,k);
		cout<<"#";
		gotoxy(79,k);
		cout<<"#";
	}
	delay(700);
	clrscr();
	for(k=16;k<=65;k++)
	{       gotoxy(k,8);
		cout<<"#";
		gotoxy(k,18);
		cout<<"#";
	}
	for(k=8;k<=18;k++)
	{	gotoxy(16,k);
		cout<<"#";
		gotoxy(65,k);
		cout<<"#";
	}
	delay(700);
	clrscr();
	for(k=23;k<=58;k++)
	{       gotoxy(k,11);
		cout<<"#";
		gotoxy(k,15);
		cout<<"#";
	}
	for(k=11;k<15;k++)
	{	gotoxy(23,k);
		cout<<"#";
		gotoxy(58,k);
		cout<<"#";
	}
	gotoxy(35,13);
	cout<<"THANK YOU !!!!";
	delay(2000);
}
void main()
{       char login;
	clrscr();
	welcome();
	delay(200);
	clrscr();
	gotoxy(2,2);
	cout<<"ARE YOU AUTHORITY(A) OR CUSTOMER(C)?A/C:\n";
	cin>>login;
	if(login=='A' || login=='a')
	{  n6=password();
	  if(n6==0){ char am;
		     delay(2000);
		     cout<<"\nDo you want to continue with the customer's main menu?Y/N:\n";
		     cin>>am;
		     if(am=='Y' || am=='y')
		     { clrscr();goto log;}
		     if(am=='N' || am=='n')
		     { cout<<"\nABORTING....\n";delay(1570);end1();exit(0);}
		   }
	  if(n6==1)
	  { delay(2000);clrscr();
	  while(1){n1=amenu();
  bb:	switch(n1)
	{
		case 1:addinfo();
			break;
		case 2:desifab();
			break;
		case 3:changepass();
			break;
		case 4:end1();
			exit(0);
			break;
		default:cout<<"WRONG CHOICE !!!!\n";
			cout<<"Enter choice from 1 to 4.\n";
			cin>>n1;
			goto bb;
	}
	}
    }
    }

      if(login=='C' || login=='c')
      {	log:  while(1){n7=cmenu();
  dd:	switch(n7)
	{
		case 1:desifab();
			break;
		case 2:shopping();
			break;
		case 3:buyshare();
			break;
		case 4:fashow();
			break;
		case 5:end1();
			exit(0);
			break;
		default:cout<<"WRONG CHOICE !!!!\n";
			cout<<"Enter choice from 1 to 5.\n";
			cin>>n7;
			goto dd;
	}
    }
  }
}


