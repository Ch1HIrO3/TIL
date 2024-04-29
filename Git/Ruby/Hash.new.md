Hash.new(0) は新しいハッシュを生成し、デフォルト値として 0 を指定。

```Ruby
counts = Hash.new(0)
puts counts # 出力: {}

puts counts['a'] # 出力: 0
puts counts # 出力: {}

counts['a'] += 1
puts counts # 出力: {"a"=>1}
puts counts['a'] # 出力: 1
```

