## 繰り返し処理
### while
条件がtrueの場合に繰り返す。  
繰り返し処理内でfalseになる処理を入れないと無限ループになってしまう。
```Java
class Main {
  public static void main(String[] args) {
    // 変数の初期化
    int number = 1;
    
    // numberが10より小さい場合に繰り返す、繰り返し処理
    while(number<10){
      System.out.println(number);
      // 変数の更新
      number++;
    }
  }
}

// 出力結果
// 1
// 2
// 3
// 4
// 5
// 6
// 7
// 8
// 9      
```
***
### for
for(カウンタ変数の初期化; 繰り返す条件; ループごとの変数の更新){  
  繰り返し実行される処理;  
}

```Java
class Main {
  public static void main(String[] args) {
    for(int i=1; i<=5; i++){
      System.out.println(i+"回目のループ");
    }
  }
}

// 出力結果
// 1回目のループ
// 2回目のループ
// 3回目のループ
// 4回目のループ
// 5回目のループ
```
***
### break / continue
繰り返し処理内で、条件分岐( if )と併用することが多い。  
条件に一致した場合、下記の動きをする。
* break  
繰り返し処理を強制終了させる。  

* continue  
繰り返し処理をスキップする。

```Java
// break

class Main{
  public static void main(String[]args){
    
    // numが５以下の条件で繰り返す処理
    for(int num=1; num<=5; num++){
      
      // numが3である条件で強制終了
      if(num==3){
        break;
      }
      System.out.println(num);
    }
  }
}

// 出力結果
// 1
// 2
```
```Java
// continue

class Main{
  public static void main(String[]args){
    
    // numが５以下の条件で繰り返す処理
    for(int num=1; num<=5; num++){

      // numが3である条件でスキップ
      if(num==3){
        continue;
      }
      System.out.println(num);
    }
  }
}

// 出力結果
// 1
// 2
// 4
// 5
```
