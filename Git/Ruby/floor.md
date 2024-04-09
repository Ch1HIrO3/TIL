### 小数点

#### .floor メソッド
与えられた数値を小数点以下を切り捨てた整数に変換するメソッド。

```Ruby
num=1.23456
puts num.floor
# => 1
```
### [毎日増加するお金](https://paiza.jp/works/mondai/loop_problems2/loop_problems2__inc_percent)
```Ruby
A,B=gets.chomp.split.map(&:to_i)

count=0
while A<=B
  X=(A*0.1).floor
  A+=X
  count+=1
end
puts count
```

***  

%.3f は、小数点以下3桁までの精度を持つ浮動小数点数を表す。  
% 演算子を使って num にこのフォーマットを適用することでnum の値が小数点以下3桁まで表示される。
```Ruby
num=1.23456
puts "%.3f" % num
# => 1.235
```

***
小数点以下も含めて取得する  
```Ruby
num = gets.to_f
```
***
小数点以下を切り上げる  
```Ruby
num = 1.345
puts num.ceil
# 出力結果　2
```
