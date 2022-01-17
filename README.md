# Домашнее задание к занятию "7.5. Основы golang"



## Задача 1. Установите golang.
Установлено

## Задача 2. Знакомство с gotour.
Ознакомился

## Задача 3. Написание кода. 
Цель этого задания закрепить знания о базовом синтаксисе языка. Можно использовать редактор кода 
на своем компьютере, либо использовать песочницу: [https://play.golang.org/](https://play.golang.org/).

1. Напишите программу для перевода метров в футы (1 фут = 0.3048 метр). Можно запросить исходные данные 
у пользователя, а можно статически задать в коде.
    Для взаимодействия с пользователем можно использовать функцию `Scanf`:
    ```
    package main
        
        import "fmt"
        
        import "math"
        
        func main() {
            fmt.Print("Enter value in foot: ")
            var input float64
            
            fmt.Scanf("%f", &input)               // округлим до 2-х знаков в строке
            output := input * float64(0.3048)     // точное значение 
            rOutput := math.Round(output)         // округлим до целого
            sOutput := fmt.Sprintf("( %.2f)", output)
            fmt.Println("Value in Meters:", rOutput, sOutput )    
        }  
    }
    ```
 
1. Напишите программу, которая найдет наименьший элемент в любом заданном списке, например:
    ```
    x := []int{48,96,86,68,57,82,63,70,37,34,83,27,19,97,9,17,}
        package main
        
        import "fmt"
        
        func main() {
            x := []int{48,2, 96,86,3,68,57,82,63,70,37,34,83,27,19,97,9,17,1}
            current := 0
            fmt.Println ("Список значений : ", x)
            for i, value := range x {
                if (i == 0) {
                   current = value 
                } else {
                    if (value < current){
                        current = value
                    }
                }
            }
            fmt.Println("Минимальное число : ", current)
        }    
    ```
1. Напишите программу, которая выводит числа от 1 до 100, которые делятся на 3. То есть `(3, 6, 9, …)`.
```
package main
        
        import "fmt"
        
        func main() {
            
            for i := 1; i <= 100; i++ {
                if ((i-1)%10) ==0 {
                        fmt.Print(i-1," -> ")
                }            
                        
                if (i%3) == 0 {
                    fmt.Print(i,", ")
                    }
                if (i%10) ==0 {
                    fmt.Println()
                }
            }
        }
```


