# rust.json

[rust.json](./rust.json) のドキュメント。AtCoder での使用を想定。

> [!NOTE]
> `$0` はスニペット展開後のカーソル位置を示します。

## テンプレート系

### `single`

テンプレート。

```rs
use proconio::input;

fn main() {
    input! {
        $0
    }
}
```

### `multi`

マルチテストケース用テンプレート。

```rs
use proconio::input;

fn main() {
    input!(t: usize);
    (0..t).for_each(|_| solve());
}

fn solve() {
    input! {
        $0
    }
}
```

## 出力系

### `pl`

標準出力。

```rs
println!("{}", $0);
```

使用例：

```rs
let ans = 42;
println!("{}", ans);
```

### `epl`

標準エラー出力。

```rs
eprintln!("{:?}", $0);
```

使用例：

```rs
let v = vec![1, 2, 3];
eprintln!("{:?}", v);
```

### `pyes`

`Yes` を出力する。

```rs
println!("Yes");
```

### `pno`

`No` を出力する。

```rs
println!("No");
```

### `p-1`

`-1` を出力する。

```rs
println!("-1");
```

## その他

### `d4`

4 方位探索用の配列。

```rs
[(1, 0), (0, 1), (!0, 0), (0, !0)]
```

使用例：

```rs
for (dx, dy) in [(1, 0), (0, 1), (!0, 0), (0, !0)] {
    let (nx, ny) = (x + dx, y + dy);
    if nx < h && ny < w {
        // 範囲内の場合の処理
    }
}
```

### `d8`

8 方位探索用の配列。

```rs
[(1, 0), (1, 1), (0, 1), (!0, 1), (!0, 0), (!0, !0), (0, !0), (1, !0)]
```

使用例：

```rs
for (dx, dy) in [(1, 0), (1, 1), (0, 1), (!0, 1), (!0, 0), (!0, !0), (0, !0), (1, !0)] {
    let (nx, ny) = (x + dx, y + dy);
    if nx < h && ny < w {
        // 範囲内の場合の処理
    }
}
```
