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
   2. daaa3d32ff98ffad7321c14815438b28a75835295
   3. 1c9f8b890cdd43c31c44647f34f1497de3c5edbd

   Создадим новую ветку для процедур `git checkout -b HW` <br>
   `git revert d014a17ca049ad5389484b1cf29e695ab7d36dcf` <br>

