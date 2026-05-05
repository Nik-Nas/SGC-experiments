# SG-experiments

Репозиторий содержит практические эксперименты к индивидуальному разбору статьи  
**«Simplifying Graph Convolutional Networks»** (Wu et al., ICML 2019).

## Содержание

- `experiment1_sgc_ablation_K.ipynb` – абляция числа шагов распространения *K* (Cora), сравнение с GCN и линейным бейзлайном.
- `experiment2_lowpass_visualization.ipynb` – визуализация низкочастотного фильтра SGC (Figure 2 статьи).
- `experiment3_model_comparison.ipynb` – сравнение SGC, MLP и линейной модели (важность графа).
- `experiment4_heterophily.ipynb` – тест SGC на гетерофильных датасетах (WebKB: Texas, Wisconsin, Cornell).

Все эксперименты самодостаточны, выполняются на CPU и не требуют дополнительных данных.

## Запуск

1. Клонируйте репозиторий:
   git clone https://github.com/your-username/sgc-paper-experiments.git
   cd sgc-paper-experiments
2. Установите зависимости (рекомендуется окружение conda или venv):
   pip install torch torch-geometric scikit-learn numpy scipy matplotlib
3. Откройте нужный ноутбук в Jupyter:
   jupyter notebook
   или запустите в Google Colab, заменив в URL github.com на colab.research.google.com/github.

## Ожидаемые результаты

- Ноутбук 1: график точности SGC при *K* = 0..4, таблица результатов.
- Ноутбук 2: спектральный фильтр и спектр признака (аналог Figure 2 статьи).
- Ноутбук 3: таблица сравнения трёх моделей на Cora.
- Ноутбук 4: сводная таблица точности SGC / GCN / GAT на гетерофильных графах.

Время выполнения первых 3 ноутбуков не превышает нескольких минут на современном CPU. 
В ноутбуке 4 стабильно наблюдались теоретико-практические противоречия, разрешившиеся только на больших датасетах.

## Ссылка на статью

- [Simplifying Graph Convolutional Networks](https://proceedings.mlr.press/v97/wu19e.html)
- Официальный код авторов: [Tiiiger/SGC](https://github.com/Tiiiger/SGC)

## Авторство

Эксперименты выполнены в рамках учебного задания по дисциплине «Архитектура моделей глубокого обучения».