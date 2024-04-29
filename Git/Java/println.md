### [1 つの文字列を出力](https://paiza.jp/works/mondai/d_rank_level_up_problems/d_rank_level_up_problems__stdout_1)
文字列「paiza」を出力する。
```Java
public class Main {
    public static void main(String[] args) {
        System.out.println("paiza");
    }
}
```
***
### [代入演算](https://paiza.jp/works/mondai/d_rank_level_up_problems/d_rank_level_up_problems__arithmetic_substitution_op_boss)

```Java
public class Main {
    public static void main(String[] args) {
      // 変数 N を 0 で初期化する
      int N = 0;

      // N に 3,286 を足した値を N へ代入する
      N += 3286;
      // N に 4,736 をかけた値を N へ代入する
      N *= 4736;

      // N を 12,312 で割った余りを N へ代入する
      N %= 12312;

      // N を出力する
      System.out.println(N);
    }
}
```
***
### 小数点以下を含めるデータ型
* double
```Java
public class Main {
    public static void main(String[] args) {
      double number = 1.234;
      System.out.println(number);
    }
}
// 出力結果 1.234
```
```Java
class Main {
  public static void main(String[] args) {
    
    // 7を2で割った値を出力してください
    System.out.println(7/2);
    // 出力結果 3
    
    // 7.0を2.0で割った値を出力してください
    System.out.println(7.0/2.0);
    // 出力結果 3.5
    
    // 7を2.0で割った値を出力してください
    System.out.println(7/2.0);
    // 出力結果 3.5
  }
}
```
### データ型のキャスト
```Java
class Main {
  public static void main(String[] args) {
    int number1 = 7;
    int number2 = 2;
    System.out.println(number1 / number2);
    // int型のため、出力結果 3
    
    // number1をdouble型にキャストし、number2で割った値を出力
    System.out.println((double)number1/number2);
    // 出力結果 3.5
  }
}
```
***
### random
* Math.random()  
0~1未満の数値をランダムに生成する。
```Java
// 数の表示とサイコロ
public class Main {
	public static void main(String[] args) {

    // 1~6の数値をランダムに生成する。
    double rand = Math.random() * 6 + 1;
		
    // 生成した数値の小数点以下を切り捨てて、変数numberに定義する。
    // => int型にキャストする。
    int number = (int)rand;
    
    System.out.println("サイコロの目は"+number+"です");
	}
}
```
ランダム数値を生成すると同時にint型へキャストする。  
→ 整数
```Java
// 値段を計算する
public class Main {
	public static void main(String[] args) {
		// 単価 ¥100~¥300
    int price = (int)(Math.random()* 3 + 1 )*100;
        
		//  購入数 1~5個
		int num = (int)(Math.random()* 5 + 1 );
		
		//  合計金額
		int total= price * num;
		
		System.out.println("単価："+ price +"円");
		System.out.println("個数："+ num +"個");
		System.out.println("合計："+ total +"円");
	}
}
```
