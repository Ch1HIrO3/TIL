### [足したり引いたり](https://paiza.jp/works/mondai/conditions_branch/conditions_branch__complex_step2)
整数Nが与えられます。Nのけた数を出力してください。
```Ruby
N,A,B=gets.chomp.split(" ").map(&:to_i)
if (A+B==N)||(A-B==N)||(-A+B==N)||(-A-B==N)
  puts "YES"
else
  puts "NO"
end
```
