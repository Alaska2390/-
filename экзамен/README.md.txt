#Ступакова Вероника
##Вариант:18
###Задание: Безопасное деление. Запросить два числа. Если второе число — ноль, обработать исключение DivideByZeroException и вывести сообщение «На ноль делить нельзя!», вместо падения программы.


```csharp
using System;

namespace SafeDivision
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("=== Безопасное деление ===");

            try
            {
                // Запрашиваем первое число
                Console.Write("Введите первое число: ");
                double firstNumber = Convert.ToDouble(Console.ReadLine());

                // Запрашиваем второе число
                Console.Write("Введите второе число: ");
                double secondNumber = Convert.ToDouble(Console.ReadLine());

                // Выполняем деление
                double result = firstNumber / secondNumber;

                // Выводим результат
                Console.WriteLine($"Результат деления: {result}");
            }
            catch (DivideByZeroException)
            {
                Console.WriteLine("На ноль делить нельзя!");
            }
            catch (FormatException)
            {
                Console.WriteLine("Ошибка: нужно ввести число!");
            }

            // Чтобы консоль не закрылась сразу
            Console.WriteLine("\nНажмите любую клавишу для выхода...");
            Console.ReadKey();
        }
    }
}
```
Скриншот:
C:\экзмаен\screen.png