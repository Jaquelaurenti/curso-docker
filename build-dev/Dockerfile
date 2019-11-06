FROM python:3.6
LABEL maintainer 'Servidor com Python'

RUN useradd www && \ 
    mkdir /app && \
    mkdir /log && \ 
    chown www /log


# Manter a parte mais estável, pois o cash sera reaproveitavel 
# Volume criado para que atraves de um container seja possivel acessar os logs de outro container
# Dockefile e o descritor que sera iniciado para a criacao das imagens



USER www
VOLUME /log
WORKDIR /app
EXPOSE 8000

ENTRYPOINT ["/usr/local/bin/python"]
CMD ["run.py"]

# o Entrypoint e o processo que sera executado