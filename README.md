#include <iostream>

using namespace std;

void Bubblesort( int ElementNum, int *tab)

{
    for ( int i = 1; i < ElementNum; i++)
    {
        for ( int j = ElementNum - 1; j >= 1; j--)
        {
            if ( tab [j] < tab [j - 1])
            {
                int yeet;
                yeet = tab[j - 1];
                tab [j - 1] = tab [j];
                tab[j] = yeet;
            }
        }
    }
}



int main()
{

    int *arr;
    int ElementNumber;

    for ( int loop = 0; loop <99999999; loop++)
    {
        cout << "How many numbers would you like to sort?" << endl;
        cin >> ElementNumber;
        arr = new int[ElementNumber];
        cout << "Type your numbers" << endl;


        for (int i = 0; i < ElementNumber; i++)
        {
            cin >> arr[i];
        }
        Bubblesort(ElementNumber,arr);

        cout << "--------------------------------------" << endl;
        for (int i = 0; i < ElementNumber; i++)
        {
            cout << arr[i] <<endl;
        }

        delete [] arr;
    }
    return 0;
}
