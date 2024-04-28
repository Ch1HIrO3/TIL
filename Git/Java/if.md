## 条件分岐
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
