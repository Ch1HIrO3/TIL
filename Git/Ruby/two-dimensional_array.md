## 二重配列
### [要素数の出力](https://paiza.jp/works/mondai/array_primer/array_primer__2dmatrix_output_step1)

```Ruby
array = [
  [1, 2, 3, 4, 5, 6],
  [8, 1, 3, 3, 1, 8]
]

# 二次元配列の要素数を計算する
elements_count = array.flatten.size

puts elements_count
```
### [全要素の出力](https://paiza.jp/works/mondai/array_primer/array_primer__2dmatrix_output_step2)

```Ruby
array = [
  [6, 5, 4, 3, 2, 1],
  [3, 1, 8, 8, 1, 3]
]

array.each do |row|
  puts row.join(' ')
end
```

### [列数の出力](https://paiza.jp/works/mondai/array_primer/array_primer__2dmatrix_output_step4)
```Ruby
array = [
  [1, 2, 3, 4],
  [6, 5, 4, 3],
  [3, 1, 8, 1]
]

puts array.first.size
# first メソッドを使用して最初の行を取得し
# その行の要素数を size メソッドで取得
```
### [各行の要素数の出力](https://paiza.jp/works/mondai/array_primer/array_primer__2dmatrix_output_step5)

```Ruby
array=[
  [1],
[2,3],
[4,5,6]
]

array.each do|low|
  puts low.size
end
# 出力結果
# 1
# 2
# 3
```

### [各行の要素数の出力](https://paiza.jp/works/mondai/array_primer/array_primer__2dmatrix_output_step6)
```Ruby
array = [
  [1, 2, 3],
  [8, 1, 3],
  [10, 100, 1]
]

# 配列の 2 行目 3 列目の要素を出力
puts array[1][2]

# 出力結果 3
```

### [二次元配列の入力](https://paiza.jp/works/mondai/array_primer/array_primer__2dmatrix_input_step1)
```Ruby
array = [
  [1, 3, 5, 7],
  [8, 1, 3, 8]
]

# 全要素を各行ずつ半角スペース区切りで出力し、各行の終わりで改行
array.each do|low|
  puts low.join(" ")
end

# 出力結果
# 1 3 5 7
# 8 1 3 8
```
### [二次元配列の入力 2](https://paiza.jp/works/mondai/array_primer/array_primer__2dmatrix_input_step2)
```Ruby
num=gets.to_i
array=[]

5.times do
  # 取得した数列を配列に入れる
  array<<gets.chomp.split.map(&:to_i)
end

array.each do|low|
  puts low.join(" ")
end
```
### [i番目の出力 1](https://paiza.jp/works/mondai/array_primer/array_primer__2dmatrix_i-thoutput_step1)
```Ruby
K,L=gets.chomp.split.map(&:to_i)
array=[
  [1,2,3,4],
  [10,100,0,5],
  [8,1,3,8],
  [15,34,94,25]
]

# 配列の K 行目 L 列目の要素を出力
puts array[K-1][L-1]
```
### [配列に含まれている? 1](https://paiza.jp/works/mondai/array_primer/array_primer__search_include_step1)
```Ruby
sequence = "10 13 21 1 6 51 10 8 15 6"
sequence = sequence.split.map(&:to_i)

# 数列に6が含まれているか否か条件分岐
if sequence.include?(6)
  puts "Yes"
else
  puts "No"
end
```
### [何番目にある? 1 ](https://paiza.jp/works/mondai/array_primer/array_primer__search_i-th_step1)
```Ruby
sequence=[1,10,2,9,3,8,4,7,5,6]

# 数列の何番目に"8"があるか出力
puts sequence.index(8)+1

# 出力結果 6
```
### [何個ある? 1 ](https://paiza.jp/works/mondai/array_primer/array_primer__search_count_step1)
```Ruby
sequence = [1, 2, 2, 1, 2, 1, 2, 1, 1, 1]

# 数列にいくつ"1"が含まれているか数えて出力
puts sequence.count(1)

# 出力結果 6
```
```Ruby
# countメソッドは文字列でも同様に使用できる。
array=["red","blue","green","green","red","red"]
puts array.count("red")

# 出力結果 3
```
