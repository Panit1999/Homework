#include<iostream>
#include<iomanip>
using namespace std;
void calprice(float price[5][3]);
void display(string name[5],float price[5][3]);
int main(void)
{	float price[5][3];
	string name[5];
		for(int i=0;i<5;i++){	
		cout << "Enter Product Name : ";
		cin >> name[i];
		cout << "Price : ";
		cin >> price[i][0];
		}
		calprice(price);
		display(name,price);
	
	return 0;
}
void calprice(float price[5][3]){
	
	for (int i=0;i<5;i++){
		price[i][1] = price[i][0]*0.07f;
		price[i][2] = price[i][0]+price[i][1];
}
}

void display(string name[5],float price[5][3])
{
	cout<<setw(30)<<setfill('-')<<" "<<endl;
	  cout<<"No."<<"\t"<<"Product"<<"\t"<<"Price"<<"\t"<<"Vat7%"<<"\t"<<"Net"<<endl;
	  cout<<setw(30)<<setfill('-')<<" "<<endl;

	  for ( int i = 0; i < 5; ++i) {
		  cout << fixed;
		  cout << setprecision(2);
		  cout<< i+1 <<"."<<"\t" << name[i] <<"\t"<< price[i][0]<<"\t" << price[i][1] << "\t"<<price[i][2]<<endl;
	  }
	  cout<<setw(30)<<setfill('-')<<" "<<endl;
	  cout<<endl;
}
