**Используя команду cat, создать два файла с данными, а затем объединить их.**

cat > file1

cat > file2

cat file1 file2 > file_merge

**Просмотреть содержимое созданного файла.**

cat file_merge

**Переименовать файл, дав ему новое имя.**

mv file_merge file_merge_rename

**Создать несколько файлов.**

touch file3 file4

**Создать директорию, переместить файл туда.**

mkdir dir

mv file_merge_rename dir/

**Удалить все созданные в этом и предыдущем задании директории и файлы.**

rm -rf *

**Создать файл file1 и наполнить его произвольным содержимым.**

cat > file1

**Скопировать его в file2**

cat file1 > file2

**Создать символическую ссылку file3 на file1.**

ln -s /home/roman/file1 file3

**Создать жесткую ссылку file4 на file1.**

ln file1 file43

**Посмотреть, какие айноды у файлов.**

drwxrwxr-x 2 roman roman 4096 мар 30 21:45 ./

drwxr-x--- 8 roman roman 4096 мар 30 21:30 ../

-rw-rw-r-- 2 roman roman   13 мар 30 21:43 file1

-rw-rw-r-- 1 roman roman   13 мар 30 21:44 file2

lrwxrwxrwx 1 roman roman    5 мар 30 21:45 file3 -> file1

-rw-rw-r-- 2 roman roman   13 мар 30 21:43 file43


**Удалить file1**

rm file1

**Что стало с остальными созданными файлами? Попробовать вывести их на экран.**

drwxrwxr-x 2 roman roman 4096 мар 30 21:46 ./

drwxr-x--- 8 roman roman 4096 мар 30 21:30 ../

-rw-rw-r-- 1 roman roman   13 мар 30 21:44 file2

lrwxrwxrwx 1 roman roman    5 мар 30 21:45 **file3 -> file1**

-rw-rw-r-- 1 roman roman   13 мар 30 21:43 file43


**Дать созданным файлам другие, произвольные имена.**

mv file2 file2_rename

**Создать новую символическую ссылку. Переместить ссылки в другую директорию.**

ln -s /home/roman/file2_rename file2_rename_ls

mkdir dir

mv file2_rename_ls dir/