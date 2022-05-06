#include <iostream>
using namespace std;
int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL);
	int T;
	cin>>T;
	while(T--)
	{
		int N;
		cin>>N;
		int arr[N];
		for(int i=1;i<=N;i++)
		{
			cin>>arr[i];

		}
		long long int prefix[N+1]={0};
		prefix[1]=arr[1];
		for(int i=2;i<=N;i++)
		{
			prefix[i]=prefix[i-1]+arr[i];
		}

		int Q;
		cin>>Q;
		while(Q--){
		long long int L,R;
		cin>>L>>R;
		if(L==1)
		{
			cout<<prefix[R]<<"\n";

		}
		else
		{
			cout<<prefix[R]-prefix[L-1]<<"\n";
		}
		/*int sum=0;
		for(int i=L;i<=R;i++)
		{
			sum=sum+arr[i];
		}

		cout<<sum<<endl;*/

	}
	}
}
