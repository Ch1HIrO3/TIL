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
