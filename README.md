# prefixalog
#include <iostream>
using namespace std;
int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL);
	int t;
	cin>>t;
	while(t--)
	{
		int n;
		cin>>n;
		for(i=1;i<=n;i++)
		{
			cin>>a[i];
		}
		int q;
		cin>>q;
		long long prefix[n+1]={0};
		prefix[1]=a[1];
		for(i=2;i<=n;i++)
		{
			prefix[i]=prefix[i-1]+a[i];
		}
		while(q--)
		{
			int l,r;
			cin>>l>>r;
			if(l==1)
			{
				cout<<prefix(r)<<"\n";
			}
			else
			{
				cout<<prefix(r)-prefix(l-1)<<"\n";
			}
		}
	}
