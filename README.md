const uses :\
1-constant variables >> while declaring a variable as constant and this make us unable to change
it in the rest of the code and also require to initialize it while declaring .\
ex :\
const float pi = 22 / 7.0;\
pi = 3.14;//Error\
output :\
Error	C3892	'pi': you cannot assign to a variable that is const\
////\
\
2- we can make a constant pointer to point to a constant variable and this is the way to
declare a pointer to the any constant variable and that's make us unable to change the value
of the variable that the pointer point to\
ex :\
const float pi = 22 / 7.0;//ok\
float const* address = & pi;//ok\
*address=3.14//Error\
\
3- we can make a constant pointer that can't change the address of it once it is
initialized or declared to any variable\
ex :\
int x = 9;  int f = 8;//ok\
int *const Xaddress = &x;//ok\
Xaddress=&f; //Error\
Xaddress++; //Error\
\
4- we can make a function with constant arguments and that's will make the function unable
to change the value of this variable when it is passed \
ex :\
int Double(const int d){\
    d=d*2;//Error >>can't change the value of the constant \
    return d;\
    }\
\
5-we can do the same if the variable is passed by reference to the function and that's to 
prevent it from modifying the value of the variable \
ex : \
int Double(const int& d){\
d=d*2;//Error\
return d;\
}\
\
6- we can make a constant data member for any class so that we can't change its value\
ex:\
class Circle{
\ public :const float pi= 3.14;
\}\
\
/////////////////////////////////////////////////\
\
uses of the & operator in c++\
\ 
1- Bitwise And : and it is used to compare each bit of the first operand to 
the bit of the second operand >> if they are both 1 then it is set to be 1
else it is set to be 0/
ex :\
unsigned short a = 0x5555;      // pattern 0101 ...  \
unsigned short b = 0xAAAA;      // pattern 1010 ...\
cout << hex << ( a & b ) << endl;// the output will be 0\
\
2-address operator as it is used to get the address of the variable and assign it 
to a pointer as example or just to get the address of the variable 
\ex : \
int x=9;\
cout<<&x<<endl;\
\
3-can be used as logic and gate in if conditions \
ex : \
bool x=true ,y=false;\
if(x&&y){\
cout<<"Wrong operation" ;}\
else \
cout<<"it is the and operation and give false"<<endl;\
\

    
