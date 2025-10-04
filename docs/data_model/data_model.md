# Модель даних проєкту "Здорове харчування"

## Сутності та атрибути

### Users
| Атрибут | Тип даних | Примітка |
|---------|-----------|----------|
| user_id | INT       | PK       |
| username | VARCHAR  | обов'язково |
| email    | VARCHAR  | обов'язково, унікальний |
| password | VARCHAR  | обов'язково |
| age      | INT      | опційно |
| height   | FLOAT    | опційно |
| weight   | FLOAT    | опційно |
| goal     | VARCHAR  | ціль користувача |
| goalweight | FLOAT  | бажана вага |

### Recipes
| Атрибут | Тип даних | Примітка |
|---------|-----------|----------|
| recipe_id | INT     | PK       |
| dishname  | VARCHAR | обов'язково |
| ingredients | TEXT | обов'язково |
| instructions | TEXT | обов'язково |
| calories | FLOAT   | обов'язково |
| proteins | FLOAT   | обов'язково |
| fats     | FLOAT   | обов'язково |
| carbs    | FLOAT   | обов'язково |

### Menudesc_info
| Атрибут | Тип даних | Примітка |
|---------|-----------|----------|
| daymenu_id | INT    | PK       |
| user_id    | INT    | FK → Users.user_id |
| total_calories | FLOAT | підсумок за день |
| total_proteins | FLOAT | підсумок за день |
| total_fats     | FLOAT | підсумок за день |
| total_carbs    | FLOAT | підсумок за день |

### Menu_items
| Атрибут | Тип даних | Примітка |
|---------|-----------|----------|
| position_id | INT     | PK       |
| daymenu_id  | INT     | FK → Menudesc_info.daymenu_id |
| recipe_id   | INT     | FK → Recipes.recipe_id |
| meal_type   | VARCHAR | тип прийому їжі (сніданок, обід, вечеря) |

### Favourites
| Атрибут | Тип даних | Примітка |
|---------|-----------|----------|
| fav_id  | INT       | PK       |
| user_id | INT       | FK → Users.user_id |
| recipe_id | INT     | FK → Recipes.recipe_id |
