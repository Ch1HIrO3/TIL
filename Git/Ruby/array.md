### 配列の要素を出力する

```Ruby
array=["int",1,2,3,]

# 半角スペースで結合して出力
puts array.join(" ")

# 要素ごとに改行して出力
puts array.join("\n")
```

#### 出力結果
```
int 1 2 3
int
1
2
3
```
***
### [動的配列](https://paiza.jp/works/mondai/data_structure/data_structure__array_boss)

```Ruby
# 1 行目に A の要素数 N と、A に対する操作回数 Q が与えられます。
N,Q=gets.chomp.split(" ").map(&:to_i)

# 2 行目に A の 各要素の値が与えられます。
A=gets.chomp.split(" ").map(&:to_i).to_a


Q.times do
  query=gets.chomp
  if query.include?("0")
    # A の末尾に x を追加する
    q,x=query.split(" ").map(&:to_i)
    A<<x
  elsif query=="1"
    # pop_back : A の末尾を削除する
    A.pop
  elsif query=="2"
    # print : A を半角スペース区切りで1行に出力する
    puts A.join(" ")
  end
end
```

```
入力例1
3 5
1 2 3
0 10
0 12
2
1
2

出力例1
1 2 3 10 12
1 2 3 10
```


## AIリファクタリング
 ```Ruby
N, Q = gets.chomp.split.map(&:to_i)
A = gets.chomp.split.map(&:to_i)

Q.times do
  query, *params = gets.chomp.split.map(&:to_i)
  # query は配列の最初の要素に割り当てられ、残りの要素は params にまとめて割り当てられます。このとき、* 演算子が使用されています。*params は「残りの要素をすべてまとめて配列として受け取る」という意味で、これにより可変長引数として params に割り当てられます。

  case query
  when 0
    _, x = params
    # 配列「params」の2番目の要素を「x」に代入
    A << x
  when 1
    A.pop
  when 2
    puts A.join(' ')
  end
end
 ```
* caseによる条件分岐