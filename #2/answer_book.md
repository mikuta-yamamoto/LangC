# 解答

## 1章
### 1-1 何もしないプログラム
#### 必須課題
```
①何も行わないmain関数だけのプログラムを書いてみよう
※ここで作成したmain関数はこの後も使うので削除しないでください
```

```c
 int main(void) {return 0;}
```
### 解答

### 1-2 コンパイラは翻訳ソフト
```
①先ほど作成したmain関数をコンパイルしてみよう
```
### 解答
- main関数を作成したディレクトリに移動しターミナル or コマンドプロンプトで以下C言語のソースをコンパイルするコマンドを実行
```
gcc ファイル名.c
```

## 2章
### 2-1 書き方のルール
#### 必須課題
```
①先ほど作成したmain関数の記述方法をトークンごとに分割しよう
②トークンに分割したらコンパイルできるか試してみう
③トークンどうしを分割せずmain関数を作成してみよう
④トークンを分割せず作成した関数をコンパイルしどんな結果になるか確認しよう
```
### 解答
### ①先ほど作成したmain関数の記述方法をトークンごとに分割しよう
```c
int
main
(
void
)
{
return
0
;
}
```
### ②トークンに分割したらコンパイルできるか試してみう
```
gcc main.c
```
### ③トークンどうしを分割せずmain関数を作成してみよう
```c
intmain(void) {return 0;}
```
### ④トークンを分割せず作成した関数をコンパイルしどんな結果になるか確認しよう
**以下のようなエラーが表示される
```c
gcc ファイル名.c

intmain(void) {return 0;}
^
1 warning generated.
Undefined symbols for architecture arm64:
  "_main", referenced from:
     implicit entry/start for main executable
ld: symbol(s) not found for architecture arm64
clang: error: linker command failed with exit code 1 (use -v to see invocation)
```
### 2-2 書き方の慣習
#### 必須課題
```
①main関数にインデントや改行を加えて読みやすいソースにリファクタリングしよう
②リファクタリングしたmain関数をコンパイルしてみよう
③main関数にコメントアウトを入れてみよう
```
### 解答
### ①main関数にインデントや改行を加えて読みやすいソースにリファクタリングしよう
```c
int main(void)
{
     return 0;
}
```
### ②リファクタリングしたmain関数をコンパイルしてみよう
```
gcc ファイル名.c
```
### ③main関数にコメントアウトを入れてみよう
```c
// main関数: プログラムのエントリーポイント
int main(void) 
{
    // プログラムが正常に終了したことを示すために0を返す
    return 0;
}
```

## 3章
### 3-1 文字列の表示
#### 必須課題
```
①main関数にprintf関数を定義し引数にHelloWorldを指定しよう
②main関数をコンパイルしよう
③main関数を実行し画面にHelloWorldを表示させよう
④HelloWorld以外の文字列を入力し画面に表示させよう
```
### 解答
### ①main関数にprintf関数を定義し引数にHelloWorldを指定しよう
```c
#include <stdio.h>

int main(void)
{
    printf("HelloWorld");
    return 0;
}
```
### ②main関数をコンパイルしよう
```
gcc ファイル名.c
コンパイルを実行すると、a.outというファイルが生成されます
```
> a.out は、C言語などのプログラミング言語で書かれたソースコードをコンパイルした後に生成される実行可能ファイルのデフォルト名です。特に、Unix系のオペレーティングシステム（LinuxやmacOSなど）で使用されるGNU Compiler Collection（GCC）などのコンパイラが、デフォルトでこの名前を使用します。

