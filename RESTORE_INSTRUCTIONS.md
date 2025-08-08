# Инструкции по восстановлению бэкапа Door Contracts

## 📦 Содержимое бэкапа

Этот бэкап содержит:
- ✅ Полный код проекта Laravel
- ✅ База данных SQLite (database-backup.sqlite)
- ✅ SQL дамп базы данных (database-dump.sql)
- ✅ Все зависимости и конфигурации
- ✅ Пользователи, договоры, филиалы, менеджеры

## 🔄 Как восстановить проект

### 1. Распакуйте архив
```bash
tar -xzf door-contracts-backup-20250806-092847.tar.gz
cd door-contracts-backup
```

### 2. Установите зависимости
```bash
composer install
npm install
```

### 3. Восстановите базу данных
```bash
# Скопируйте базу данных
cp database-backup.sqlite database/database.sqlite

# Или восстановите из SQL дампа
sqlite3 database/database.sqlite < database-dump.sql
```

### 4. Соберите ассеты
```bash
npm run build
```

### 5. Очистите кэш
```bash
php artisan cache:clear
php artisan config:clear
php artisan view:clear
php artisan route:clear
```

### 6. Запустите проект
```bash
php artisan serve
```

## 👥 Пользователи в системе

### Администратор
- Email: admin@admin.com
- Роль: admin

### Менеджеры
- Ербол Смаилов: erekesuperhero@gmail.com
- Дарина Жакай: darina.zhakay@mail.ru
- Жамбыл Пірәліұлы: zhambyl.piraliuly@gmail.com
- Зухра Махмутова: fatimamahmutova05@gmail.com
- Фарход Сулейманов: Faha_93_34@mail.ru
- Тоқмұсбек Әбілдабек: tokmusbek003@gmail.com
- Маржан Галымжановна: ozhantaevamarzhan@gmail.com
- Фатима Махмутова: fatima.mahkmutova@mail.ru
- Әлсейіт Әбсейіт: alseytabseyt@gmail.com
- Даулет Жаксибеков: dake.zb@mail.ru
- Амитова Сымбат: aktosha_00@mail.ru

### ROP пользователь
- Бақдаулет Сейдалы: bagdaulet_seydaly@mail.ru

## 🔧 Функциональность

### Для менеджеров (manager):
- ✅ Панель управления
- ✅ Управление менеджерами
- ✅ Просмотр договоров

### Для администраторов (admin):
- ✅ Все функции менеджера
- ✅ Управление пользователями
- ✅ Управление филиалами

## 🚀 Быстрый старт

1. Распакуйте архив
2. Перейдите в папку проекта
3. Выполните: composer install && npm install && npm run build
4. Скопируйте базу данных: cp database-backup.sqlite database/database.sqlite
5. Запустите: php artisan serve
6. Откройте: http://localhost:8000

---
Дата создания бэкапа: 6 августа 2025, 09:28
Версия проекта: Door Contracts v1.0
