**JavaScript 字符串 方法**  

**1，str.charAt(index)方法从一个字符串中返回指定的字符。**
```
var str = "Brave new world";
str.charAt(0) // B
str.charAt(999) // ''
```
---
**2，str.concat(string2, string3[, ..., stringN])方法将一个或多个字符串与原字符串连接合并，形成一个新的字符串并返回。**
```
强烈建议使用 赋值操作符（+, +=）代替 concat 方法
var hello = "Hello, ";
console.log(hello.concat("Kevin", " have a nice day.")); /* Hello, Kevin have a nice day. */
```
---
**3,String.endsWith()方法用来判断当前字符串是否是以另外一个给定的子字符串“结尾”的，根据判断结果返回 true 或 false**
```
const str1 = 'Cats are the best!';

console.log(str1.endsWith('best', 17));
// output: true

const str2 = 'Is this a question';

console.log(str2.endsWith('?'));
// output: false
```
---
**4,str.includes(searchString, position)方法用于判断一个字符串是否包含在另一个字符串中，根据情况返回 true 或 false。区分大小写**
```
var str = 'To be, or not to be, that is the question.';

console.log(str.includes('To be'));       // true
console.log(str.includes('question'));    // true
console.log(str.includes('nonexistent')); // false
console.log(str.includes('To be', 1));    // false
console.log(str.includes('TO BE'));       // false
```
---
**5,String.indexOf()方法返回调用它的 String 对象中第一次出现的指定值的索引，从 fromIndex 处进行搜索。如果未找到该值，则返回 -1**
```
str.indexOf(searchValue)
str.indexOf(searchValue, fromIndex)
"Blue Whale".indexOf("Blue");     // 返回  0
"Blue Whale".indexOf("Blute");    // 返回 -1
"Blue Whale".indexOf("Whale", 0); // 返回  5
```
---
**6,str.lastIndexOf(searchValue[, fromIndex])方法返回调用String 对象的指定值最后一次出现的索引，在一个字符串中的指定位置 fromIndex处从后向前搜索。如果没找到这个特定值则返回-1**
```
'canal'.lastIndexOf('a');     // returns 3 （没有指明fromIndex则从末尾l处开始反向检索到的第一个a出现在l的后面，即index为3的位置）
'canal'.lastIndexOf('a', 2);  // returns 1（指明fromIndex为2则从n处反向向回检索到其后面就是a，即index为1的位置）
```
---
**7,str.match(regexp)方法检索返回一个字符串匹配正则表达式的结果。**
---
**8,str.padEnd(targetLength [, padString])方法会用一个字符串填充当前字符串（如果需要的话则重复填充），返回填充后达到指定长度的字符串。从当前字符串的末尾（右侧）开始填充。**
```
'abc'.padEnd(10);          // "abc       "
'abc'.padEnd(10, "foo");   // "abcfoofoof"
'abc'.padEnd(6, "123456"); // "abc123"
'abc'.padEnd(1);           // "abc"
```
---
**9,str.padStart(targetLength [, padString])方法用另一个字符串填充当前字符串(重复，如果需要的话)，以便产生的字符串达到给定的长度。填充从当前字符串的开始(左侧)应用的。**
```
'abc'.padStart(10);         // "       abc"
'abc'.padStart(10, "foo");  // "foofoofabc"
'abc'.padStart(6,"123465"); // "123abc"
'abc'.padStart(8, "0");     // "00000abc"
'abc'.padStart(1);          // "abc"
```
---
**10，str.repeat(count);构造并返回一个新字符串，该字符串包含被连接在一起的指定数量的字符串的副本**
```
count介于0和正无穷大之间的整数 : [0, +∞)
"abc".repeat(-1)     // RangeError: repeat count must be positive and less than inifinity
"abc".repeat(0)      // ""
"abc".repeat(1)      // "abc"
"abc".repeat(2)      // "abcabc"
"abc".repeat(3.5)    // "abcabcabc" 参数count将会被自动转换成整数.
"abc".repeat(1/0)    // RangeError: repeat count must be positive and less than inifinit
```
---
**11,str.replace(regexp|substr, newSubStr|function)字符串替换**
```
var str = 'Twas the night before Xmas...';
var newstr = str.replace(/xmas/i, 'Christmas');
console.log(newstr);  // Twas the night before Christmas...
```
---
**12,str.slice(beginIndex[, endIndex])方法提取某个字符串的一部分，并返回一个新的字符串，且不会改动原字符串**
```
var str1 = 'The morning is upon us.', // str1 的长度 length 是 23。
    str2 = str1.slice(1, 8),
    str3 = str1.slice(4, -2),
    str4 = str1.slice(12),
    str5 = str1.slice(30);
console.log(str2); // 输出：he morn
console.log(str3); // 输出：morning is upon u
console.log(str4); // 输出：is upon us.
console.log(str5); // 输出：""
```
---
**13，str.split([separator[, limit]])方法使用指定的分隔符字符串将一个String对象分割成子字符串数组，以一个指定的分割字串来决定每个拆分的位置**
```
var str = 'The quick brown fox jumps over the lazy dog.';

var words = str.split(' ');
console.log(words[3]);
// expected output: "fox"
```
---
**14,str.startsWith(searchString[, position])方法用来判断当前字符串是否以另外一个给定的子字符串开头，并根据判断结果返回 true 或 false**
```
var str = "To be, or not to be, that is the question.";

alert(str.startsWith("To be"));         // true
alert(str.startsWith("not to be"));     // false
alert(str.startsWith("not to be", 10)); // true
```
---
**15，str.substring(indexStart[, indexEnd])方法返回一个字符串在开始索引到结束索引之间的一个子集, 或从开始索引直到字符串的末尾的一个子集**
```
substring 提取从 indexStart 到 indexEnd（不包括）之间的字符
如果任一参数小于 0 或为 NaN，则被当作 0。
```
---
**16，str.toLocaleLowerCase(locale)方法根据任何指定区域语言环境设置的大小写映射，返回调用字符串被转换为小写的格式。**
```
参数 locale 指明要转换成小写格式的特定语言区域

toLocaleUpperCase() 使用本地化（locale-specific）的大小写映射规则将输入的字符串转化成大写形式并返回结果字符串。

toLowerCase() 会将调用该方法的字符串值转为小写形式，并返回

toUpperCase()  方法返回一个将调用字符串转换为大写形式的值。（如果这个值不是字符串则会被变成字符串）
```
---
**17，str.trim() 方法会从一个字符串的两端删除空白字符**
```
trimEnd() 方法从一个字符串的末端移除空白字符

trimStart() 方法从字符串的开头删除空格
```

