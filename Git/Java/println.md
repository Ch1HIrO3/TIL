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
