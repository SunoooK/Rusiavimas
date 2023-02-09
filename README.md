# Rusiavimas
#include <iostream>
#include <vector>

using namespace std;

void daugybarusiavimas (vector<int>(skaiciai), vector<int>(&skaiciaikv), int n)
{
    for (int i = 0; i < n; ++i)
        skaiciaikv.push_back(skaiciai[i]*skaiciai[i]);

        sort(skaiciaikv.begin(),skaiciaikv.end());
}

void spausdinti (vector<int>(skaiciaikv))
{
    for(int elem:skaiciaikv)
        cout<<elem<<" ";
}

int main() {
    vector<int>skaiciai{};
    int sk;
    cout<<"Irasykite kieki skaiciu: ";
    cin>>sk;
    int laikinas;
    for (int i = 0; i < sk; ++i)
    {
        cin>>laikinas;
        skaiciai.push_back(laikinas);
    }
    int n=skaiciai.size();
    vector<int>skaiciaikv{};

    daugybarusiavimas(skaiciai,skaiciaikv,n);
    spausdinti(skaiciaikv);
    return 0;
}

