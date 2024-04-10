FROM python:3.12.3-alpine

COPY src/main.py /app/
COPY requirements.txt /app/

RUN adduser simpleuser -D && chown -R simpleuser /app

USER simpleuser

WORKDIR /app

RUN pip install -r requirements.txt \
    && mkdir data

EXPOSE 8000

ENTRYPOINT ["python3", "main.py"]