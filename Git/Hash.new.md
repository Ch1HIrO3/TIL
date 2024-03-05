Hash.new(0) は新しいハッシュを生成し、デフォルト値として 0 を指定します。

```Ruby
counts = Hash.new(0)

puts counts['a'] # 出力: 0
puts counts['b'] # 出力: 0

counts['a'] += 1
puts counts['a'] # 出力: 1

```

