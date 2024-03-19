### [終了判定](https://paiza.jp/works/mondai/conditions_branch/conditions_branch__complex_step4)
長さ N の数列Aが与えられます。  
1 つ目の要素から最も左にある奇数の要素の手前までの値の和を求めてください。
```Ruby
N = gets.to_i
A = gets.chomp.split(" ").map(&:to_i)

sum = 0
A.each do |num|
  if num.even?
    sum += num
  else
    break
  end
end

puts sum
```  
***  
【誤答】  
```
警告
warning: already initialized constant S
warning: previous definition of S was here
```
警告が表示される理由は、変数 S が最初に S=0 として定義され、後で再定義されているためです。  
Rubyでは、変数の再定義は警告が発生します。
```Ruby
N=gets.to_i
A=gets.chomp.split(" ").map(&:to_i).to_a
S=0

A.each do|num|
  if num%2==0
    S+=num
  else
    break
  end
end
puts S
```
```Ruby
N=gets.to_i

# to_aは不要
A=gets.chomp.split(" ").map(&:to_i)

# 変数Sの名前を変数sumとしたところ警告文が解消された。
sum=0

A.each do|num|
  if num%2==0 # もしくは if num.even?
    sum+=num
  else
    break
  end
end
puts sum
```
