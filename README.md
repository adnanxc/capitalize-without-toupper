# capitalize-without-toupper
capitalize the first letter of each word

#include <iostream>
using namespace std;

string modify (string a){
    string n = a;
    int length = a.length();
    if(a[0]>=97 && a[0]<=122){
    n[0]=a[0] - 32;
    }

    for(int i=1; i<length; i++){
        if(a[i]==' '){
            int x = a[i+1] - 32;
            n[i+1]= (char)x;
        }

    }

   return n;
}




int main(){
    string s;
    cout << "Enter your string: ";
    getline(cin,s);

    cout << "New string: " << modify(s);
}
