Dockerfile
=============
- Referenz: https://docs.docker.com/engine/reference/builder/
- Best Practices: https://docs.docker.com/engine/userguide/eng-image/dockerfile_best-practices

## Basis image
```
FROM ubuntu
FROM <image>:<tag>
```

## Dateien in den Container bringen
Im Zweifelsfall **COPY** verwenden
```
ADD https://github.com/jekyll/docker/blob/master/repos/jekyll/opts.yml /tmp
COPY test.png /tmp
COPY ["test a.png", "test b.png" "/tmp"]
```

## Befehl im Container ausführen
Häufig für *apt-get update && apt-get install*
```
RUN echo "abc" > /tmp/echo.txt
RUN ["/bin/bash", "-c", "echo hello"]
```

## Basis-Kommando des Containers festlegen
Zwei Konzepte **CMD** und **ENTRYPOINT**
- CMD
    ```
    CMD ["ping", "localhost"]
    ```

- ENTRYPOINT
    ```
    ENTRYPOINT ["ping", "localhost"]
    ```

- Kombinierbar
    ```
    FROM ubuntu
    ENTRYPOINT ["ping", "-c", "3"]
    CMD ["localhost"]
    ```

## Umgebungsvariablen
```
ENV JAVA_HOME=/usr/lib/jvm/
```

# User
```
USER root
```

# Arbeitsverzeichnis
```
WORKDIR /var/lib/jenkins
```

# Healthcheck
```
HEALTHCHECK --interval=5m --timeout=3s \
  CMD curl -f http://localhost/ || exit 1
```
