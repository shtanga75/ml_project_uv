# Ml_project_uv

##### Структура проекта

ml_project_uv/
├── app/

│   └── main.py

├── requirements_ML.txt

├── requirements_service.txt 

├── requirements_jupyter.txt

├── pyproject.toml

├── .gitignore

├── README.md

└── .python-version

## Шаги по установке

0. ### Установка UV через pip

   ```
   pip install uv
   ```

   <img src="screens\UV1.jpg" alt="UV1" style="zoom:67%;" />

1.  ### Создание папки проекта и виртуального окружения

```
mkdir ml_project_uv
cd ml_project
```

2.	### Создайте окружение
	
	```
	uv init
	mkdir app
	```
	
	<img src="screens\UV2.jpg" alt="UV2" style="zoom: 80%;" />
	
	<img src="screens\UV3.jpg" alt="UV3" style="zoom:67%;" />
	
3.	### Установите зависимости
```
pip install -r requirements_ML.txt
pip install -r requirements_service.txt
pip install -r requirements_jupyter.txt
```
<img src="screens\UV4.jpg" alt="UV3" style="zoom:67%;" />

Проверка установленных пакетов

```
pip list
```

​	<img src="screens\UV5.jpg" alt="UV3" style="zoom:67%;" />

<img src="screens\UV6.jpg" alt="UV6" style="zoom: 80%;" />




4. ### git и github
---


1. ##### установка git https://git-scm.com/download/win
#####    2. Создание репозитория на GitHub

3. ##### Инициализация Git в папке project

4. ##### Проверка файла .gitignore. 

​	Убедитесь, что файл .gitignore создан и содержит:".venv/"

#####    5. Добавление файлов в репозиторий

Проверьте статус репозитория: 
```		
git status
```
 Добавьте все файлы (кроме исключенных в .gitignore): 
```
git add .
```

<img src="screens\git.jpg" alt="git" style="zoom:67%;" />


7. ##### Создание коммита
```
git commit -m "ML_project setup with venv"
```

<img src="screens\git2.jpg" alt="git2" style="zoom:67%;" />


8. ##### Подключение к GitHub репозиторию

```
git remote add origin https://github.com/shtanga75/ml_project_uv.git
```

Проверьте подключение:
```
git remote -v
```

<img src="screens\git3.jpg" alt="git3" style="zoom:67%;" />


9. Загрузка кода на GitHub в cmd

```
git push -u origin main
```

​	либо через GitHub Desktop<img src="screens\git4.jpg" alt="git4" style="zoom:67%;" />

------


​			

5. 	### FastAPI-приложение

	Создайте папку "app" и файл "main.py":

```
    from fastapi import FastAPI

	app = FastAPI()

	@app.get("/ping")
	def ping():
		return {"status": "ok"}
```

<img src="screens\8.jpg" alt="8" style="zoom: 67%;" />

<img src="screens\9.jpg" alt="9" style="zoom:67%;" />

Запуск:

```
uv run uvicorn app.main:app --reload
```
<img src="screens\UV7.jpg" alt="UV7" style="zoom:67%;" />

Откройте в браузере: http://127.0.0.1:8000/ping

<img src="screens\UV8.jpg" alt="UV8" style="zoom:67%;" />
