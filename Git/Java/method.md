## メソッド
あくまでmainメソッド内で呼び出したprintDataメソッドが実行されているもの。
```Java
// Mainクラスを定義
public class Main{
  // mainメソッドを定義
  public static void main(String[]args){
    printData(); // printDataメソッドを呼び出し
  }

  // printDataメソッドを定義
  // public static void メソッド名(データ型 変数名)
  public static void printData(){
    System.out.println("これはprintDataメソッド");
  }
}

// 出力結果
// これはprintDataメソッド
```
### 引数
```Java
class Main {
  public static void main(String[] args) {
    // 引数に数値を渡す
    printData(4);
    printData(17);    
  }

  // 引数を受け取り、変数timeに代入
  public static void printData(int time) {
    // 「現在◯◯時です」と出力される処理
    System.out.println("現在"+ time +"時です");
  }
}

// 出力結果
// 現在4時です
// 現在17時です
```
複数の引数を渡す場合は、「,」で区切る。
```Java
public class Main{
  public static void main(String[]args){
    printDate("りんご",3);
    printDate("桃",6);
  }

  public static void printDate(String fruit,int num){
    System.out.println(fruit + "は" + num + "個ある");
  }
}

// 出力結果
// りんごは3個ある
// 桃は6個ある
```
### 戻り値
returnを使用。

下記の場合  
fruitメソッドの戻り値がprintDateの引数として渡されている。  
また、同じ名前「fruit」メソッドが存在するが、引数の数が異なるため定義できる。
```Java
public class Main{
  public static void main(String[]args){
    // printDateメソッドに引数を二つ渡す。
    printDate(fruit("りんご","みかん","もも"),500);
    printDate(fruit("ぶどう","なし"),300);
  }

  // 戻り値はないため、voidでメソッドを作成する。
  public static void printDate(String fruit, int num){
    System.out.println("購入品："+ fruit);
    System.out.println("合計額：¥"+ num);
  }

  public static String fruit(String fruit1, String fruit2, String fruit3){
  // mainメソッドから引数を渡され、戻り値を返す。
    return fruit1 +"・"+ fruit2 +"・"+ fruit3 ;
  }

  public static String fruit(String fruit1, String fruit2){
  // 同名「fruit」メソッドを定義→オーバーロード。
  // mainメソッドから引数を渡され、戻り値を返す。
    return fruit1 +"・"+ fruit2 ;
  }
}

// 出力結果
// 購入品：りんご・みかん・もも
// 合計額：¥500
// 購入品：ぶどう・なし
// 合計額：¥300
```
### boolean型との併用・条件分岐
* boolean型  
真偽値(true/false)を返すデータ型。  
下記の場合、oddメソッド内でnumが2で割り切れない時にtrueを戻り値として返す。
```Java
public class Main{
  public static void main(String[]args){
    int num = 5;
    if(odd(num)){
      System.out.println(num + "は奇数");
    }else{
      System.out.println(num + "は偶数");
    }
  }

  public static boolean odd(int num){
    return num%2 !=0;
  }
}

// 出力結果
// 5は奇数
```
