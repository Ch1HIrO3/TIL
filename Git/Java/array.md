## 配列
データ型[]配列の名前 = {要素,要素,要素…}
```Java
public class Main{
  public static void main(String[]args){
    int[]num={1,2,3};
    System.out.println(num[1]);
    // 出力結果 2

    String[]colour={"red","blue","yellow"};
    System.out.println(colour[0]);
    // 出力結果 red

    // 要素の上書き
    colour[0]="green";
    System.out.println(colour[0]);
    // 出力結果 green
  }
}
```
### 繰り返し処理との併用
* length  
配列.length = 配列内の要素数
```Java
public class Main{
  public static void main(String[]args){

    int[]sequence = {1,4,7,9};

    // 配列の要素の数だけ繰り返す処理
    for(int i=0; i<sequence.length; i++){
      System.out.println(sequence[i]);
    }
  }
}

// 出力結果
// 1
// 4
// 7
// 9
```
* 配列用のfor構文  
for(データ型 変数名:配列名){  
  繰り返す処理  
}
```Java
public class Main{
  public static void main(String[]args){
    String[]array = {"red","blue","yellow"};

    // for(データ型 変数名:配列名)
    for(String colour:array){
      System.out.println(colour);
    }
  }
}

// 出力結果
// red
// blue
// yellow
```
