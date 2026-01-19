FROM python:3.12-slim
WORKDIR /app
COPY python-service/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY python-service .
CMD ["python","app.py"]
