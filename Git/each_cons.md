決められた回数(num)の分だけ、ハッシュ(array)の要素を足し合わせる。
→ each_consメソッドを使用する。

```Ruby
array = [3, 6, 4, 7, 8, 9]
num = 3
sum = []

# arrayの要素を取り出す
array.each_cons(num) do |group|
  # 各グループの合計を計算する
  total = group.sum
  sum << total
end

p sum
# 出力結果　 [13, 17, 19, 24]
```

num個ずつのグループが生成されてブロック変数(group)に代入されている。
要素の連続するグループを簡単に反復処理できる。
