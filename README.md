# MarkelovAM
1. Установил GitCmd, and GitHab
1.2   Создал учетную запись на GitHub:
    ```
    git config --global user.name "MinisterWise"
    git config --global user.email "akexandrmarkelov2004rex@gmail.com"
    ```
2.3.4. Создал репозиторий на GitHub и папку в который его поместил:
   * Создал локальный репозиторий:
     ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/b8ff440f-eb90-46bf-961a-27882038d20d)

      ```
      mkdir git_work
      cd git_work
      git init
      ```
5. Создал пустой текстовый файл и добавил его в локальный репозиторий:
       ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/3211e3b9-9b57-410c-bfe1-a5045aca6175)
       
      ```
    echo > worktext.txt
    git add worktext.txt
    git commit -m "Добавлен пустой текстовый файл"
    
      ```
6. Сделал 5 абзацев в текстовом файле:
     ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/9c00faf4-10e4-4304-983b-fed2853395f6)
6.2 Создал commit на ru для каждого абзаца, но мой Git CMD не поддерживает tu при чеке :
     ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/8ca23e44-e8bb-4072-98d8-50301b1623fa)

7. Посмотрел статус текущего репозитория:
  ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/567d8726-9818-4d6b-8870-ee0c201735c5)

      ```
      git status
      ```

8. Добавил новый файл: newfile.txt
   ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/52e0fcec-8ed7-43e6-948c-96885f83d296)

      ```
      git add newfile.txt
      ```
9. Создал коммит, указал для него комментарий:
    ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/4db8a601-5623-492b-9760-2fe7103c82bb)
   ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/33cbdd9f-4f39-4d6b-be98-fa8122bb61ec)

10. Посмотрел протокол коммитов:
  ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/5f7eb4d9-8138-4373-9c27-84f85f3fbe65)

      ```
      git log
      ```

11. Посмотрел изменения в файле по сравнению с последним коммитом, изминений нет:
    ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/ea66f2c2-9f59-41e1-90a5-c2f7d22bfd44)
      ```
      git diff HEAD worktext.txt
      git diff HEAD newfile.txt
      ```
12. Убрал последние изминения из файла:
    ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/e8c75ec3-da2b-438a-b7fc-cd01f4609ccc)
    ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/79a30244-dc1d-4b54-b4f6-de207c2844cf)

      ```
      git checkout -- newfile.txt
      git checkout -- worktext.txt
      ```

13. Просмотрел существующие ветки:
    ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/33f52a54-d275-4e46-889c-b042cc0ded6a)

      ```
      git branch
      ```
14. Создал новую ветку:
![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/6ac684f5-9d59-41e6-bd1d-eebb7e9321f0)
![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/2232e48c-689f-4e5a-98a6-af42b2abc720)


      ```
      git branch new_vetka
      ```
15. Переключился на новую ветку:
![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/0cb121dd-c254-4424-b898-ead270da302e)

      ```
      git switch new_vetka
      ```
16.Создал новую ветку и сразу же переключился на нее:
![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/91400b61-876c-46c7-817a-f248b18c31ba)
     
      ```
      git switch -c new_branch_name
      ```
17. Переключился на старую ветку и удалил новую ветку:
    ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/5aa9c3ef-d13b-490b-b8ef-559ea5aa6f53)

      ```
      git branch -d new_branch_name
      ```
18. Добавил (merge) изменения из указанной ветки в текущую:
    ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/f2066293-45fa-4c07-a0b3-3f2c20296d13)

      ```
      git merge master
      ```

19.Создал конфликт добавив одни изминения в ветку master и другие в new_vetka и попробовал соединить воедино данные ветки:
    ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/f150ed59-ffb0-49bc-866a-eecdc7103fa7)
      ```
      git merge new_vetka
      ```
20.21 Для того чтобы мне исправить данный конфликт, мне нужно убрать изминения с ветки master и отменить слияние веток:
    ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/4e32f0b1-7cf6-43a6-9651-ae25fca9cc76)
    ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/fd958c98-7330-4159-aae8-c3ed198e62cc)

22.Переключиться на указанный коммит:
 
  ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/4b1b44dc-189a-4760-9395-27e19b053399)

      ```
      git checkout 085a3eb369aebe9894ad6df16526855b88bcfa2
      git checkout b99e7d6
      ```
23.Сделать ребазирование (rebase) текущей ветки:
![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/02e658cc-0875-40ab-97ca-93146d7a5d99)
      ```
      git rebase b99e7d6
      ```


24.Удалить ветку new_vetka:
![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/62435e1a-994e-43e3-9485-d9311316b274)

      ```
      git branch -d new_vetka
      git branch -D new_vetka
      ```
25. Пропустить текущий кмфликтыный коммент:
    ![image](https://github.com/MinisterWise/MarkelovAM/assets/163382199/8b2175b7-a76a-4bcc-859f-8cfb0f588a8f)
      ```
      git rebase --skip
      ```
26.

