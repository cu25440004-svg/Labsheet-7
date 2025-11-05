// ============================================================
// 1. Find Length of String using strlen()
// ============================================================
#include<iostream>
#include<string.h>
using namespace std;
int main(){
 char s[50];
 cout<<"Enter string: "; cin>>s;
 cout<<"Length="<<strlen(s);
 return 0;
}

/*
Output:
Enter string: hello
Length=5
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 2. Count Number of Vowels in String using strlen()
// ============================================================
#include<iostream>
#include<cstring>
using namespace std;
int main(){
 char s[200];
 int c=0;
 cout<<"Enter string: ";
 cin.ignore();
 cin.getline(s,200);
 for(int i=0;i<strlen(s);i++){
  char ch=s[i];
  if(ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u'||ch=='A'||ch=='E'||ch=='I'||ch=='O'||ch=='U')
   c++;
 }
 cout<<"Vowels="<<c;
 return 0;
}

/*
Output:
Enter string: Hello World
Vowels=3
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 3. Copy One String to Another using strcpy()
// ============================================================
#include<iostream>
#include<string.h>
using namespace std;
int main(){
 char a[50],b[50];
 cout<<"Enter string: "; cin>>a;
 strcpy(b,a);
 cout<<"Copied string: "<<b;
 return 0;
}

/*
Output:
Enter string: world
Copied string: world
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 4. Check if Two Strings are Equal using strcpy() & Comparison
// ============================================================
#include<iostream>
#include<string.h>
using namespace std;
int main(){
 char a[50],b[50],x[50],y[50];
 cout<<"Enter 1st: "; cin>>a;
 cout<<"Enter 2nd: "; cin>>b;
 strcpy(x,a); strcpy(y,b);
 cout<<(strcmp(x,y)==0?"Equal":"Not Equal");
 return 0;
}

/*
Output:
Enter 1st: hello
Enter 2nd: hello
Equal
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 5. Concatenate Two Strings using strcat()
// ============================================================
#include<iostream>
#include<string.h>
using namespace std;
int main(){
 char a[50],b[50];
 cout<<"Enter 1st: "; cin>>a;
 cout<<"Enter 2nd: "; cin>>b;
 strcat(a,b);
 cout<<"Joined: "<<a;
 return 0;
}

/*
Output:
Enter 1st: good
Enter 2nd: morning
Joined: goodmorning
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 6. Join First and Last Name using strcat()
// ============================================================
#include<iostream>
#include<string.h>
using namespace std;
int main(){
 char f[50],l[50];
 cout<<"First name: "; cin>>f;
 cout<<"Last name: "; cin>>l;
 strcat(f," "); strcat(f,l);
 cout<<"Full name: "<<f;
 return 0;
}

/*
Output:
First name: Akash
Last name: Singh
Full name: Akash Singh
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 7. Compare Two Strings using strcmp()
// ============================================================
#include<iostream>
#include<string.h>
using namespace std;
int main(){
 char a[50],b[50];
 cout<<"Enter 1st: "; cin>>a;
 cout<<"Enter 2nd: "; cin>>b;
 int r=strcmp(a,b);
 if(r==0) cout<<"Equal";
 else if(r>0) cout<<"1st>2nd";
 else cout<<"1st<2nd";
 return 0;
}

/*
Output:
Enter 1st: cat
Enter 2nd: bat
1st>2nd
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 8. Check if Two Strings are Equal (Case-Sensitive) using strcmp()
// ============================================================
#include<iostream>
#include<string.h>
using namespace std;
int main(){
 char a[50],b[50];
 cout<<"Enter 1st: "; cin>>a;
 cout<<"Enter 2nd: "; cin>>b;
 cout<<(strcmp(a,b)==0?"Equal":"Not Equal");
 return 0;
}

/*
Output:
Enter 1st: Apple
Enter 2nd: apple
Not Equal
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 9. Arrange Array of Strings in Alphabetical Order using strcmp()
// ============================================================
#include<iostream>
#include<string.h>
using namespace std;
int main(){
 int n; cout<<"Count: "; cin>>n;
 char s[10][50],t[50];
 for(int i=0;i<n;i++) cin>>s[i];
 for(int i=0;i<n-1;i++)
  for(int j=i+1;j<n;j++)
   if(strcmp(s[i],s[j])>0){ strcpy(t,s[i]); strcpy(s[i],s[j]); strcpy(s[j],t); }
 cout<<"Sorted:\n";
 for(int i=0;i<n;i++) cout<<s[i]<<"\n";
 return 0;
}

/*
Output:
Count: 3
cat bat apple
Sorted:
apple
bat
cat
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 10. Reverse a String using strrev()
// ============================================================
#include<iostream>
#include<string.h>
using namespace std;
int main(){
 char s[50];
 cout<<"Enter: "; cin>>s;
 cout<<"Reversed: "<<strrev(s);
 return 0;
}

/*
Output:
Enter: hello
Reversed: olleh
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 11. Check if String is Palindrome using strrev()
// ============================================================
#include<iostream>
#include<string.h>
using namespace std;
int main(){
 char s[50],r[50];
 cout<<"Enter: "; cin>>s;
 strcpy(r,s); strrev(r);
 cout<<(strcmp(s,r)==0?"Palindrome":"Not Palindrome");
 return 0;
}

/*
Output:
Enter: madam
Palindrome
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 12. Find First Occurrence of Character using strchr()
// ============================================================
#include<iostream>
#include<string.h>
using namespace std;
int main(){
 char s[50],ch; cout<<"Enter: "; cin>>s;
 cout<<"Find char: "; cin>>ch;
 char *p=strchr(s,ch);
 if(p) cout<<"Found at pos "<<(p-s);
 else cout<<"Not Found";
 return 0;
}

/*
Output:
Enter: banana
Find char: n
Found at pos 2
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 13. Find Last Occurrence of Character using strrchr()
// ============================================================
#include<iostream>
#include<string.h>
using namespace std;
int main(){
 char s[50],ch; cout<<"Enter: "; cin>>s;
 cout<<"Find char: "; cin>>ch;
 char *p=strrchr(s,ch);
 if(p) cout<<"Last pos="<<(p-s);
 else cout<<"Not Found";
 return 0;
}

/*
Output:
Enter: banana
Find char: a
Last pos=5
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 14. Find a Substring inside Another String using strstr()
// ============================================================
#include<iostream>
#include<string.h>
using namespace std;
int main(){
 char s[50],sub[50];
 cout<<"Enter main: "; cin>>s;
 cout<<"Enter sub: "; cin>>sub;
 char *p=strstr(s,sub);
 if(p) cout<<"Found at pos "<<(p-s);
 else cout<<"Not Found";
 return 0;
}

/*
Output:
Enter main: pineapple
Enter sub: apple
Found at pos 4
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 15. Check if One String is Present in Another using strstr()
// ============================================================
#include<iostream>
#include<string.h>
using namespace std;
int main(){
 char s[50],sub[50];
 cout<<"Enter main: "; cin>>s;
 cout<<"Enter sub: "; cin>>sub;
 cout<<(strstr(s,sub)?"Present":"Not Present");
 return 0;
}

/*
Output:
Enter main: hello
Enter sub: ell
Present
*/

