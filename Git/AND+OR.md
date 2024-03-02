[AND+OR](https://paiza.jp/works/mondai/conditions_branch/conditions_branch__bool_boss)

```Ruby
# 3 つの整数X, Y, Zが与えられます。
X,Y,Z=gets.chomp.split(" ").map(&:to_i)

# 「Xが 10 以上」かつ「Yが 10 以上」の場合はYES
# 「Zが 10 以上の」場合はXとYの値にかかわらず必ずYESを出力
if Z>=10
  puts "YES"
elsif X>=10 && Y>=10
  puts "YES"
# そうではない場合はNOを出力してください。
else
  puts "NO"
end
```

## 三項演算子を使用する
条件式 ? 真の場合の値 : 偽の場合の値

```Ruby
# 3 つの整数X, Y, Zが与えられます。
X, Y, Z = gets.chomp.split.map(&:to_i)

# Zが 10 以上の場合はXとYの値にかかわらず必ずYESを出力
# それ以外の場合はXとYの両方が10以上の場合にYESを出力
# それ以外の場合はNOを出力してください。
puts Z >= 10 || (X >= 10 && Y >= 10) ? 'YES' : 'NO'

```
