### [1 つの入力](https://paiza.jp/works/mondai/d_rank_level_up_problems/d_rank_level_up_problems__stdin_3)
半角スペースを含まない文字列が 1 行で与えられるので、そのまま出力
```Java
// 入力された値をclass内部で使用
import java.util.*;
public class Main {
    public static void main(String[] args) {
      
        // 入力された値を変数scとして定義
        Scanner sc = new Scanner(System.in);
        // 変数scを文字列（String型）変数textとして定義
        String text = sc.next();
        System.out.println(text);

        sc.close();
    }
}
```
***
### [半角スペース区切りの 2 つの入力](https://paiza.jp/works/mondai/d_rank_level_up_problems/d_rank_level_up_problems__stdin_boss)
Scanner クラスの next メソッドは特に指定しない限り、入力を空白文字区切りで受け取る。  
下記の場合、2 回 next メソッドを用いることで、入力されるすべての文字列を受け取る。
```Java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String line = sc.next();
        String text = sc.next();
        System.out.println(line);
        System.out.println(text);

        sc.close();
    }
}
// 入力例
// hello world

// 出力結果
// hello
// world
```
***
### [引き算・掛け算](https://paiza.jp/works/mondai/d_rank_level_up_problems/d_rank_level_up_problems__accompanied_by_stdin_2)
半角スペース区切りで入力された値を変数A・Bとして定義。  
差と積を半角スペース区切りで出力する。
```Java
import java.util.*;

public class Main{
  public static void main(String[]args){
    Scanner sc = new Scanner(System.in);
    int A = sc.nextInt();
    int B = sc.nextInt();

    System.out.println(A-B +" "+ A*B);

    sc.close();
  }
}
```
