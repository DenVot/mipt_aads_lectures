# Книга лекций (A3)

Этот проект собирает все лекции в одну книгу с оглавлением.

## Структура

- `main.tex` — корневой файл книги и обложка.
- `presets.tex` — общие пакеты и макросы (перенесены из лекции).
- `lectures_manifest.tex` — список лекций, которые входят в книгу.
- `lectures/<номер_и_тема>/lecture.tex` — контент отдельной лекции.

## Как добавить новую лекцию

1. Создайте папку `lectures/NN_topic/`.
2. Добавьте файл `lectures/NN_topic/lecture.tex`.
3. Перенесите в него **только тело** лекции (без `\documentclass`, `\begin{document}`, `\end{document}`).
4. Подключите лекцию в `lectures_manifest.tex`:

```tex
\chapter{Название лекции}
\input{lectures/NN_topic/lecture.tex}
```

## Сборка

```bash
cd "Книга__Все_лекции_A3"
pdflatex -interaction=nonstopmode main.tex
pdflatex -interaction=nonstopmode main.tex
```
