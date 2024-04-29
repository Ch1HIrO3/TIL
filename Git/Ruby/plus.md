### [足したり引いたり](https://paiza.jp/works/mondai/conditions_branch/conditions_branch__complex_step2)
整数N, A, B ( - 99 ≦ N, A, B ≦ 100 ) があります。  
以下の 2 つの操作をそれぞれ 1 回ずつおこなったとき、Nを 0 にできる場合はYESを、できない場合はNOを出力してください。  
1. NにAを足す、またはNからAを引く  
2. NにBを足す、またはNからBを引く
```Ruby
N,A,B=gets.chomp.split(" ").map(&:to_i)
if (A+B==N)||(A-B==N)||(-A+B==N)||(-A-B==N)
  puts "YES"
else
  puts "NO"
end
```
