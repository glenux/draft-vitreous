FROM crystallang/crystal:0.34

COPY . /app

WORKDIR /app

RUN shards install \
 && crystal build -o vitreous src/main.cr


