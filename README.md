# MyNumberConvertion

## 自己写的一个进制转换小工具，主要用于十进制和其他进制的转换

### 使用方法，以64进制为例
```

const MyNumberConvertion = require('./my-number-convertion'); //引入转换器
//初始化的字符串，字符串长度就是进制，从左到右，0对应数值0，最后一个字符~对应数值63
const chars64 = '0123456789abcdefghigklmnopqrstuvwxyzABCDEFGHIGKLMNOPQRSTUVWXYZ-~';
//初始化转换器
const convertion64 = new MyNumberConvertion(chars64);
let str64 = '445306828';
let num64 = convertion64.transfer(str64);//将数字转换成64进制
let source64 = convertion64.revert(num64);//将64进制字符还原成原始数据
console.log(`原始数据：${str64}`);
console.log(`转换后：${num64}`)
console.log(`还原后：${source64}`);

```

### 可根据不同的初始化字符串自定义不同的进制
### nodejs环境可运行node demo查看示例
