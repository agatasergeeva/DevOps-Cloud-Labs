## Лабораторная работа №2

Для начала напишем “плохой” Dockerfile, в котором есть три “bad practices” по написанию докерфайлов: 
```
FROM python:latest
COPY . /app
CMD ["python", "/app/app.py"]
```
Описание этих “bad practices”:
1. **Использование latest**: 
Это «bad practices», так как version latest может измениться со временем и привести к неожиданному поведению приложения. 
