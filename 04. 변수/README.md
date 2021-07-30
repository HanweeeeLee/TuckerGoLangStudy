# 04. 변수

## 변수 선언

Example)
```GoLang
package main

import "fmt"

func main() {
	var a int = 10 // a변수 선언
	var msg string = "Hello Variable" // msg 변수 선언

	a = 20 // a값 변경
	msg = "Good Morning" // msg값 변경
	fmt.Println(msg, a) // 출력
}
```

```GoLang
package main

import "fmt"

func main() {
	var minimumWage int = 10
	var workingHour int = 10

	var income int = minimumWage * workingHour

	fmt.Println(minimumWage, workingHour, income)
}

```

## 변수 선언의 다른 형태

example)
```GoLang
package main

import "fmt"

func main() {
	var a int = 3 // 기본형태
	var b int // 초기값 생략. 초기값은 타입별 기본값으로 대체
	var c = 4 // 타입 생략. 변수 타입은 우변 값의 타입이 됨
	d := 5 // 선언 대입문 :=를 사용해서 var 키워드와 타입 생략

	fmtPrintln(a, b, c, d) // 3 0 4 5
}
```
> 타입별 기본값 -> 정수타입: 0 / 실수타입: 0.0 / 불리언: false / 문자열: "" / 그 외: nil









