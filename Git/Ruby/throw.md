## [野球の審判（力試し編）](https://paiza.jp/works/mondai/c_rank_skillcheck_archive/umpire_01)

ある打者の番における投球の結果 (ストライクまたはボール) が与えられるので、各投球に対してどのようなコールをすればよいかを出力してください。  

1 球目: ボール → "ball!"  
2 球目: ストライク → "strike!"  
3 球目: ボール → "ball!"  
4 球目: ストライク → "strike!"  
5 球目: ストライク → "out!"  

5 球目では、ボールが 2 つ、ストライクが 3 つたまったのでこの打者はアウトとなります。

1 球目: ボール → "ball!"  
2 球目: ストライク → "strike!"  
3 球目: ボール → "ball!"  
4 球目: ボール → "ball!"  
5 球目: ストライク → "strike!"  
6 球目: ボール → "fourball!"  

6 球目では、ストライクが 2 つ、ボールが 4 つたまったのでこの打者はフォアボールとなります。

```Ruby
num=gets.to_i
array=[]
out=0
fourball=0

num.times do
  throw=gets.chomp
  array<<throw
end

array.each do|call|
  if call =="strike"
    out+=1
    if out==3
      puts "out!"
      break
    end
    puts "strike!"
  elsif call == "ball"
    fourball+=1
    if fourball==4
      puts "fourball!"
      break
    end
    puts "ball!"
  end
end
```
***
AIリファクタリング
```Ruby
num = gets.to_i
throws = []

num.times do
  throws << gets.chomp
end

out_count = 0
fourball_count = 0

throws.each do |throw|
  case throw
  when "strike"
    out_count += 1
    if out_count == 3
      puts "out!"
      break
    else
      puts "strike!"
    end
  when "ball"
    fourball_count += 1
    if fourball_count == 4
      puts "fourball!"
      break
    else
      puts "ball!"
    end
  end
end
```

このリファクタリングされたコードでは、以下の変更が加えられています。

変数や配列の名前をより意味のあるものに変更しました。  
out変数とfourball変数をout_countとfourball_countにリネームしました。  
case-when構文を使用して、if-elsif-else文を置き換えました。これにより、コードがより読みやすくなりました。  
不要な変数やコードを削除し、コードを簡潔にしました。
