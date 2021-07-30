# 03. Hello Go World
## 3.4 Hello Go World 코드 뜯어보기
```GoLang
package main // 어떤 패키지에 속하는지 main 패키지는 프로그램 시작점을 포함한다.

import "fmt" // fmt 패키지 import

func main() { // 함수 시작점
	// Hello Go World 출력
	fmt.Println("Hello Go World")
}
```

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

# 열거형
```GoLang
type ColorType int
const (
	Red ColorType = iota
	Blue
	Green
	Yellow
)

// 각 ColorType 열거값에 따른 문자열을 반환하는 함수
func colorToString(color ColorType) string {
	switch color {
	case Red:
		return "Red"
	case Blue:
		return "Blue"
	case Green:
		return "Green"
	case Yellow:
		return "Yellow"
	default:
		return "Undefined"
	}
}
```

# 상수
```GoLang
const Pig int = 0

```

# 배열
var 변수명 [요소 개수]타입
```GoLang
package main

import "fmt"

func main() {
	var t [5]float64 = [5]float64{24.0, 25.9, 27.8, 26.9, 26.2} 

	for i := 0; i < 5; i++ {
		fmt.Print(t[i] ) // 24.0 25.9 27.8 26.9 26.2
	}
}

var temps [5]float64 = [5]float64{24.3, 26.7} // 초기화 시키지 않은 나머지 3개는 0으로 초기화가 된다.

x := [...]int{10, 20, 30} // ...로 갯수를 생략할 수 있다.
```

## 다중배열
```GoLang
var b = [2][5]int{
	{ 1, 2, 3, 4, 5 },
	{ 6, 7, 8, 9, 10 }, // 여러줄로 초기화할때 맨 뒤에 , 붙어야만 하는거 일수도 있는듯
}
```


# 구조체
```GoLang
package main

import "fmt"

type House struct {
	Address string
	Size int
	Price float64
	Type string
}

func main() {
	var house House
	house.Address = "서울시 강동구 ..."
	house.Size = 28
	house.Price = 9.8
	house.Type = "아파트"

	fmt.Println("주소: ", house.Address) 
	fmt.Println("크기: %d 평\n:", house.Size) 
	fmt.Println("가격: %.f억 원\n", house.Price) 
	fmt.Println("타입: ", house.Type) 
}
```










