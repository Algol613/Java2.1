# Отчёт о тестировании приложения "BankTransfer"
Необходимо проверить работу банковского приложения отображающего причину ошибки при трансфере денежных средств на счет VIP-клиента


Для проверки данной ошибки было принято решение воссоздать ситуацию в IntelliJ IDEA.

Были воспроизведены следующие шаги:

1 Запустить приложение IntelliJ IDEA

2 Cоздать новый проект Java2.1

3 Создать и заполнить файлы .gitignore и README.md из

https://github.com/netology-code/javaqa-homeworks/blob/master/.gitignore

https://github.com/netology-code/javaqa-homeworks/blob/master/programming/report.md

4 Запустить терминал Alt+F12

5 Инициализировать папку командой git init

6 Создать базовое приложение (на основании примера, который рассматривался на лекции), позволяющее воспроизвести ситуацию

7 Добавить и сохранить файлы в локальном репозитории

8 Отправить данные с локального репозитория на GitHub


### Было произведено:
 
Функциональное компонентное тестирование по позитивному сценарию.

## Результаты:

https://github.com/Algol613/Java2.1/issues/1

# Общие рекомендации:

Заменяем в 

    public class BankTransfer {

        public static void main(String[] args) {
        int score = 2_000_000_000;
        int transfer = 500_000_000;
        score = score + transfer;

        System.out.println(score);
        }

    }
 
 на 

    public class BankTransfer {

        public static void main(String[] args) {
        long score = 2_000_000_000;
        int transfer = 500_000_000;
        score = score + transfer;

        System.out.println(score);
        }

    }

и при Run получим корректные данные.

## Рекомендации:
Рекомендовано выделить категорию VIP-клиентов и написать для них отдельный код расчета, допускающий большие значения на счетах.
