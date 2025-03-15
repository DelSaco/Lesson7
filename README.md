# Lesson7
for.foreach.while

namespace Lesson4
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.OutputEncoding = System.Text.Encoding.UTF8;

            
            List<int> numbers = new List<int>(); // Создаем пустой список
            int count = 15; // Количество элементов в списке

            Console.WriteLine("Введите 15 целых чисел:");

            // Цикл для ввода 15 чисел
            for (int i = 0; i < count; i++)
            {
                int number;

                while (true) // Бесконечный цикл для проверки ввода
                {
                    Console.Write($"Введите число {i + 1}: ");

                    // Проверяем, является ли введенная строка целым числом
                    if (int.TryParse(Console.ReadLine(), out number))
                    {
                        // Если введено число, добавляем в список
                        numbers.Add(number);
                        break; // Выход из цикла, если ввод корректный
                    }
                    else
                    {
                        // Если ввод некорректен, выводим сообщение об ошибке
                        Console.WriteLine("Ошибка! Введите корректное целое число.");
                    }
                }
            }

            // Выводим все элементы списка на консоль
            Console.WriteLine("\nВведенные числа:");
            foreach (int num in numbers)
            {
                Console.WriteLine(num);
            }

            Console.ReadLine();
        }

    }
}
