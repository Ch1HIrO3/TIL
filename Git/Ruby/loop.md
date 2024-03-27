### [ある数字までの出力 1 ](https://paiza.jp/works/mondai/loop_problems/loop_problems__print_num_step1)

* 1.upto(10)  
1から10までの整数を順番に取り出して、それぞれを変数numに代入しながら繰り返し処理を行う構文
```Ruby
1.upto(10) do|num|
  puts num
end

# 出力結果
# 1
# 2
# 3
# 4
# 5
# 6
# 7
# 8
# 9
# 10
```
***
### [数字の受け取り 1 ](https://paiza.jp/works/mondai/loop_problems/loop_problems__input_num_step1)

* each  
配列の要素を順番に取り出して、それぞれを変数numに代入しながら繰り返し処理を行う構文
```Ruby
array=gets.chomp.split.map(&:to_i)
array.each do|num|
  puts num
end

# 入力例
# 1 2 3 4 5 6 7 8 9 10

# 出力
# 1
# 2
# 3
# 4
# 5
# 6
# 7
# 8
# 9
# 10
```
[a ~ z までを表示 ](https://paiza.jp/works/mondai/loop_problems/loop_problems__print_alpha)
```Ruby
('a'..'z').each do |alphabet|
  puts alphabet
end
```
```Ruby
('あ'..'ん').each do |alphabet|
  puts alphabet
end
```
***
### [ある数をある回数表示 2 ](https://paiza.jp/works/mondai/loop_problems/loop_problems__rep_num_step2)

* times  
指定された回数分、繰り返し処理を行う構文
```Ruby
X,Y=gets.chomp.split.map(&:to_i)
Y.times do
  puts X
end

# 入力例1
# 3 8

# 出力例1
# 3
# 3
# 3
# 3
# 3
# 3
# 3
# 3
```
***
