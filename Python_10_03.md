# ТИП 2
## № 72587
Логическая функция F задаётся выражением:
(x → (z → w)) ∧ (z → (y ≡ ¬ w))
```
print("x y z w")
for x in range(0, 2):
    for y in range(0, 2):
        for z in range(0, 2):
            for w in range(0, 2):
                if (x <= (z <= w)) and (z <= (y == (not w))):
                    print(x, y, z, w)
```
# Ответ: xzyw
## № 76699
Логическая функция F задаётся выражением:
(x ≡ ¬(w ≡ y)) ∧ (w ≡ (y → z)).
Дан частично заполненный фрагмент, содержащий неповторяющиеся строки таблицы истинности функции F.
```
print("x y z w")
for x in range(2):
    for y in range(2):
        for z in range(2):
            for w in range(2):
                if ((x == (int(not (w == y)))) and (w == (y <= z))):
                    print(x, y, z, w)
```
# Ответ: yzxw
## № 78027
Миша заполнял таблицу истинности логической функции F
(x ∧ y ∨ ¬x) ∧ w ∨ z,
но успел заполнить лишь фрагмент из трёх различных её строк, даже не указав, какому столбцу таблицы соответствует каждая из переменных w, x, y, z.
```
print("x y z w F")
for x in range(2):
    for y in range(2):
        for z in range(2):
            for w in range(2):
                F = ((x and y or not x) and w) or z
                if not F: 
                    print(x, y, z, w, 0)
```
# Ответ: zxyw

# ТИП 3
## № 59741
Сколько существует чисел, восьмеричная запись которых содержит 5 цифр, причем в записи нет цифры 1. Также все цифры записи различны и никакие две чётные и две нечётные цифры не стоят рядом.
```
count = 0
for a in '234567':
    for b in '0234567':
        if b == a: continue
        for c in '0234567':
            if c == a or c == b: continue
            for d in '0234567':
                if d == a or d == b or d == c: continue
                for e in '0234567':
                    if e == a or e == b or e == c or e == d: continue
                    if ((a in '1357') != (b in '1357') and
                        (b in '1357') != (c in '1357') and
                        (c in '1357') != (d in '1357') and
                        (d in '1357') != (e in '1357')):
                        count += 1
print(count
```
# Ответ: 180
## № 3693
Все 5-⁠буквенные слова, составленные из 5 букв А, К, Л, О, Ш, записаны в алфавитном порядке.
Вот начало списка:
1.  ААААА
2.  ААААК
3.  ААААЛ
4.  ААААО
5.  ААААШ
6.  АААКА
На каком месте от начала списка стоит слово ШКОЛА?
```
word = 'ШКОЛА'
number = 0
for ch in word:
    if ch == 'А': number = number * 5 + 0
    elif ch == 'К': number = number * 5 + 1
    elif ch == 'Л': number = number * 5 + 2
    elif ch == 'О': number = number * 5 + 3
    elif ch == 'Ш': number = number * 5 + 4
print(number + 1)
```
# Ответ: 2711
## № 27379
Виктор составляет 4-⁠буквенные коды из букв В, И, К, Т, О, Р. Каждую букву можно использовать не более одного раза, при этом нельзя ставить рядом две гласные и две согласные. Сколько различных кодов может составить Виктор?
```
count = 0
letters = 'ВИКТОР'
vowels = 'ИО'
for a in letters:
    for b in letters:
        if b == a: continue
        for c in letters:
            if c == a or c == b: continue
            for d in letters:
                if d == a or d == b or d == c: continue
                if ((a in vowels) != (b in vowels) and
                    (b in vowels) != (c in vowels) and
                    (c in vowels) != (d in vowels)):
                    count += 1
print(count)
```
# Ответ: 48
