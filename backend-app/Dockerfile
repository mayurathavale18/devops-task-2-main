FROM python:3.12-alpine

WORKDIR /app

RUN apk add python3-dev gcc libc-dev libffi-dev

COPY requirements.txt .

RUN pip install --no-cache-dir --upgrade -r requirements.txt

COPY . .

EXPOSE 9000

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "9000"]