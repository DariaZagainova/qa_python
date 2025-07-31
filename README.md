# qa_python Sprint_4

## Описание

#### Приложение BooksCollector. 
Позволяет установить жанр книг и добавить их в избранное.

## Функциональность

#### Класс BooksCollector содержит:
Словарь books_genre, куда можно добавить пару 
Название книги: Жанр книги.
Список favorites, который содержит избранные книги.
Список genre, который содержит доступные жанры.
Список genre_age_rating, который содержит жанры с возрастным рейтингом.
#### Набор методов для работы со словарем books_genre и списком favorites: 
1. **_add_new_book_** — добавляет новую книгу в словарь без указания жанра. Название книги может содержать максимум 40 символов. Одну и ту же книгу можно добавить только один раз.
2. **_set_book_genre_** — устанавливает жанр книги, если книга есть в books_genreи её жанр входит в списокgenre.
3. **_get_book_genre_** — выводит жанр книги по её имени.
4. **_get_books_with_specific_genre_** — выводит список книг с определённым жанром.
5. **_get_books_genre_** — выводит текущий словарь books_genre.
6. **_get_books_for_children_** — возвращает книги, которые подходят детям. У жанра книги не должно быть возрастного рейтинга.
7. **_add_book_in_favorites_** — добавляет книгу в избранное. Книга должна находиться в словаре books_genre. Повторно добавить книгу в избранное нельзя.
8. **_delete_book_from_favorites_** — удаляет книгу из избранного, если она там есть.
9. **_get_list_of_favorites_books_** — получает список избранных книг.

## Покрытие тестами

#### Тесты реализованы с использованием pytest и проверяют:

1. **_test_add_new_book_add_two_books_books_count_is_two_** - метод _add_new_book_, добавление двух новых книг.
2. **_test_set_book_genre_valid_input_genre_assigned_** - методы *set_book_genre*, при передаче корректных данных жанр книги устанавливается и получаем словарь books_genre с указаанием жанра.
3. **_test_get_book_genre_existing_book_returns_correct_genre_** - методы *get_book_genre*, получаем словарь books_genre с жанром книги по её названию.
4. **_test_get_books_with_specific_genre_fantasy_return_all_matching_books_** - метод *get_books_with_specific_genre*, выводятся все добавленные книги в жанре фантастики.
5. **_test_get_books_genre_new_collector_returns_empty_dict_** - метод *get_books_genre* возвращает пустой словарь для нового объекта.
6. **_test_get_books_for_children_books_with_allowed_genres_in_list_** - метод *get_books_for_children*, если книга не принадлежит к жанру из возрастных ограничений, то она включается в список, возвращаемый методом.
7. **_test_add_book_in_favorites_new_book_added_** - метод *add_book_in_favorites*, новая книга добавляется в список избранных.
8. **_test_add_book_in_favorites_book_already_in_favorites_not_added_** - метод *add_book_in_favorites*, книга повторно не добавляется, если она уже есть в списке избранных.
9. **_test_delete_book_from_favorites_book_in_favorites_book_removed_** - метод *delete_book_from_favorites_books*, книга удаляется из списка избранных.
10. **_test_get_list_of_favorites_returns_all_favorite_books_** - метод *get_list_of_favorites* выводит список с избранными книгами.

#### Перед запуском тестов установить необходимые библиотеки:
pip install pytest pytest-cov

#### Запуск  тестов:
pytest -v tests.py

#### Проверка покрытия кода:
pytest --cov=main tests.py

#### Покрытие

Проект покрыт тестами на 100%.

| Name  | Stmts   | Miss  | Cover |
| :-----:|:-----:|:-----:|:----:|
|main.py| 38 | 0 | 100%|

## Автор

Daria Zagainova (40daria.z@gmail.com), когорта 28FS
