## 学习笔记

### 异步编程
回调函数 callback,Promise,async await

### let局部变量
代码块用`{}`包起来，同名变量可以重复使用
```
    {
        let win = true;
        for (let j = 0; j < 3; j++) {
            if (pattern[j][j] != color) {
                win = false;
                break;
            }

        }
        if (win) {
            return true;
        }
    }
    {
        let win = true;
        for (let j = 0; j < 3; j++) {
            if (pattern[j][2 - j] != color) {
                win = false;
                break;
            }

        }
        if (win) {
            return true;
        }
    }
```

### 数组复制
一维数组：Object.create(一维数组)
二维数组：JSON.parse(JSON.stringify(二维数组)