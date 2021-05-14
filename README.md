# prime_fact

#include<bits/stdc++.h>
using namespace std;
void primeFactors(long long int n,vector<int>&v)
{
if(n%2!=0)

cout<<2<< "^" <<0<<"*";

else
{
while (n % 2 == 0)
{
n = n/2;
}
}
for (int i = 3; i <= (n*n); i = i + 2)
{
while (n % i == 0)
{
v.push_back(i);
n = n/i;
}
}
if (n > 2)
v.push_back(n);
}
int main()
{
     int t;
     cin>>t;
     while(t--)
     {
        long long int n;
         cin>>n;
         vector<int>v;
           primeFactors(n,v);
   map<int,int>m;
         for(int i=0;i<v.size();i++)
         {
           m[v[i]]++;
         }

for(auto it=m.begin();it!=m.end();it++)
{
if(it==m.begin())
cout<<it->first<<"^"<<it->second;
else
cout<<"*"<<it->first<<"^"<<it->second;
}
cout<<endl;

     }

}
