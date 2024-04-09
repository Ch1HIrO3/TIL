### [ある数字までの出力 1 ](https://paiza.jp/works/mondai/loop_problems/loop_problems__print_num_step1)

## 1.upto(10)  
1から10までの整数を順番に取り出して、それぞれを変数numに代入しながら繰り返し処理を行う構文  
* each処理に繰り返し範囲を指定する方が一般的。
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

## each  
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
## [FizzBuzz](https://paiza.jp/works/mondai/loop_problems/loop_problems__fizzbuzz)
* 範囲演算子 (1..100) を使用して繰り返し範囲を指定
```Ruby
(1..100).each do |i|
  case
  when i % 15 == 0
    puts "FizzBuzz"
  when i % 3 == 0
    puts "Fizz"
  when i % 5 == 0
    puts "Buzz"
  else
    puts i
  end
end
```


***
### [ある数をある回数表示 2 ](https://paiza.jp/works/mondai/loop_problems/loop_problems__rep_num_step2)

## times  
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
```Ruby
# 回数Nが入力される
N = gets.to_i

# N回数、数値が入力される
array = N.times.map { gets.to_i }

# 合計を算出する
puts array.sum

# 入力例
# 5
# 1
# 2
# 3
# 4
# 5

# 出力結果
# 6
```
***
### [九九の表示 1 ](https://paiza.jp/works/mondai/loop_problems/loop_problems__kuku_step1)

## while  
指定された条件が真である間、繰り返し文を実行します。  
while の後に続く条件式が評価され、条件が真であれば、ループの本体が実行されます。  
条件が偽になるまでループが続きます。
```Ruby
array=[]
num=1

while num<=9
  array<<num*8
  num+=1
end

puts array.join(" ")

# 出力結果
# 8 16 24 32 40 48 56 64 72
```
### [けた数の測定2 で何回割れる？](https://paiza.jp/works/mondai/loop_problems2/loop_problems2__div_two)
整数 N が与えられます。  
N が何回 2 で割れるかを求め、出力してください。
```Ruby
num=gets.to_i
count=0

while num%2==0
  count+=1
  num/=2
end

puts count
```
***

### [N が M ずつ増えたときにいつ K を越える？](https://paiza.jp/works/mondai/loop_problems2/loop_problems2__inc_m)
```Ruby
N,M,K=gets.chomp.split.map(&:to_i)
# N が M ずつ増えるとき、何回目に K を越えるか出力してください。

count=0
while N<=K
  N+=M
  count+=1
end
puts count
```
