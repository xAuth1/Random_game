#include <iostream>
#include <cstdlib>
#include <time.h>

using namespace std;

int liczba, strzal, ile_prob=0;

int main()
{
    cout << "Witaj! Pomyœlalem sobie liczbe 1...100" << endl;
    srand(time(NULL));
    liczba = rand()%100+1;

    while(strzal!=liczba)
    {
        ile_prob++;

        cout<<"Zgadnij jaka (to twoja "<<ile_prob<<" proba)";
        cin>>strzal;

        if(strzal==liczba)
          cout<<"Wygrales w "<<ile_prob<<"probie"<<endl;

        else if(strzal<liczba)
          cout<<"Za malo"<<endl;

        else if(strzal>liczba)
            cout<<"Za duzo"<<endl;
    }

    system("pause");

    return 0;
}
