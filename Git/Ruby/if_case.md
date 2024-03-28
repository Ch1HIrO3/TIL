### [単純な条件分岐](https://paiza.jp/works/mondai/conditions_branch/conditions_branch__simple_step1)
文字列Sが与えられます。
Sがpaizaと一致する場合はYESを、一致しない場合はNOを出力してください。
* 条件が単純な分岐はif文を使用
```Ruby
S=gets.chomp
if S=="paiza"
  puts "YES"
else
  puts "NO"
end
```  


## [FizzBuzz](https://paiza.jp/works/mondai/loop_problems/loop_problems__fizzbuzz)
* 条件が複雑になる場合はcase文を使用
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
