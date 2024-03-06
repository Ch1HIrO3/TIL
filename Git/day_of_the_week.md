### [曜日の判定](https://paiza.jp/works/mondai/conditions_branch/conditions_branch__mod_step4)
ある月の 1 日は日曜日、 2 日は月曜日...です。X日は何曜日でしょう。
```Ruby
X=gets.to_i
S=["Sun","Mon","Tue","Wed","Thu","Fri","Sat"]
day=X%7

puts S[day-1]
```

修正
```Ruby
X=gets.to_i
S=["Sat","Sun","Mon","Tue","Wed","Thu","Fri"]
day=X%7

puts S[day]
```