cout<<"\n--------------------------------------------\n";
// ============================================================
// 16. Count the Number of Words in a String using strlen() and spaces
// ============================================================
#include<iostream>
#include<cstring>
using namespace std;
int main(){
 char s[200]; int c=1;
 cout<<"Enter string: ";
 cin.ignore();
 cin.getline(s,200);
 for(int i=0;i<strlen(s);i++)
  if(s[i]==' ' && s[i+1]!=' ' && s[i+1]!='\0') c++;
 cout<<"Words="<<c;
 return 0;
}

/*
Output:
Enter string: This is my book
Words=4
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 17. Remove All Vowels from a String using String Functions
// ============================================================
#include<iostream>
#include<cstring>
using namespace std;
int main(){
 char s[200],r[200]; int j=0;
 cout<<"Enter string: ";
 cin.getline(s,200);
 for(int i=0;i<strlen(s);i++)
  if(!strchr("aeiouAEIOU",s[i])) r[j++]=s[i];
 r[j]='\0';
 cout<<"Without vowels: "<<r;
 return 0;
}

/*
Output:
Enter string: Education
Without vowels: dctn
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 18. Copy Only First 5 Characters using strncpy()
// ============================================================
#include<iostream>
#include<cstring>
using namespace std;
int main(){
 char s1[100],s2[100];
 cout<<"Enter string: "; cin>>s1;
 strncpy(s2,s1,5);
 s2[5]='\0';
 cout<<"Copied(5 chars): "<<s2;
 return 0;
}

/*
Output:
Enter string: Computer
Copied(5 chars): Compu
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 19. Join Multiple Strings into One Sentence using strcat()
// ============================================================
#include<iostream>
#include<cstring>
using namespace std;
int main(){
 char s1[50],s2[50],s3[50],s[200]="";
 cout<<"Enter 1st word: "; cin>>s1;
 cout<<"Enter 2nd word: "; cin>>s2;
 cout<<"Enter 3rd word: "; cin>>s3;
 strcat(s,s1); strcat(s," ");
 strcat(s,s2); strcat(s," ");
 strcat(s,s3);
 cout<<"Sentence: "<<s;
 return 0;
}

/*
Output:
Enter 1st word: I
Enter 2nd word: love
Enter 3rd word: coding
Sentence: I love coding
*/

cout<<"\n--------------------------------------------\n";

// ============================================================
// 20. Check Whether Two Strings are Anagrams using String Functions
// ============================================================
#include<iostream>
#include<cstring>
#include<algorithm>
using namespace std;
int main(){
 char a[100],b[100];
 cout<<"Enter 1st: "; cin>>a;
 cout<<"Enter 2nd: "; cin>>b;
 if(strlen(a)!=strlen(b)){ cout<<"Not Anagram"; return 0; }
 sort(a,a+strlen(a));
 sort(b,b+strlen(b));
 cout<<(strcmp(a,b)==0?"Anagram":"Not Anagram");
 return 0;
}

/*
Output:
Enter 1st: listen
Enter 2nd: silent
Anagram
*/

cout<<"\n--------------------------------------------\n";
