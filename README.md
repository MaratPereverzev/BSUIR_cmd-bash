# BSUIR_cmd-bash
Данная лабораторная работа была предназначена для ознакомления с командной строкой операционных систем **Windows** и **Linux**.
В рамках ЛР 1 необходимо создать исполняемый файл *.bat* и *.sh* в соответствии с заданным вариантом.

## Условие ЛР 1 (48 вариант)
  ![image](https://github.com/MaratPereverzev/BSUIR_cmd-bash/assets/82408701/ec12d7e5-357f-4e71-894c-affaf5890131)
## Описание алгоритма, пример запуска и выполнения программы ([*.bat*](https://github.com/MaratPereverzev/BSUIR_cmd-bash/blob/main/48.bat) файл)
   ![image](https://github.com/MaratPereverzev/BSUIR_cmd-bash/assets/82408701/8432f8c8-ead3-4001-a3ce-1e2f491c5fdb)

   На вход программе приходит некоторое число и относительный путь к файлу, содержащему строки, в каждой из которых написано через пробел целое число и строка.
   
   #### Переменные:
  - *number* - хранит некоторое число, которое пришло на вход программе.
  - *path* - хранит относительный путь к файлу
  - *isInteger* - хранит результат произведения **number * 1** (в случае, если переменная **number** - число, то результат будет равен этому же числу соответственно; в ином случае - 0)
  - *dateStr* - хранит название файла, который необходимо создать

   #### Методы:
  - *checkNumber* - проверяет переменную **number** на валидность
  - *checkPath* - проверяет переменную **path** на валидность

   #### Последовательность действий:
  1. Ввод переменных *number* и *path*
  2. Вызов функций *checkNumber* и *checkPath*
  3. В случае валидности двух переменных, создаёт файл формата *текущая_дата.txt* и записывает туда данные согласно условию, иначе - завершает работу с выводом отладочной информации

   #### Пример запуска
   Запустим командную строку **cmd** любым удобным способом
   ![image](https://github.com/MaratPereverzev/BSUIR_cmd-bash/assets/82408701/8127643d-911c-4c45-ad39-045665b4251f)

   После запуска нас встречает командная строка. Для выполнения нашего [*.bat*](https://github.com/MaratPereverzev/BSUIR_cmd-bash/blob/main/48.bat) файла, перейдём в соответствующую папку для запуска нашего файла с помощью консольной команды *cd* (change directory)

      cd путь_к_файлу

   ![image](https://github.com/MaratPereverzev/BSUIR_cmd-bash/assets/82408701/6083e86f-6b19-4d02-ab32-353051964f9c)

   Для выполнения любого .bat файла, необходимо прописать консольную команду 
   
     start название_файла.bat

   ![image](https://github.com/MaratPereverzev/BSUIR_cmd-bash/assets/82408701/cb7b67b3-7140-423a-b3d9-59dd8b5d723e)

   Ваш .bat файл успешно запущен!!!!

   #### Пример выполнения программы
   Перед демонстрацией работы программы создадим произвольный текстовый файл с расширением **.txt** и заполним данными согласно условию

   ![image](https://github.com/MaratPereverzev/BSUIR_cmd-bash/assets/82408701/e1a813c2-f09e-4f2f-b9f1-09f912603834)

   На входе программа, соответствуя условию, запрашивает число и путь. Для отображения полного функционала введём для начала корректные данные

   ![image](https://github.com/MaratPereverzev/BSUIR_cmd-bash/assets/82408701/b056fde6-d28d-4c7c-881a-09681161f583)

   Программа успешно заканчивает работу, после чего переходим в папку, где хранится .bat файл и замечаем новый файл соответствующий формату *текущая_дата.txt*, давайте откроем его

   ![image](https://github.com/MaratPereverzev/BSUIR_cmd-bash/assets/82408701/fe2105b3-8dd0-4d39-995e-24cf90870de0)

   В результате программы было записано 2 строки, числа которых превышают введённое (500)

   ![image](https://github.com/MaratPereverzev/BSUIR_cmd-bash/assets/82408701/57dc8d9f-f1be-47fd-a3e4-53f014e31b81)

   Для проверки корректности работы программы, так же введём отрицательное значение

   ![image](https://github.com/MaratPereverzev/BSUIR_cmd-bash/assets/82408701/a071e3f4-8829-4fd9-af98-29c9f479c229)

   Из результата выполнения программы так же видно, что в файл записываются и те строки, число которых совпадает с введённым. Однако что будет если пользователь введёт некорректное число? Введём произвольную строку, состоящую не только из цифр и знака -

   ![image](https://github.com/MaratPereverzev/BSUIR_cmd-bash/assets/82408701/976b8ad1-a911-4797-b8f4-527ce788ae0d)

   В результате выполнения программы вывелась отладочная информация, что наша переменная *number* не имеет числовой тип данных. Такого рода проверки на корректность ввода остерегают пользователя от ввода некорректных данных и, несомненно, от непредсказуемого результата выполнения программы 

   ![image](https://github.com/MaratPereverzev/BSUIR_cmd-bash/assets/82408701/aef2053e-fc52-4516-b245-4b0822ecc659)

   Теперь введём наоборот, правильное число, но некорректный путь. В результате выполнения снова вывелась отладочная информация, но совершенно другого характера: такого пути не существует

   ![image](https://github.com/MaratPereverzev/BSUIR_cmd-bash/assets/82408701/88be4431-2291-4314-abd5-220765fc61fc)

   Так же в программе реальзовано условие на ввод лидирующих нулей (нулей, которые стоят перед самим числом). Давайте выполним программу с данной строкой

   ![image](https://github.com/MaratPereverzev/BSUIR_cmd-bash/assets/82408701/81099285-0241-4333-9b13-2e015112a5a0)

   Как результат программа завершилась успешно, а это значит, что в наш .txt файл что-то записалось. Так и есть, в файл записались строки, которые удовлетворяют нашему условию

   ![image](https://github.com/MaratPereverzev/BSUIR_cmd-bash/assets/82408701/87b8f25f-e53a-4827-aa3e-e9430f24556b)


   #### На этом функционал .bat файла заканчивается. Теперь рассмотрим подробнее .sh файл
---