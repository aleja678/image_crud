# Imagen base con OpenJDK 17
FROM eclipse-temurin:17-jdk-alpine

# Establecer el directorio de trabajo dentro del contenedor
WORKDIR /app

VOLUME /tmp

# Copiar el archivo JAR generado por Maven al contenedor
#COPY target/images_galery-0.0.1-SNAPSHOT.jar app.jar

ARG JAR_FILE=target/*.jar
COPY ${JAR_FILE} app.jar

# Exponer el puerto 9090 (el puerto donde corre Spring Boot)
EXPOSE 8080

# Comando para ejecutar la aplicación
CMD ["java", "-jar", "app.jar"]