## 安装  
~~~
以下类库都在\\think\\helper命名空间下
composer require ibibicloud/think-helper
~~~

## Str 字符串操作

```
// 检查字符串中是否包含某些字符串
Str::contains('我是中国人', '我是');			// true
Str::contains('我是中国人', ['我', '啊'])	;	// true

// 检查字符串是否以某些字符串结尾
Str::endsWith('我是中国人', '中国人')	;		// true
Str::endsWith('我是中国人', ['国', '人'])	;	// true

// 检查字符串是否以某些字符串开头
Str::endsWith('我是中国人', '我是');			// true
Str::endsWith('我是中国人', ['我', '是'])	;	// true

// 获取指定长度的随机字母数字组合的字符串
Str::random(8);			// 'xjBIKyRH'

// 字符串转小写
Str::lower('Abcd');		// 'abcd'

// 字符串转大写
Str::upper('abcd');		// 'ABCD'

// 获取字符串的长度
Str::length('abcd');	// 4

// 截取字符串
Str::substr($string, $start, $length = null);
Str::substr('abcdefg', 2, 3);	// 'cde'

// 驼峰转下划线
Str::snake($value, $delimiter = '_');
Str::snake('AbcDef');			// 'abc_def'

// 下划线(_/-)转驼峰(首字母小写)
Str::camel('abc_def');			// 'abcDef'

// 下划线(_/-)转驼峰(首字母大写)
Str::camel('abc_def');			// 'AbcDef'

// 转为首字母大写的标题格式
Str::title('abc_def');			// 'Abc_Def'
Str::title('abc-def');			// 'Abc-Def'
```