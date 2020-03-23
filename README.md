# Отчёт о тестировании приложения "BankTransfer"
Необходимо проверить работу банковского приложения отображающего причину ошибки при трансфере денежных средств на счет VIP-клиента


Для проверки данной ошибки было принято решение воссоздать ситуацию в IntelliJ IDEA.

Были воспроизведены следующие шаги:

    Запустить приложение IntelliJ IDEA
    Cоздать новый проект Java2.1
    Создать и заполнить файлы .gitignore и README.md из
    https://github.com/netology-code/javaqa-homeworks/blob/master/.gitignore
    https://github.com/netology-code/javaqa-homeworks/blob/master/programming/report.md
    Запустить терминал Alt+F12
    Инициализировать папку командой git init
    Создать базовое приложение (на основании примера, который рассматривался на лекции), позволяющее воспроизвести ситуацию
    Добавить и сохранить файлы в локальном репозитории
    Отправить данные с локального репозитория на GitHub


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