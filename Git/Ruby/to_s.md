### [半加算器](https://paiza.jp/works/mondai/logical_operation/logical_operation__basic_step8)

```Ruby
A, B = gets.chomp.split.map(&:to_i)
sum = A + B
binary_sum = sum.to_s(2) # 10進数を2進数に変換

# 2進数表現の下から2けた目と1けた目の値を取得
C = binary_sum[-2].to_i
S = binary_sum[-1].to_i

puts "#{C} #{S}"

```

to_s(2)メソッドは、数値を2進数の文字列に変換するためのメソッドです。  
具体的には、数値オブジェクトに対してこのメソッドを呼び出すと、その数値を2進数の文字列に変換して返します。

```Ruby
N = 4
puts N.to_s(2)
# 出力結果 100

```
***
### [10 進数から M 進数に変換](https://paiza.jp/works/mondai/loop_problems2/loop_problems2__conv_nbase)
```Ruby
N,M=gets.chomp.split.map(&:to_i)
puts N.to_s(M)
```
