#  Eatly — Планування харчування та підбір рецептів

## Опис
Веб-додаток, що допомагає користувачам планувати своє харчування, рахувати калорії, зберігати щоденник харчування та підбирати рецепти за наявними інгредієнтами.  


## Інсталяція та запуск

### Клонування репозиторію
bash
git clone <посилання>
1.  Запуск фронтенду
cd frontend
npm install
npm run dev
3.  Запуск бекенду
cd backend
pip install -r requirements.txt
uvicorn main:app –reload
4.  Налаштування БД
1.  Створіть .env файл у backend/
2.  Вкажіть змінні оточення:
DATABASE_URL=postgresql://user:password@localhost:5432/dbname
JWT_SECRET=ваш_секрет
alembic upgrade head
 
 
#### Структура репозиторію
1.  /frontend — код React застосунку
2.  /backend — бекенд на Flask
3.  /docs — документація, макети


#### Технології
1.  Frontend: HTML/CSS, JS
2.  Backend: Python, Flask, Postman
3.  Database: SQLAlchemy
4.  CI/CD: GitHub 




### Автори
1.  Стольнікова Альона — HTML/CSS, JS
2.  Синицина Оксана — HTML/CSS
3.  Любаневич Анастасія — Авторизація
4.  Глушко Марія — Функції
5.  Мельничук Анастасія — База даних, рецепти
6.  Петрівська Зореслава — UI/UX, дизайн, Product owner
7.  Лагодна Марія — Project manager
