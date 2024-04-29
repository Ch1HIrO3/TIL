## 条件分岐
### if
```Java
// 標準入力の値を取得
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int number = scan.nextInt();

    // 以下、条件分岐
        if(number==100){
            System.out.println("numberは100である");    
        } elseif (number>100){
            System.out.println("numberは100より大きい");
        } else {
            System.out.println("numberは100より小さい");
        }
    }
}
```
***
### case
caseごとに必ず「break」を記述する。  
「default」でどの条件にも当てはまらない場合の処理を記述。（elseに近い）
```Java
class Main {
  public static void main(String[] args) {
    int num = 0;

    // 以下、条件分岐
    switch (num) {
      case 1:
        System.out.println("numは1");
        break;
      case 2:
        System.out.println("numは2");
        break;
      default:
        System.out.println("numは1でも2でもない");
        break;
    }
  }
}
```
