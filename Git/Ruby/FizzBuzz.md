### [FizzBuzz (paizaランク C 相当)](https://paiza.jp/works/mondai/conditions_branch/conditions_branch__mod_boss)

整数Nが与えられます。   
Nが 3 で割り切れる場合はFizz  
Nが 5 で割り切れる場合はBuzz  
 Nが 3 と 5 の両方で割り切れる場合はFizzやBuzzの代わりにFizzBuzzを出力してください。  
 ただし、Nが 3 の倍数でも 5 の倍数でもないときはNをそのまま出力してください。

 ```Ruby
 N=gets.to_i
Fizz = N%3==0
Buzz = N%5==0

if Fizz&&Buzz
  puts "FizzBuzz"
elsif Fizz
  puts "Fizz"
elsif Buzz
  puts "Buzz"
else
  puts N
end
 ```

## AIリファクタリング
 ```Ruby
 N = gets.to_i

if (N % 3).zero? && (N % 5).zero?
  puts "FizzBuzz"
elsif (N % 3).zero?
  puts "Fizz"
elsif (N % 5).zero?
  puts "Buzz"
else
  puts N
end
 ```

 * 変数を定義し過ぎない
 * .zero?メソッドの使用
