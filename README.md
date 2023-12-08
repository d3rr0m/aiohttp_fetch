# Курс Data Engineer от slurm.io
# Unit 2. Python и терминал
После установки пакета `SlurmDE` появится команда `start_fetching`, запустив которую будут получены данные из сервиса API `http://5.159.103.105:4000/api/v1/logs` и сохранене в файл формата CSV. 

## Сборка пакета
#### Python3 должен быть уже установлен.
1. Клоинруйте проект командой и перейдите в директорию проекта
 ```bash
git clone git@gitlab.slurm.io:data_engineer_s058356/data_engineer_review.git
```
Перейдите в папку проекта:
```bash
cd data_engineer_review
```
2. Создайте виртуальное окружение:
```bash
python3 -m venv venv
```
3. Активируйте только что созданное виртуальное окружение.
```bash
$ source venv/bin/activate
```
4. Запустите сборку пакета командой:
```bash
$ python3 setup.py sdist
```
5. После сборки пакет его необходимо установить. Выполнить это можно командой:
```bash
$ pip install dist/SlurmDE-0.0.1.tar.gz
```
## Запуск
Запуск можно выполнить командой `start_fetching`. Итоговый csv файл создан в директории запуска команды `start_fetching`
### Необязательные параметры
```
-s - Номер стартовой страницы с которой начнется выборка данных. Значение по умолчанию - 1.
```
```
-e - Номер последней страницы на которой выборка данных закончится. Значение по умолчанию - масимально доступное кол-во страниц.
```
```
-t - Количевство одновременно работающих asyncio.task. Рекомендуемое значение - не более 7. Значение по умолчанию - 5.
```
```
-f - Имя файла, куда будет сохранен датасет. Значение по умолчанию - customs_data.csv
```
