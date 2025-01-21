FROM python:3.9-slim

WORKDIR /app

# Устанавливаем зависимости
COPY requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt

# Копируем все файлы приложения
COPY . /app/

# Устанавливаем переменные окружения
ENV PYTHONUNBUFFERED 1

# Команда для запуска сервера Django
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
