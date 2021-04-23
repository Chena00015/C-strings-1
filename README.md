#include <stdio.h>

int main() {

char string1[100];
int i, vowels, consonants;

printf("Input sentence: ");
gets(string1);

i=0;

while(string1[i]!='\0')
    {
        if(string1[i]=='a' ||string1[i]=='e' ||string1[i]=='i' ||string1[i]=='o' ||string1[i]=='u')
           string1[i]=string1[i]-32;
           i++;
     
    }
    
        vowels=0, consonants=0;
        
        for (int i = 0; string1[i] != '\0'; ++i) {
        
        if (string1[i] == 'a' || string1[i] == 'e' || string1[i] == 'i' ||
            string1[i] == 'o' || string1[i] == 'u' || string1[i] == 'A' ||
            string1[i] == 'E' || string1[i] == 'I' || string1[i] == 'O' ||
            string1[i] == 'U') {
            ++vowels;
            
    }   else 
        if ((string1[i] >= 'a' && string1[i] <= 'z') || (string1[i] >= 'A' && string1[i] <= 'Z')) { 
            ++consonants;
    }
    
    }
    
    printf("\nString Converted: ");
    puts(string1);
     

printf("\nLength of String: %d\n", i);

printf("\nVowels: %d\n", vowels);

printf("\nConsonants: %d\n", consonants);

return 0;

}
