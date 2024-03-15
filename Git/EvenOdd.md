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
