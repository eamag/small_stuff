В данной папке содержится простое решение задачи B. 

Идея решения следующая: в качестве ответа выбирается целое предложение из параграфа, такое что оно сильнее всего пересекается со словами из вопроса.  

## Инструкция по созданию решения:

1. Склонируйте репозиторий себе на компьютер
2. Зайдите в папке taskB
3. Выполните команду: `python3 create_submission.py -p simple-baseline/predict.py -o output_simple.zip` (из файла `create_submission_simple.sh`)
4. Создастся архив: output_simple.zip, который можно отправить в систему


## Инструкция по проверке решения:

1. Склонируйте репозиторий себе на компьютер
2. Зайдите в папку taskB
3. Положите в папку taskB файл с данными (`train.csv`)
4. Выполните `python3 split_train.py train.csv`, в результате появится два файла: `train_without_validate.csv`, `validate.csv`. Первый будем в будущем использовать для обучения, второй для проверка работы моделей.
5. Выполните `python3 check_solution.py -t docker --submission_folder ml-baseline --data_file validate.csv`, в результате вы увидите в конце строчку вида: `{'f1': 0.3361121166011774}`
6. Теперь можете добавлять и улучшать модель.