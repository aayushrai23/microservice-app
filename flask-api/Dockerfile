FROM python:3.9-alpine

WORKDIR /app
COPY requirements.txt .

RUN apk add --no-cache \
    build-base \
    python3-dev \
    libffi-dev \
    openssl-dev \
    && pip install --no-cache-dir -r requirements.txt

COPY . .

ENV PORT=5000
EXPOSE 5000

CMD ["python", "app.py"]
