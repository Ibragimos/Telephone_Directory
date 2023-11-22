last_name = input("Введите фамилию для копирования: ")
# Запрашиваем у пользователя ввод фамилии для копирования

with open(source_file, 'r', encoding='utf-8') as source_f
# Открываем файл (source_file, мы его определяем в функции) для чтения ('r') и файловый объект сохраняется в переменной source_f

data = source_f.readlines()
# Прочитанные строки из исходного файла сохраняются в списке data

found_entries = [entry for entry in data if last_name in entry]
# Создаем новый список found_entries, содержащий только те записи, в которых встречается введенная пользователем фамилия (last_name). 
# Это достигается с использованием генератора списка и условия (if last_name in entry).

if not found_entries
# Проверяем, содержит ли список found_entries какие-либо записи. Если список пуст (нет записей с указанной фамилией), выводится сообщение об ошибке

with open(destination_file, 'a', encoding='utf-8') as dest_f
# Открывается целевой файл (destination_file) для добавления записей ('a' - append), и файловый объект сохраняется в переменной dest_f

dest_f.writelines(found_entries)
# Найденные записи с указанной фамилией записываются в целевой файл с использованием метода writelines
