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

***
### [1からNまでの整数を1から順に表示](https://paiza.jp/works/mondai/c_rank_skillcheck_sample/fizz-buzz)
```Ruby
N=gets.to_i

N.times do|num|
  fizz=((num+1)%3==0)
  buzz=((num+1)%5==0)
  if fizz && buzz
    puts "Fizz Buzz"
  elsif fizz
    puts "Fizz"
  elsif buzz
    puts "Buzz"
  else
    puts num+1
  end
end
```

### 【模範解答】
```Ruby
n = gets.to_i

1.upto(n) do |i|
  if (i % 15).zero?
    puts 'Fizz Buzz'
  elsif (i % 3).zero?
    puts 'Fizz'
  elsif (i % 5).zero?
    puts 'Buzz'
  else
    puts i
  end
end
```
3の倍数でありかつ5の倍数でもあるような数は、15の倍数です。  
「1.upto(n) do |i|」は、1からnまでの整数を順番に取り出して、それぞれを変数iに代入しながら繰り返し処理を行う構文です。  

具体的には、1からnまでの範囲を示すメソッドであるuptoメソッドを使用して、1からnまでの数字を順番に取り出しています。  
その後、do〜endブロック内で繰り返し処理が行われます。変数iには現在のループ回数が代入されます。  
この構文を使うことで、1からnまでの範囲に対して繰り返し処理を行うことができます。
