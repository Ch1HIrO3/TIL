### [偶奇の判定](https://paiza.jp/works/mondai/conditions_branch/conditions_branch__mod_step3)
長さ N の数列Aが与えられます。  
この数列に含まれる偶数の要素の個数と、奇数の要素の個数を答えてください。
```Ruby
N=gets.to_i
array=gets.chomp.split(" ").map(&:to_i).to_a
even=0
odd=0

array.each do|num|
  if num%2==0
    even+=1
  else
    odd+=1
  end
end

puts "#{even} #{odd}"
```

修正
```Ruby
N = gets.to_i
array = gets.chomp.split.map(&:to_i)
even_count = array.count(&:even?)
odd_count = array.count(&:odd?)

puts "#{even_count} #{odd_count}"

```
***
### [偶奇の判定](https://paiza.jp/works/mondai/loop_problems2/loop_problems2__even_odd)
```Ruby
# 数字の個数Nが入力される
N = gets.to_i

# 数字が入力される
numbers = gets.chomp.split.map(&:to_i)

# 数字ごとに偶数か奇数かを出力する
numbers.each do |num|
  puts num.odd? ? "odd" : "even"
end
```
puts num.odd? ? "odd" : "even" は、三項演算子と呼ばれる条件演算子です。
これは、条件式を評価し、その結果に基づいて2つの値のうちの1つを返します。

この式では、num が奇数であるかどうかを判断します。
num.odd? は num が奇数であれば真を返し、偶数であれば偽を返します。
その結果、条件式が真の場合は "odd" が、偽の場合は "even" が返されます。

num.odd? が true であれば、式は "odd" を返します。
num.odd? が false であれば、式は "even" を返します。

```Ruby
# 同義
N=gets.to_i
array=gets.chomp.split.map(&:to_i)

array.each do|num|
  if num.odd?
    puts "odd"
  elsif num.even?
    puts "even"
  end
end
```
