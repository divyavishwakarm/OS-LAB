#include <iostream>

using namespace std;
class S{
    private:
    int stck[100];
	int top=-1;
    public:
    void push(int value)
    {
        if(stackfull())
        {
            cout<<"overflow"<<endl;
        }
        else
        {
            top++;
            stck[top]=value;
        }
    }
    bool stackfull()
    {
        if(top==99)
        return true;
        else
        return false;
        
    }
    int pop()
    {
        if(stackempty())
        cout<<"underflow"<<endl;
        else
        return stck[top--];
        return(-1);
    }
    bool stackempty()
    {
        if(top==-1)
        return true;
        else
        return false;
    }
  void  display()
    {
        for(int i=0;i<=top;i++)
        {
            cout<<stck[i]<<endl;
        }
    }
};

int main()
{
    S s;
    int ch;
    do{
        cout<<"1.push"<<endl;
        cout<<"2.pop"<<endl;
        cout<<"3.display"<<endl;
        cout<<"4.exit"<<endl;
        cout<<"enter choice"<<endl;
        cin>>ch;
        switch(ch)
        {
            case 1:int value;
			cout<<"Enter the value"<<endl;
			cin>>value;
			s.push(value);
            break;
            
            case 2:s.pop();
            break;
            
            case 3:s.display();
            break;
        }
    }
    while(ch!=4);
}
