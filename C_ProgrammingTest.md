# C_ProgrammingTest
# These are the answers to the questionnaire.

TASK1

__________________________________________
1) It is a data type that holds any one character that could be any character. e.g. "1", "A", "&".
2) It indicates that it is a list. In this case, this list contains strings.
3) 168
4) AddressIP[1] instead of AddressIP[0].
__________________________________________

TASK2
__________________________________________
#include <stdio.h>
unsigned char AddressIP[]={192,17,0,5};
char dot = '.';
int main()
{
printf("%u", (unsigned int)AddressIP[0]);
printf(".");
printf("%u", (unsigned int)AddressIP[1]);
printf(".");
printf("%u", (unsigned int)AddressIP[2]);
printf(".");
printf("%u", (unsigned int)AddressIP[3]);
return 0;
}
__________________________________________

TASK3

__________________________________________
1) const is a constant that does not allow changing of its value after it is declared. It is usually used to avoid and detect any mistakes.
2) They are called bitwise operations or bitmasks. The byte AddressIP is shifted 24 places to the right and $0FF performs bitwise operation which then becomes 168.
__________________________________________

TASK4

__________________________________________
#include <stdio.h>
unsigned long AddressIP=0xA80C0005;
unsigned long SubnetMask = 0xFFFFFFF0;

int main()
{
GetList(AddressIP,0xFFFFFFF0);
return 0;
}

void GetList (unsigned long NetworkID, unsigned long SubnetMask) {
unsigned char Byte1 = (AddressIP>>24)&0xFF;
unsigned char Byte2 = (AddressIP>>16)&0xFF;
unsigned char Byte3 = (AddressIP>>8)&0xFF;
unsigned char Byte4 = (AddressIP)&0xFF;
printf("==> %d.%d.%d.%d",Byte1,Byte2,Byte3,Byte4);
}

1) It is the initial SubnetMask (255.255.255.240) and it is reserved.
2) It is the last SubnetMask (255.255.255.255) and it is reserved.
3) It displays a list of available networkID's.
__________________________________________
