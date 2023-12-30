# mycode
домашнее задание
Задача 1:
Ver.1 :
def check_temperature (temperature):
if temperature < 15.5:
return "ХОЛОДНО"
elif temperature > 28:
return "ЖАРКО"
else:
return "НОРМАЛЬНО"

# Считываем температуру с клавиатуры
temp_in_cel = float(input("Введите температуру в градусах Цельсия: "))

# Проверяем температуру и выводим результат
result = check_temperature (temp_in_cel)
print("Сейчас", result)

Ver. 2 :
def check_temperature (temperature):
if temperature < 15.5:
return "ХОЛОДНО"
elif temperature > 28:
return "ЖАРКО"
else:
return "НОРМАЛЬНО"

# Считываем температуру с клавиатуры, но теперь не выдает ошибку при введении запятой вместо точки
temp_in_cel = float(input("Введите температуру в градусах Цельсия: ").replace(',', '.'))

# Проверяем температуру и выводим результат
result = check_temperature (temp_in_cel)
print(result)

Задача 2:
def найти_кота(строки):
for строка in строки:
if 'Кот' in строка or 'кот' in строка:
return True
return False

# Считываем количество строк
количество_строк = int(input("Введите количество строк: "))

# Считываем строки
строки = []
for _ in range(количество_строк):
строка = input("Введите строку: ")
строки.append(строка)

# Проверяем наличие кота и выводим результат
if найти_кота(строки):
print("МЯУ")
else:
print("НЕТ")

Ver. 2
def naiti_kota(stroki):
return any('Кот' in stroka or 'кот' in stroka for stroka in stroki)

# Считываем количество строк
kolichestvo_strok = int(input("Введите количество строк: "))

# Считываем строки
stroki = [input("Введите строку: ") for _ in range(kolichestvo_strok)]

# Проверяем наличие кота и выводим результат
if naiti_kota(stroki):
    print("МЯУ")
else:
    print("НЕТ")

Ver. 3
def naiti_kota(stroki):
  return any('Кот' in stroka or 'кот' in stroka for stroka in stroki)

# Считываем количество строк
while True:
try:
n = int(input("Введите количество строк: "))
break
except ValueError:
print("Некорректный ввод. Введите целое число.")

# Считываем строки
stroki = [input() for _ in range(n)]

# Проверяем наличие кота и выводим результат
if naiti_kota(stroki):
print("МЯУ")
else:
print("НЕТ")

Задача 3:

Ver 1
def проверить_буквы(короткое, длинное):
# Проверяем, содержатся ли все буквы короткого слова в длинном
return all(буква in длинное for буква in короткое)

# Считываем слова
слова = []
while True:
слово = input("Введите слово (или 'стоп' для завершения): ")
if слово.lower() == 'стоп':
break
слова.append(слово)

# Находим самое короткое и самое длинное слово
самое_короткое = min(слова, key=len)
самое_длинное = max(слова, key=len)

# Проверяем, содержатся ли все буквы короткого слова в длинном
результат = "ДА" if проверить_буквы(самое_короткое, самое_длинное) else "НЕТ"

# Выводим результат
print(f"Самое короткое слово: {самое_короткое}")
print(f"Самое длинное слово: {самое_длинное}")
print(f"Содержатся ли все буквы короткого слова в длинном: {результат}")

Ver. 2
def проверить_буквы(короткое, длинное):
# Проверяем, содержатся ли все буквы короткого слова в длинном
return all(буква in длинное for буква in короткое)

# Считываем слова
слова = []
while True:
слово = input("Введите слово: ")
if слово.lower() == 'стоп':
break
слова.append(слово)

# Находим самое короткое и самое длинное слово
самое_короткое = min(слова, key=len)
самое_длинное = max(слова, key=len)

# Проверяем, содержатся ли все буквы короткого слова в длинном
результат = "ДА" if проверить_буквы(самое_короткое, самое_длинное) else "НЕТ"

# Выводим результат
print(результат)

Ver. 3
def check_letters(short, long):
# Проверяем, содержатся ли все буквы короткого слова в длинном
return all(letter in long for letter in short)

# Считываем слова
words = []
while True:
word = input()
import sys
word = sys.stdin.buffer.raw.readline().decode('utf-8').strip()
if word.lower() == 'стоп':
break
words.append(word)

# Находим самое короткое и самое длинное слово
shortest_word = min(words, key=len)
longest_word = max(words, key=len)

# Проверяем, содержатся ли все буквы короткого слова в длинном
result = "ДА" if check_letters(shortest_word, longest_word) else "НЕТ"

# Выводим результат
print(result)


Задача 4
Ver. 1:
# Считываем количество покупок
количество_покупок = int(input("Введите количество покупок: "))

# Считываем сами покупки
список_покупок = []
for _ in range(количество_покупок):
    покупка = input("Введите название покупки: ")
    список_покупок.append(покупка)

# Выводим список покупок
print("Список покупок:")
for покупка in список_покупок:
    print(покупка)

Ver. 2:
# Считываем количество покупок
количество_покупок = int(input("Введите количество покупок: "))

# Считываем сами покупки и создаем список
список_покупок = [input("Введите название покупки: ") for _ in range(количество_покупок)]

# Выводим список покупок
print("Список покупок:")
for покупка in список_покупок:
    print(покупка)

Ver. 3:
# Считываем количество покупок
import sys
n = int(sys.stdin.buffer.raw.readline().decode('utf-8').strip())

# Считываем сами покупки и создаем список
покупки = [sys.stdin.buffer.raw.readline().decode('utf-8').strip() for _ in range(n)]

# Выводим список покупок
print ('\n')
print(*покупки, sep='\n')




Задача 5
# Считываем строку
line = input("Введите строку: ")

# Создаем новую строку, повторяя каждый символ дважды
new_line= ''.join([symbol * 2 for symbol in line])

# Выводим новую строку
print(new_line)

Задача 6
def greet():
    # Спрашиваем у пользователя имя и фамилию
    name = input("Введите ваше имя: ")
    surname = input("Введите вашу фамилию: ")

    # Выводим официальное приветствие
    print(f"Здравствуйте, {name} {surname}.")

# Вызываем функцию
greet()

Задача 7
class LittleBell:
    def sound(self):
        print("ding")

# Пример использования
bell = LittleBell()
bell.sound()
