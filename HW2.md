# Урок 2. Работа с изменениями

1. Просмотрите историю коммитов в своём проекте и выберите три случайных коммита. Просмотрите изменения, которые были в них сделаны.

2. Верните эти изменения командой git revert последовательно, чтобы в итоге получилось тоже три коммита.

3. Попробуйте отменить эти три коммита:

- последний — командами git reset --soft и git restore;
- предпоследний — командой git reset --mixed и git restore;
- первый — командой git reset --hard.

### Solution:

#### Для выполнения домашнего задания использовался репозиторий https://github.com/Silva0308/git_adv_sem2
1. Просмотр коммитов
commit 51d2ea70fdfe3d2360508377b8494c0017cdcca6 (HEAD -> main, origin/main)
Author: Silva0308 <v.travinina@gmail.com>
Date:   Wed Jul 5 17:17:26 2023 +0300

    gitinnor added

commit 8897d25c3fd2a037185a5e518b32e931b2a3161b
Author: Daniil Pilipenko <sortedmap@gmail.com>
Date:   Tue Nov 1 10:42:31 2022 +0300

    refactoring

commit daaa3d32ff98ffad7321c14815438b28a7583529
Author: Daniil Pilipenko <sortedmap@gmail.com>
Date:   Tue Nov 1 10:37:58 2022 +0300

    reset button enabling/disabling added

commit bbf1b69d61ce9ebadb0ecfe9563a50bf0a88b3d5
Author: Daniil Pilipenko <sortedmap@gmail.com>
Date:   Tue Nov 1 10:36:46 2022 +0300

    reset button added

commit fe4e2639663f50c652dc7dfcae7c715bba3e87f8
Author: Daniil Pilipenko <sortedmap@gmail.com>
Date:   Tue Nov 1 10:29:18 2022 +0300

    button inactivation added

    etc...

    2. Используемые коммиты:

   1. d014a17ca049ad5389484b1cf29e695ab7d36dcf
   2. 51d2ea70fdfe3d2360508377b8494c0017cdcca6
   3. 8897d25c3fd2a037185a5e518b32e931b2a3161b

   Создадим новую ветку для процедур `git checkout -b HW` <br>
   `git revert d014a17ca049ad5389484b1cf29e695ab7d36dcf` <br>

```
       Автослияние index.html
[HW ec56715] Revert "text styles changed" for homework
 1 file changed, 1 insertion(+), 1 deletion(-)
   ```

   `git add .` <br>

   `git revert 51d2ea70fdfe3d2360508377b8494c0017cdcca6` <br>
   ```
   [HW 33ba4bd] Revert "gitinnor added" for hw
 3 files changed, 343 insertions(+), 1 deletion(-)
 delete mode 100644 .gitignore
 create mode 100644 logs/access.log
 create mode 100644 logs/error.log
```
   `git revert 8897d25c3fd2a037185a5e518b32e931b2a3161b` <br>

   ```
      подсказка: Ожидание, пока вы закроете редактор с файлом... error: There was a problem with the editor 'vi'.
Пожалуйста, укажите сообщение, при указании опций -m или -F.
   ```


3. Отмена коммитов:

   1. `git reset --soft 9526c49aab999a14cc9221fb4000abe5f2db97e3` <br>
      `git status` <br>

      ```
     Текущая ветка: HW
Изменения, которые будут включены в коммит:
  (используйте «git restore --staged <файл>...», чтобы убрать из индекса)
        изменено:      HW2.md

Изменения, которые не в индексе для коммита:
  (используйте «git add <файл>...», чтобы добавить файл в индекс)
  (используйте «git restore <файл>...», чтобы отменить изменения в рабочем каталоге)
        изменено:      HW2.md
           
      ```

      `git restore --staged staged HW2.md` <br>
      `git restore staged HW2.md` <br>

   2. `git reset --mixed 33ba4bdb122a3e93cae3b3958c6559639f278f38` <br>
      `git status`

      ```
        Непроиндексированные изменения после сброса:
M       HW2.md
M       main.js
      ```

      `git restore git restore HW2.md` <br>

   3. `git reset --hard 33ba4bdb122a3e93cae3b3958c6559639f278f38` <br>

      ```
      Указатель HEAD сейчас на коммите 33ba4bd Revert "gitinnor added" for hw
      ```