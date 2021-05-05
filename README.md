# SemaKhan-EC_Calculator_Khan
#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>
#include <iostream>
using namespace std;
int main()
{

    char s[255];
    char s1[255];
    int m;
    int n;
    cin >> s;
    int i = 0;
    int flag1 = 0;
    while (s[i] != '\0')
    {
        if (!isdigit(s[i])) //check if all are digits
        {
            cout << "\nplease enter valid number";
            flag1 = 1;
            break;
        }
        i++;
    }
    cout << endl;
    cin >> s1;
    int flag2 = 0;
    i = 0;
    while (s1[i] != '\0')
    {
        if (!isdigit(s1[i])) //check if all are digits
        {
            cout << "\nplease enter valid number";
            flag2 = 1;
            break;
        }
        i++;
    }
    if (flag1 == 0)
    {
        m = atoi(s);
    } //convert to int
    else
    {
        cout << "\nnumber 1 was not valid can't perform operation ";
    }
    if (flag2 == 0)
    {
        n = atoi(s1); // convert to int
    }
    else
    {
        cout << "number 2 was not valid can't perform operation ";
    }
    if (flag1 == 0 && flag2 == 0)
    {
        cout << "\nenter the operation you want to perfrom: ";
        char op;
        cin >> op;
        switch (op)
        {
        case '+':cout << "\n" << m + n;
            break;
        case '-':cout << "\n" << m - n;
            break;
        case '*':cout << "\n" << m * n;
            break;
        case '/':cout << "\n" << m / (n * 1.0);
            break;
        default:cout << "\nenter a valid operator";
        }
    }
    cout << endl;

}
