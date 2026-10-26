# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main() {
    char text[100];
    int key;

    printf("Enter the plain text: ");
    scanf("%s", text);
    printf("Enter the key value: ");
    scanf("%d", &key);

    for (int i = 0; i < strlen(text); i++) {
        char ch = text[i];
        int shift = key % 26;

        if (ch >= 'a' && ch <= 'z')
            text[i] = (ch - 'a' + shift + 26) % 26 + 'a';
        else if (ch >= 'A' && ch <= 'Z')
            text[i] = (ch - 'A' + shift + 26) % 26 + 'A';
    }

    printf("Cipher text: %s\n", text);
    return 0;
}
```

## OUTPUT:

## OUTPUT:
<img width="455" height="221" alt="Screenshot 2026-10-26 213737" src="https://github.com/user-attachments/assets/88753f1f-b3eb-40e0-871b-e91fcb3b13a8" />
<img width="420" height="237" alt="Screenshot 2026-10-26 213715" src="https://github.com/user-attachments/assets/b8a2aa86-b6c8-4d00-8bf6-0426aa680ce3" />



## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
