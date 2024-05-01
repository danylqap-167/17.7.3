def numbers_sort(numbers):
    for i in range(1, len(numbers)):
        x = numbers[i]
        idx = i
        while idx > 0 and numbers[idx - 1] > x:
            numbers[idx] = numbers[idx - 1]
            idx -= 1
        numbers[idx] = x
    return numbers


def binary_search(numbers, num, left, right):
    position = -1

    while left <= right:
        mid = (left + right) // 2

        if numbers[mid] < num:
            left = mid + 1
        elif numbers[mid] >= num:
            position = mid
            right = mid - 1

    if position != -1 and position <= len(numbers) - 1:
        return position
    else:
        return -1


while True:
    sequence = input("Введите последовательность чисел, разделенных пробелом: ")
    try:
        numbers = list(map(float, sequence.split()))
        if len(numbers) < 2:
            print("Пожалуйста, введите как минимум два числа.")
        else:
            break
    except ValueError:
        print("Неверный ввод. Пожалуйста, введите числа, разделенные пробелами.")

# Сортируем список по возрастанию с помощью функции numbers_sort
numbers = numbers_sort(numbers)

#  проверяем его на корректность
while True:
    try:
        num = float(input("Введите любое число: "))
        break
    except ValueError:
        print("Неверный ввод. Пожалуйста, введите число.")

index = binary_search(numbers, num, 0, len(numbers) - 1)

# Выводим результат
if index <= 0:
    print(f"Введенное пользователем число {num} не отвечает условиям задачи.")
elif index == -1:
    print(f"Введенное пользователем число {num} не отвечает условиям задачи.")
else:
    print(
        f'Номер позиции элемента равен {index - 1}, меньше введенного пользователем числа: {num} в списке {numbers}.')
    print(f"Элемент, больший или равный введенному числу {num}, на позиции {index}.")
