# Code
```cpp

#include<iostream>
#include<string.h>
using namespace std;
void encrypt(char code[],int k)
{
    int n=strlen(code);
    char c;
    for(int i=0;i<n;i++)
    {
        if(isupper(code[i]))
        {
            c=char((int(code[i])-65+k)%26+65);
            code[i]=c; 
        }
        else if(islower(code[i]))
        {
            c=char((int(code[i])-97+k)%26+97);
            code[i]=c; 
        }
    }
}
int main()
{
    int k;
    char code[50];
    cout<<"\nenter string to be encrypted: ";
    cin.getline(code,100);
    cout<<"\nenter shift/key: ";
    cin>>k;
    encrypt(code,k);
    cout<<"\nEncrypted code: ";
    cout<<code;
    return 0;
}
```

# Explanation
The user is asked to input a string which he/she wants to be encrypted and also how many shifts to be applied. 

The *encrypt()* is called and the parameters are passed. 
* It checks if the characters in the string is in uppercase or lowercase, converts it to **plaintext** accordingly
(with proper usage of ASCII values) and adds the shift.
* **Mod26** might seem unnecessary for some values but for values above 26,it is highly necessary as it restricts
values above 26(plaintext goes from 0 to 25,a total of 26).

Finally the encrypted code is displayed.       
