FROM python:3.10-slim

WORKDIR /app

COPY Pipfile ./
# Convert Pipfile requirements or copy app files
COPY . /app

RUN pip install --no-cache-dir --upgrade pip && \
    pip install flask flask-cors pytest gunicorn

EXPOSE 5000

CMD ["gunicorn", "-b", "0.0.0.0:5000", "app:app"]
