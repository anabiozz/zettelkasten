Links: [[Math]] [[Golang]]

```go
func recursionCountDigits(number int) int {  
 if number < 10 {  
  return 1  
 } else {  
  return 1 + recursionCountDigits(number/10)  
 }  
}  
```