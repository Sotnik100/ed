### Строки

```Go
package main

import (
	"fmt"
)
var char uint32 = '\u7777'
var char2 uint64 = '\u3344' //Одинарные ковычки для символов
func main() {
  fmt.Println(string(char) + " " + string(char2))//Иероглефы
  fmt.Println("Hello, world"[0])
  fmt.Println(string("Hello, world"[0]))
  fmt.Println(`Первая строка
Вторая строка
Третья строка`)
}
```
*Результат*
```
睷 ㍄
72
H
Первая строка
Вторая строка
Третья строка
```
### Фибоначчи
```Go
func fibonacci() func() int {
    first, second := 0, 1
    return func() int {
        ret := first
        first, second = second, first+second
        return ret
    }
}
```
