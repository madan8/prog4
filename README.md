Pink is sad because of some reasons, he wants to cheer up by listening to some songs
from his favorite band, Pink Floyd.
There are N records and Pink will be happy if he listens to them in the ascending
order, i.e., first the song No. 1, then No.2 and so on (He has to listen to all the N songs
to become Happy).
Pink is delivered his records in some given order, he can either add the record to the
Playlist in the delivered order or put some on another table. After being put on the
table only the topmost record can be added to the playlist at any time.
Print whether Pink will be sad or happy after the delivery of the records.#include<bits/stdc++.h>

using namespace std;

#define ll long long int

int main()
{
ll n;
cin>>n;

ll a[n+1];

for(ll i=1;i<=n;i++)

cin>>a[i];

ll c=1;

stack<ll> s;

for(ll i=1;i<=n;i++)

{

s.push(a[i]);

while((!s.empty()) && (c==s.top()))

{

c++;

s.pop();

}

}

if(!s.empty())

cout<<"Sad"<<endl;

else

cout<<"Happy"<<endl;

}
