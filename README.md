#Архитектура компьютера

Три программы реализуют некие алгоритмы на языках программирования тех архитектур, что изначально были заданы:
  - risc-v.txt для архитекутры Risc-V
  - f32a.txt  для стековой архитектуры
  - acc32.txt для аккумуляторной архитекутры

#Risc-V

На данной архитектуре реализован следующий алгоритм

    def capital_case_pstr(s):
    """Convert the first character of each word in a Pascal string to upper case"""
      return (s.title(), "")
    
    
    assert capital_case_pstr('hello world') == ('Hello World', '')
    assert capital_case_pstr('python programming') == ('Python Programming', '')

Данный алгоритм - шаблон для приветсвия пользователя в стиле C-строк

#Стековая архитекутра

На текущей архитектуры требоволось реализовать алгоритм для подсчета количества четных чисел от 1 до n.

    def sum_even_n(n):
      """Sum of even numbers from 1 to n"""
      if n <= 0:
          return -1
      total = 0
      for i in range(1, n + 1):
          if i % 2 == 0:
              total += i
      return total


    assert sum_even_n(5) == 6
    assert sum_even_n(10) == 30
    assert sum_even_n(90000) == 2025045000


#Аккумуляторная архитектура

На ней реализован алгоритм подсчета дилителей для числа N

      def count_divisors(n):
        """Count the number of divisors of a natural number"""
        if n < 1:
            return -1
        count = 0
        for i in range(1, n + 1):
            if n % i == 0:
                count += 1
        return count


    assert count_divisors(2) == 2
    assert count_divisors(4) == 3
    assert count_divisors(6) == 4
    assert count_divisors(10) == 4