### ③main関数を実行し画面にHelloWorldを表示させよう
```
カレントディレクトリによって実行コマンドは変わります。
例 ./a.out
```
### ④HelloWorld以外の文字列を入力し画面に表示させよう
```
任意の文字列を出力してください
```
### 3-2 改行文字
#### 必須課題
```
①エスケープシーケンスを用いて実行結果のように画面に表示させよう
実行結果
I'm from 
Fukuoka prefecture


②エスケープシーケンスを用いて実行結果のように画面に表示させよう
実行結果
1
2
3
4
5
6
7
8
9
10

③実行結果のように文字が頭揃えで表示されるプログラムを作成しよう
実行結果
I'm from Fukuoka prefecture
I'm from Tokyo   prefecture
```
### 解答
### ①エスケープシーケンスを用いて実行結果のように画面に表示させよう
```c
#include <stdio.h>

int main(void)
{
    printf("I'm from \n");
    printf("Fukuoka prefecture\n");
    return 0;
}
```
### ②エスケープシーケンスを用いて実行結果のように画面に表示させよう
```c
#include <stdio.h>

int main(void)
{
    printf("1\n");
    printf("2\n");
    printf("3\n");
    printf("4\n");
    printf("5\n");
    printf("6\n");
    printf("7\n");
    printf("8\n");
    printf("9\n");
    printf("10\n");

    return 0;
}
```
### ③実行結果のように文字が頭揃えで表示されるプログラムを作成しよう
```c
#include <stdio.h>

int main(void)
{
    printf("I'm from\tFukuoka prefecture\n");
    printf("I'm from\tTokyo tprefecture\n");
    return 0;
}
```
## 4章
### 4-1 数値の表示
#### 必須課題
```
①%dを用いて数値の1000を文字列に変化し表示させるプログラムを作成してみよう
実行結果
1000

②%dを用いて数値の1000、2000、3000を文字列に変換し1000+2000=3000と表示させよう
実行結果
1000+2000=3000
```
### 解答
### ①%dを用いて数値の1000を文字列に変化し表示させるプログラムを作成してみよう
```c
#include <stdio.h>

int main(void)
{
    printf("%d", 1000);
    return 0;
}
```
### ②%dを用いて数値の1000、2000、3000を文字列に変換し1000+2000=3000と表示させよう
```c
#include <stdio.h>

int main(void)
{
    printf("%d+", 1000);
    printf("%d=", 2000);
    printf("%d\n", 3000);
    return 0;
}
```

### 4-2 基本的な計算
#### 必須課題
```
①1000+2000を行うプログラムを作成しましょう
②上記プログラム実行結果を画面に表示させましょう
実行結果
3000
```
### 解答
### ①1000+2000を行うプログラムを作成しましょう
```c
int main(void)
{
    1000 + 2000;
}
```
### ②上記プログラム実行結果を画面に表示させましょう
```c
#include <stdio.h>

int main(void)
{
    printf("%d\n", 1000 + 2000);
    return 0;
}
```
### 4-3数値の種類
#### 必須課題
```
実数値でそれぞれの計算を行うプログラムを作成し表示させましょう
※演算子(+,-,×,÷)はC言語で用いられる記法に換えて計算を行ってください
①20.0+4.0
②10.0-5.0
③3.0×7.0
④6.0÷3.0
実行結果
```
### 解答
### ①20.0+4.0
```c
#include <stdio.h>

int main(void)
{
    printf("%f\n", 20.0 + 4.0);
    return 0;
}
24.000000
```

