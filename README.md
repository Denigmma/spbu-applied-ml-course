# Прикладные задачи машинного обучения: домашние задания

Мурадян Денис Степанович, 4 курс бакалавриата ИИНД СПбГУ

## ДЗ 1. CUB-200-2011

Классификация 200 видов птиц на датасете [CUB-200-2011](https://www.kaggle.com/datasets/coolerextreme/cub-200-2011).

Обучены три архитектуры: ResNet-50, EfficientNet-B7 и EfficientNetV2-S. Для каждой проверены итеративная разморозка слоёв с адаптивным lr, итеративная аугментация и псевдолейблинг. Техники добавляются по очереди: baseline, unfreeze, augment, pseudo. Каждый режим обучен на трёх сидах, результаты усреднены.

[Решение](hw1_iterative_training/hw1_cub200.ipynb)

## Запуск

Python 3.12

```bash
pip install -r requirements.txt
```

```bash
jupyter lab hw1_iterative_training/hw1_cub200.ipynb
```

Датасет скачивается внутри ноутбука через `kagglehub`. На Kaggle ноутбук берёт его из `/kaggle/input`, если он подключён как input.
