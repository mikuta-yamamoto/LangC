# 本日の総合テスト
## 1.基本構造と出力
- C言語で、"Welcome to C Programming!"と出力するプログラムを作成してください。
#include <stdio.h>

int main(void) {
    printf("Welcome to C Programming!\n");
    return 0;
}

---

## 2.C言語で、次の計算を行うプログラムを作成してください。
- 整数xに10を代入し、yにxの2倍を代入する。
- zにxとyの和を代入する。
- 最後に、x、y、zの値をそれぞれ出力する。
#include <stdio.h>

int main(void) {
    int x = 10;
    int y = x * 2;
    int z = x + y;
    
    printf("x: %d, y: %d, z: %d\n", x, y, z);
    return 0;
}

---

## 3.変数と型変換
- 整数型の変数priceに500を代入し、その後、1.1倍した結果を浮動小数点数として出力するC言語プログラムを作成してください。
  
