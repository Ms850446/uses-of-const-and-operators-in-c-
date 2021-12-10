const uses :
1-constant variables >> while declaring a variable as constant and this make us unable to change
it in the rest of the code and also require to initialize it while declaring .                      
ex :    
const float pi = 22 / 7.0;\
pi = 3.14;//Error\
output :\
Error	C3892	'pi': you cannot assign to a variable that is const
/////

2- we can make a constant pointer to point to a constant variable and this is the way to
declare a pointer to the any constant variable and that's make us unable to change the value
of the variable that the pointer point to
ex :
const float pi = 22 / 7.0;//ok
float const* address = &pi;//ok
*address=3.14//Error

3- we can make a constant pointer that can't change the address of it once it is
initialized or declared to any variable
ex :
int x = 9;  int f = 8;//ok
int* const Xaddress = &x;//ok
Xaddress=&f; //Error
Xaddress++; //Error

4- 

