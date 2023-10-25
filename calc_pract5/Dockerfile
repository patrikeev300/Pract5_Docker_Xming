
FROM ubuntu:latest

# Устанавливаем необходимые пакеты для графического интерфейса и Java
RUN apt-get update && apt-get install -y \
    openjdk-11-jdk \
    x11-apps \
    xauth \
    && rm -rf /var/lib/apt/lists/*


ENV DISPLAY=:0

# Копируем файл calc.jar внутрь контейнера
COPY calc.jar /usr/src/app/

# Запускаем приложение при старте контейнера
CMD ["java", "-jar", "/usr/src/app/calc.jar"]