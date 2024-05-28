## オブジェクト指向

### クラス
インスタンスを生成するための設計図。  
情報を記述する。  

### インスタンス
オブジェクトと同義。  
クラスをもとに生成される。  
（変数に代入して使用する。）

* Main.java
```Java
class Main{
  public static void main(String[]args){

    // objectクラスのインスタンスを生成
    new object();

    // 生成したインスタンスは変数に代入する。
    // クラス型 変数名 = インスタンスの生成
    Object object = new object();
  }
}
```
* object.java
```Java
class object{
  // インスタンスの情報
}
```
