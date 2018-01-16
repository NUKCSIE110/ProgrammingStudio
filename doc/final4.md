---
title : 期末考第四題
layout : default
---

``` c++
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
#include<vector>

using namespace std;

int main() {
    char key_info[1000];
    char word;
    int count = 0;
    vector<int> loc;
    FILE *key = fopen("key.gpg", "rb");
    FILE *fin = fopen("final.gpg", "rb");
    FILE *content = fopen("content.txt", "w");
    while (key != NULL) {
		word = fgetc(key);
        if (feof(key) != 0) break;
        printf("%c", word);
        if (word == '@') {
            loc.push_back(count);
        }
        count++;
    }
    
    printf("\n");
    char data[100];
    fgets(data, 100, fin);
    for (int i = 0; i < loc.size(); i++) {
        printf("%c", data[loc.at(i)]);
    }
    fclose(content);

    content = fopen("content.txt", "w");
    for (int i = 0; i < loc.size(); i++) {
        fprintf(content,"%c", data[loc.at(i)]);
    }
    fclose(content);
    fclose(key);
    fclose(fin);
    system("pause");
    return 0;
}
```