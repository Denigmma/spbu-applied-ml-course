# Прикладные задачи машинного обучения: домашние задания

Мурадян Денис Степанович, 4 курс бакалавриата ИИНД СПбГУ

## ДЗ 1. CUB-200-2011

Классификация 200 видов птиц. Сравнить три архитектуры и проверить, как на качество влияют итеративная разморозка, аугментация и псевдолейблинг.

[Ноутбук ДЗ 1](https://github.com/Denigmma/spbu-applied-ml-course/blob/7b82875f2c100eb5d358fc8e30d819ccf2170d98/hw1_iterative_training/hw1_cub200.ipynb) · [PR с решением](https://github.com/Denigmma/spbu-applied-ml-course/pull/1)

## ДЗ 2. Агрегация асессорских оценок

Сгенерировать или найти датасет асессорских оценок, посчитать по нему разные статистики и описать, почему они похожи на реальные данные. Применить Majority Vote, Weighted Majority Vote и Dawid-Skene. Замерить качество и сделать выводы.

В Toloka Relevance 5 асессоры оценивали релевантность документа запросу по шкале от 1 до 5. Сравнил три метода на 23 702 тестовых заданиях. Для документов с двумя допустимыми оценками засчитывал попадание в любую из них. Отдельно разобрал, чем контроль отличается от остальных заданий, какие градации путают асессоры и на каких классах ошибается каждый метод.

[Ноутбук ДЗ 2 с результатами](hw2_crowd_label_aggregation/hw2_toloka.ipynb) · [Датасет на Kaggle](https://www.kaggle.com/datasets/edsukhodolskaya/toloka-aggregation-relevance-5)

### Запуск ДЗ 2

На Kaggle импортируйте ноутбук, подключите датасет **Toloka Aggregation Relevance 5** через **Add Input** и запустите все ячейки по порядку. Достаточно CPU. Таблицы и графики последнего прогона также доступны в ноутбуке на GitHub.

Для запуска в Jupyter из корня репозитория понадобится Python 3.12. При первом запуске с доступом в интернет ноутбук скачает данные через `kagglehub`.

```bash
python -m pip install -r hw2_crowd_label_aggregation/requirements.txt
jupyter lab hw2_crowd_label_aggregation/hw2_toloka.ipynb
```

Чтобы повторить расчёт из командной строки и сохранить выводы в отдельном файле:

```bash
jupyter nbconvert --to notebook --execute --ExecutePreprocessor.timeout=1800 --output hw2_check.ipynb hw2_crowd_label_aggregation/hw2_toloka.ipynb
```
