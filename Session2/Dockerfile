FROM alpine:3.9

LABEL maintainer="kalterman89@gmail.com"

RUN apk update && apk add python3

RUN pip3 install --upgrade pip && \
    pip3 install Click==7.0 && \
    pip3 install Flask==1.0.2 && \
    pip3 install itsdangerous==1.1.0 && \
    pip3 install Jinja2==2.10 && \
    pip3 install MarkupSafe==1.1.1 && \
    pip3 install Werkzeug==0.14.1

COPY . /src

WORKDIR /src

EXPOSE 5000

ENTRYPOINT ["python3", "./app.py"]