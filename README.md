# Document Processor
Этот проект реализует процессор документов, который обрабатывает входные данные о документах и возвращает результирующий документ с обновленными полями. Проект состоит из двух основных компонентов: основной логики и тестов.

# Структура проекта
document_processor.py: основной файл с реализацией классов Document и Processor.
test_document_processor.py: тестовый файл для проверки корректности работы метода Process.
### 1. Клонирование репозитория
bash

git clone [https://github.com/your-username/document-processor.](https://github.com/DmitriiEzhov/ML_Internship-VK-/tree/main)git

cd document-processor

### 2. Запуск основной логики
bash 

python document_processor.py

### 3. Запуск тестов
bash

python test_document_processor.py
# Описание классов
## Document
Класс Document представляет собой документ с полями:
### Url: уникальный идентификатор документа.
### PubDate: время публикации документа.
### FetchTime: время получения документа.
### Text: текст документа.
### FirstFetchTime: время первого получения документа (опционально).
## Processor
Класс Processor содержит метод Process, который принимает список документов и возвращает результирующий документ с обновленными полями на основе следующих правил:
Поля Text и FetchTime должны быть из документа с наибольшим FetchTime.
Поле PubDate должно быть из документа с наименьшим FetchTime.
Поле FirstFetchTime должно быть минимальным значением FetchTime.
