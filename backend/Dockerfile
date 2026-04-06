FROM python:3.9-slim
# Устанавливаем рабочую директорию
WORKDIR /app

RUN pip install --upgrade pip
# Копируем зависимости и устанавливаем их
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
# Копируем остальные файлы приложения
COPY . .
# Команда для запуска приложения
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]