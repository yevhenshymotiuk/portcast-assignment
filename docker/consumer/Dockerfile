FROM python:3.6

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

WORKDIR /home/consumer

COPY . /home/consumer/

RUN apt-get update -y
RUN apt-get upgrade -y

RUN apt-get install -y chromium-driver chromium

# Install poetry and its dependencies
RUN pip install poetry \
    && poetry config virtualenvs.create false \
    && poetry install --no-dev