### ②10.0-5.0
```c
#include <stdio.h>

int main(void)
{
    printf("%f\n", 10.0 - 5.0);
    return 0;
}
5.000000
```
### ③3.0×7.0
```c
#include <stdio.h>

int main(void)
{
    printf("%f\n", 3.0 * 7.0);
    return 0;
}
21.000000
```
### ④6.0÷3.0
```c
#include <stdio.h>

int main(void)
{
    printf("%f\n", 6.0 / 3.0);
    return 0;
}
2.000000
```
## 5章
### 5-1 数値を記憶する
#### 必須課題
```
①main関数の中に、int型でprice変数を作成しましょう
②作成した関数をコンパイルして、コンパイル結果を確認してみましょう
③変数priceに数値の100を代入しましょう
④コンパイルし結果を表示させましょう
実行結果
100

⑤price変数に数値の50を加算する処理をプログラムに記述しコンパイル、表示まで行いましょう
実行結果
150

⑥インクリメントを用いて変数price(100が代入されている状態)を101に加算する処理をプログラムに記述し、コンパイル、表示まで行いましょう
実行結果
101
```
### 解答
### ①main関数の中に、int型でprice変数を作成しましょう
```c
#include <stdio.h>

int main(void)
{
    int price; /* 変数宣言の部分 */
    return 0;
}
```
### ②作成した関数をコンパイルして、コンパイル結果を確認してみましょう
```c
gcc ファイル名.c
```
### ③変数priceに数値の100を代入しましょう
```c
#include <stdio.h>

int main(void)
{
    int price; /* 変数宣言の部分 */
    price = 100; /*代入の部分*/
    printf("%d\n", price);
    return 0;
}
```
### ④コンパイルし結果を表示させましょう
```c
gcc ファイ名.c
```
### ⑤price変数に数値の50を加算する処理をプログラムに記述しコンパイル、表示まで行いましょう
```c
#include <stdio.h>

int main(void)
{
    int price; /* 変数宣言の部分 */
    price = 100; /*代入の部分*/
    price = price + 50; /*priceに50を加算*/
    printf("%d\n", price);
    return 0;
}
```
### ⑥インクリメントを用いて変数price(100が代入されている状態)を101に加算する処理をプログラムに記述し、コンパイル、表示まで行いましょう
```c
```
### 5-2 変数の種類
#### 必須課題
```
①double型(実数)で変数priceに10を代入しコンパイル、出力まで行いましょう
```
### 解答
### ①double型(実数)で変数priceに10を代入しコンパイル、出力まで行いましょう
```c
#include <stdio.h>

int main(void)
{
    double price = 10;
    printf("%f\n", price);

    return 0;
}
10.000000
```

### 5-3 型の変換
#### 必須課題
```
①整数30と実数1.05の掛け算を行うプログラムを作成し、コンパイル、表示まで行いましょう
②上記表示結果を整数表記にキャストし表示しましょう
```
### 解答
### ①整数30と実数1.05の掛け算を行うプログラムを作成し、コンパイル、表示まで行いましょう
```c
#include <stdio.h>

int main(void)
{
    printf("%f\n", 30 * 1.05);
    return 0;
}
31.500000
```
### ②上記表示結果を整数表記にキャストし表示しましょう
```c
#include <stdio.h>

int main(void)
{
    printf("%f\n", (int)30 * 1.05);
    return 0;
}
31
```

### 5-4 数値の桁揃え
#### 必須課題
```
printf関数を用いて数値の桁数を指定したプログラムを作成しそれぞれ、コンパイル、表示まで行いましょう
①int型の変数aに20000、変数bに300、変数cに1をそれぞれ代入し%5dを用いて、表示させましょう
実行結果
Aは、20000です。
Bは、  500です。
Cは、    1です。
```
### 解答
### ①int型の変数aに20000、変数bに300、変数cに1をそれぞれ代入し%5dを用いて、表示させましょう
```c
#include <stdio.h>

int main(void)
{
    int a = 20000, b = 300, c = 1;

    printf("Aは %d です。\n", a);
    printf("Bは %d です。\n", b);
    printf("Cは %d です。\n", c);

    return 0;
}
```

# 本日の総合テスト
## 1.基本構造と出力
- C言語で、"Welcome to C Programming!"と出力するプログラムを作成してください。
### 解答
```c
#include <stdio.h>

int main(void) {
    printf("Welcome to C Programming!\n");
    return 0;
}
```

## 2.C言語で、次の計算を行うプログラムを作成してください。
- 整数xに10を代入し、yにxの2倍を代入する。
- zにxとyの和を代入する。
- 最後に、x、y、zの値をそれぞれ出力する。
### 解答
```c
#include <stdio.h>

int main(void) {
    int x = 10;
    int y = x * 2;
    int z = x + y;
    
    printf("x: %d, y: %d, z: %d\n", x, y, z);
    return 0;
}
```

## 3.変数と型変換
- 整数型の変数priceに500を代入し、その後、1.1倍した結果を浮動小数点数として出力するC言語プログラムを作成してください。
### 解答
```c
#include <stdio.h>

int main(void) {
    int price = 500;
    double result = price * 1.1;
    printf("Price after increase: %.2f\n", result);
    return 0;
}
```