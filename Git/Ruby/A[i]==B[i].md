### [同値判定](https://paiza.jp/works/mondai/conditions_branch/conditions_branch__complex_step3)
整数N, 2 つの数列A, B が与えられます。  
 1 ≦ i ≦ N を満たす整数 i のうち、A_i と B_i が等しくなるような i の個数を求めてください。
```Ruby
N = gets.to_i
A = gets.chomp.split(" ").map(&:to_i)
B = gets.chomp.split(" ").map(&:to_i)
count = 0

# 2 つの数列の対応する要素を比較し、等しい場合に count を増やす
N.times do |i|
  count += 1 if A[i] == B[i]
end

puts count
```  
***  
【誤答】  
配列内部の全ての要素を比較してしまったもの。
```Ruby
N=gets.to_i
A=gets.chomp.split(" ").map(&:to_i).to_a
B=gets.chomp.split(" ").map(&:to_i).to_a
count=0

A.each do|num|
  B.each do|i|
    if num==i
      count+=1
    end
  end
end

puts count
```
