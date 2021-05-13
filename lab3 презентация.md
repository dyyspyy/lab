---
marp: true
---


# **РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ**


### **Факультет физико-математических и естественных наук**
### **Кафедра прикладной информатики и теории вероятностей**

---

# **ОТЧЕТ** 
# **ПО ЛАБОРАТОРНОЙ РАБОТЕ № 	2**
### *дисциплина:	Операционные системы*


### Студент: Севастьянов Дмитрий Вадимович 
### Группа: НФИбд-02-20

###  **Москва**
### 2021

---
### **Цель работы:** Изучить идеологию и применение средств контроля версий

---
### 1.	Создаём аккаунт на github

![N|Solid](https://sun9-52.userapi.com/impg/RHacsKxp2DNo4Qsl0rYYcgEmXEHL-WHry0jf7A/mYVXmNWOu5k.jpg?size=641x161&quality=96&sign=493d3e95095f6a9734bf965ffaf7f50c&type=album)

---

### 2.	Генерируем ключи командой и копируем:
Ssh -keygen -C “Sevastyanov”
cat ~/.ssh/id_rsa.pub | xclip -sel clip
![N|Solid](https://sun9-45.userapi.com/impg/2NuIWvbw15VBIhQQL_dGQTEToArYsDa9sREQOg/yD-FKFsq4vg.jpg?size=455x303&quality=96&sign=e9ccc750a86f17cff7ca432cdcf6c117&type=album)

---

### 3. Вставляем публичный ключ на гит хаб
![N|Solid](https://sun9-2.userapi.com/impg/7wq6MhiMYZDcE_j06lzjkshCV5CwEvwwAcFJWA/opokepOu1Yk.jpg?size=403x277&quality=96&sign=1459dcb65bcc9c583fcd7aa1e16cedf3&type=album)

---

### 4. Создаём репозиторий:
![N|Solid](https://sun9-76.userapi.com/impg/Uv1pAOHwipmSeQRrr5Hy45HHXpM-LIjAUXmaEg/pwRS6wTKiHQ.jpg?size=541x547&quality=96&sign=759942016f575e0e4115db255a3b7f6f&type=album)

---
### 5.	Инициализируем системы git:
 git init
### И создаём заготовку для файла README.md: 
echo "# Лабораторные работы" >> README.md git add README.md
![N|Solid](https://sun9-8.userapi.com/impg/m9zZAutYKKh7iW10q1diZe9Y3C8H-QP0bidGLQ/tQ8YNN34L4A.jpg?size=531x417&quality=96&sign=abbb843da1e09f641765f9c72b6d02fe&type=album)

---

### 6. Делаем первый коммит и выкладываем на github: 
git commit -m "first commit"
git remote add origin
> git@github.com:<username>/sciproc-intro.git 

---

git push -u origin master
![N|Solid](https://sun9-57.userapi.com/impg/S6-M1F7yzW-3n4EPTa6fLYAeQa-QUyhyuINi4A/aRe5YSCfgRo.jpg?size=831x365&quality=96&sign=5643066da362b0d867ed3d4a2d2e9d6b&type=album)

---

### 7. Добавим файл лицензии:
wget https://creativecommons.org/licenses/by/4.0/legalcode.txt
↪ -O LICENSE
### – Добавим шаблон игнорируемых файлов. Просмотрим список имеющихся шаблонов:
curl -L -s https://www.gitignore.io/api/list
![N|Solid](https://sun9-70.userapi.com/impg/ob3KRy00SAiy2a9GzsCmK3NJtTX3v3QFBFpGog/GENOwXB1LUk.jpg?size=835x363&quality=96&sign=5cbb1f87ab9645a4f68d0ba845851fbe&type=album)

---

### 8. Затем скачаем шаблон, например, для C:
curl -L -s https://www.gitignore.io/api/c >> .gitignore
![N|Solid](https://sun9-5.userapi.com/impg/RABWyOjRGKeHdIxERkeur0Kdn6iborsaXAXQPw/-T8at4u9zBk.jpg?size=574x205&quality=96&sign=515bb71f8b5ff1938528bb080e0f4be9&type=album)

---

### 9. Добавим новые файлы:
git add .
– Выполним коммит:
git commit -a
![N|Solid](https://sun9-9.userapi.com/impg/rEzymfhcXZf-EfJDhT3TDHK9PE9JVIMwh81pYQ/znsequweUtw.jpg?size=612x114&quality=96&sign=9207ad304a655fd68baa246e6dbea5a9&type=album)

---

### 10. Отправим на github:
git push
![N|Solid](https://sun9-18.userapi.com/impg/JiJYDxrcxXQXmm-ldbQubWpdB6TuBgUpyJZ8nw/BSPgr9m9RH8.jpg?size=540x150&quality=96&sign=7292eb327d493d9d78dc8ed8d0c2a6db&type=album)

---

### 11. Установили доп. Пакеты
![N|Solid](https://sun9-62.userapi.com/impg/VbiM5Rq44b_DYRwTRdTtpJcB89U8GPUVq_MVMQ/WKwkLh8rX8k.jpg?size=709x38&quality=96&sign=778d5f968f3b25787149e88c1097a85c&type=album)

---

### 12. Инициализируем git-flow
git flow init
Префикс для ярлыков установим в v.
– Проверьте, что Вы на ветке develop:
git branch
![N|Solid](https://sun9-8.userapi.com/impg/spqpOy16qOKE15gbGRwFiEJSgebc-7L-gX1nag/JoV-zp6LwCk.jpg?size=549x292&quality=96&sign=880df01da77be3d6244fde6fe00bbae7&type=album)

---

### 13. Создадим релиз с версией 1.0.0  - git flow release start 1.0.0
![N|Solid](https://sun9-16.userapi.com/impg/ckLCP0TjRTeqUoROcLPX5BI6oW6Y1TiF9xO2eA/vq5_CN4mCOI.jpg?size=691x309&quality=96&sign=e30531a41630c44221237c6000c036cc&type=album)

---

### 14. Запишем версию:
echo "1.0.0" >> VERSION
– Добавим в индекс:
git add .
git commit -am 'chore(main): add version'

---
– Зальём релизную ветку в основную ветку
git flow release finish 1.0.0
– Отправим данные на github
git push --all
git push --tags
– Создадим релиз на github.
![N|Solid](https://sun9-12.userapi.com/impg/_X-XAQwcfNLybMG8rXEqPueYPnkkl5Mhf95RVA/WmhHoShYyDk.jpg?size=685x276&quality=96&sign=fd39b49da1a3b1773861295647774567&type=album)

---

### 15. Всё появимлось 
![N|Solid](https://sun9-76.userapi.com/impg/7n6AaIaZI8QJwlZPJlrdoxZkw8kEHw3IodcWQQ/HTgw4gy_3fA.jpg?size=774x119&quality=96&sign=eff435a676708f18ecc32ab48e7ea840&type=album)

---


### **Вывод:** Я изучил идеологию и применение средств контроля версий








