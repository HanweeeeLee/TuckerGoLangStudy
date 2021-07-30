# 05 fmt 패키지를 이용한 텍스트 입출력

## printf println print
다른 언어와 똑같음..

## 특수 문자
```GoLang
package main

import "fmt"

func main() {
	str := "Hello\tGo\t\tWorld\n"Go\"is Awesome!\n"

	fmt.print(str)
	fmt.printf("%s", str)
	fmt.printf("%q", str) // 키워드들이 먹히지 않고 plan text로 나온다. -> "Hello\tGo\t\tWorld\n"Go\"is Awesome!\n"
}

```

