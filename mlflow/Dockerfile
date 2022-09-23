FROM continuumio/miniconda3:latest

RUN apt-get update && apt-get install -y git
RUN pip install mlflow psycopg2-binary pymysql boto3

WORKDIR /app
RUN cd /app && git clone https://github.com/mlflow/mlflow-example.git

COPY wait-for-it.sh wait-for-it.sh
RUN chmod +x wait-for-it.sh
