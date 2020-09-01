#include<iostream>
#include<conio.h>
#include<string.h>
#include<stdlib.h>

using namespace std;
template<class t>
class stacks1
{
	int n;
	int top;
	t *nodes;
	
	public:
    	stacks1(int t1)
        {
			n=t1;
            top=-1;
            nodes=new t[n];
        }

		void push(int j)
        {
            if(top<n)
			{
                top =top+1;
				nodes[top]=j;
			}
            else
			{
				cout<<" stack is full overflow! "<<endl;
			}
    	}
		
		t pop()
        {
            if(top<0)
			{
                return 0;
            }
            else
            	return(nodes[top--]);
        }

	    ~stacks1()
        {
            delete[]nodes;
        }

		int isempty()
        {
           if(top==-1)
           {
                return 1;
           }
           else return 0;
        }

		void display()
        {
            for(int i=top;i>=0;--i)
                cout<<""<<nodes[i];
        }
};

int main()
{
	int i2=1;
	do{
		int c1,c2;
		cout<<"\n\t\t\tSTACK OPERATION \n\n";
		cout<<" Enter two large No to be added\n"<<endl;
		string str1,str2;
		cout<<" Enter the No 1 \n";
		cin>>str1;
		cout<< "\nEnter the No 2\n";
		cin>>str2;

		c1=str1.size();
		c2=str2.size();

		stacks1<int> stk1(c1);
		stacks1<int> stk2(c2);
		stacks1<int> stk3(c1+c2);

		int b=0;
		while(b!=c1)
		{
			stk1.push(str1[b]-'0') ;++b;
		}
		b=0;
		while(b!=c2)
		{
			stk2.push(str2[b]-'0') ;
			b++;
		}

		int k=c1, l=c2, m, c=0;
		if(c1>=c2)
		{
			while(k>=0)
			{
				m=c+stk1.pop()+stk2.pop();
				c=0;
				if(m>=10)
				{
					c=1;
					m=m%10;
				}
				stk3.push(m);
				--k;
			}
		}

		c=0;
		if(c2>c1)
		{
			while(l>=0)
			{
				m=c+stk1.pop()+stk2.pop();
				c=0;
				if(m>=10)
				{
					c=1;
					m=m%10;
				}
				stk3.push(m);
				--l;
			}
		}

		cout<<"\nBoth no added \n\n";
		cout<<"\nThe result is \n\n"<<endl;
		cout<<"\t";

		stk3.display();

		cout<<endl;
		cout<<"\t\n Do you want to add again : Press Y \n";
		char ch2;
		cin>>ch2;

		if(ch2=='y' || ch2=='Y')
			continue;
		else 
			break;
	}while(i2);

	return 0;
}
