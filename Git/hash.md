### ハッシュのキーとバリューを取得する

```Ruby
hash={one:1,two:2,three:3}

puts hash.keys
puts hash.values
```

#### 出力結果
one  
two  
three  
1  
2  
3  
***
### 二重ハッシュの値を取得する

ハッシュdateを定義
```Ruby
data = [
  {x: {y: {z: '1'}}},
  {x: {y: {z: '2'}}},
  {x: {y: {z: '3'}}},
]
```
```Ruby
data.each do |item|
  puts item[:x]
end

# 出力結果
# {:y=>{:z=>"1"}}
# {:y=>{:z=>"2"}}
# {:y=>{:z=>"3"}}
```
```Ruby
data.each do |item|
  puts item[:x][:y][:z]
end

# 出力結果
# {:z=>"1"}
# {:z=>"2"}
# {:z=>"3"}
```
```Ruby
data.each do |item|
  puts item[:x][:y][:z]
end

# 出力結果
# 1
# 2
# 3
```
