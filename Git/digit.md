### [けた数の測定](https://paiza.jp/works/mondai/conditions_branch/conditions_branch__complex_step1)
整数Nが与えられます。Nのけた数を出力してください。
```Ruby
N=gets.chomp.to_s
puts N.length
```
入力された数値を文字列として受け取り、文字数を出力。
***


### [各桁の和](https://paiza.jp/works/mondai/loop_problems2/loop_problems2__digit_sum)
整数 N の各桁の和を計算し、出力する
```Ruby
N=gets.to_i
puts N.digits.sum
# 入力例1
# 12345

# 出力例1
# 15
```
一の位から順番に出力する。
```Ruby
N=gets.to_i
puts N.digits
# 入力例1
# 12345

# 出力例1
# 5
# 4
# 3
# 2
# 1
```
