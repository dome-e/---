#include <iostream>
#include <cstdlib>
#include <time.h>
#include <unistd.h>
using namespace std;

int main()
{
    //int a, b, c, d, e, f;
    //int t, y, u, i, o, p;
    int wygrane[6];

// wygrane[2] thats how you access them arrays



   srand(time(NULL)); //nie moze byc w funkcji for bo zepsuje losowanie


system("clear");
sleep (1);


   for (int i=0; i<6; i++)
 {
         wygrane[i]= rand()%49+1;
int n;
         for( n=0; n<i; n++)
       {
       while (wygrane[i]==wygrane[n])
       {wygrane[i]= rand()%49+1;}
        }

    n=0;




/*
       cout<< "\a" << wygrane[i]<< endl; // glupotka- jezeli napisze sie \ to znaczy ze bedzie sie dziac cos nietypowego
                                         // w tym przypadku chodzi o \a od audio, mozna tez uzyc \n zamiast endl;


        sleep(1); // glupotka zeby byly przerwy miedzy wyswietlaniem sie licz
*/


    }


cout << "LOTTO \n Podaj 6 liczb z zakresu 1-49 \n Kazda z nich potwierdz wciskajac przycisk ENTER";



bool noijak;
int wybrane[6];
int suma=0;

cout <<endl;


for (int x=0; x<6; x++)
{
   // cout << "podaj liczbe z zakresu 1-49:";
    cin >> wybrane[x];

}

system("clear"); //na macu zmien cls na clear
sleep(1);

for (int s=0; s<6; s++)
{
    int g;
    for ( g=0; g<6; g++)
   {



    if (wybrane[s]==wygrane[g])
       {noijak=true;}

    if (wybrane[s]!=wygrane[g])
        {noijak=false;}









     if (noijak==true)
    {

    if (suma<1)
    {cout << endl<<endl;
    }



cout << " Gratulacje, wybrana przez Ciebie "<< wygrane[g] << " to liczba wygrywajaca B))"<< " \a"<< "  \a" << "  \a "<<endl;

    suma++;
sleep(2);

    }

   /* if (noijak==false)
        cout <<"  glupio, bo " << v << ". liczba niejes wygrywajaca B( \n";
   */

   }



   g=0;
}

if(suma==0)
    {
        sleep(1);
        cout<< "Spróbuj jeszcze raz";
        sleep(2);}
cout << "\n \n Liczba trafionych liczb:"<< suma<< endl<< endl<<endl;


sleep(1);
cout<< "--- WIECEJ INFORMACJI --- \n";
cout << endl<< "\n Liczby wygrywajace:          ";
    for(int p=0; p<6; p++)

    {cout << "|";
    if (wygrane[p]<10)
        cout << " ";
    cout<< wygrane[p]<< "|";}
    cout<< endl;


cout << "\n Liczby wybrane przez Ciebie: ";
    for(int p=0; p<6; p++)

    {cout << "|";
    if (wybrane[p]<10)
        cout << " ";
    cout<< wybrane[p]<< "|";}
       cout<< endl;




    cout <<endl<<endl<<endl;
    return 0;
}
