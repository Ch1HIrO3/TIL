## 二重配列
### [要素数の出力](https://paiza.jp/works/mondai/array_primer/array_primer__2dmatrix_output_step1)

```Ruby
array = [
  [1, 2, 3, 4, 5, 6],
  [8, 1, 3, 3, 1, 8]
]

# 二次元配列の要素数を計算する
elements_count = array.flatten.size

puts elements_count
```
### [全要素の出力](https://paiza.jp/works/mondai/array_primer/array_primer__2dmatrix_output_step2)

```Ruby
array = [
  [6, 5, 4, 3, 2, 1],
  [3, 1, 8, 8, 1, 3]
]

array.each do |row|
  puts row.join(' ')
end
```

### [列数の出力](https://paiza.jp/works/mondai/array_primer/array_primer__2dmatrix_output_step4)
```Ruby
array = [
  [1, 2, 3, 4],
  [6, 5, 4, 3],
  [3, 1, 8, 1]
]

puts array.first.size
# first メソッドを使用して最初の行を取得し
# その行の要素数を size メソッドで取得
```
### [各行の要素数の出力](https://paiza.jp/works/mondai/array_primer/array_primer__2dmatrix_output_step5)

```Ruby
array=[
[1],
[2,3],
[4,5,6]
]

array.each do|low|
  puts low.size
end
# 出力結果
# 1
# 2
# 3
```
