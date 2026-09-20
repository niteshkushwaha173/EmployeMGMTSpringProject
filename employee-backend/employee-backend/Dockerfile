# Java version pom.xml ki <java.version> se match honi chahiye (17 / 21 / 25)
ARG JAVA_VERSION=25

# ---- Build stage ----
FROM maven:3.9-eclipse-temurin-${JAVA_VERSION} AS build
WORKDIR /app

# Pehle sirf pom.xml copy karo taaki dependencies ka Docker layer cache ho
COPY pom.xml .
RUN mvn dependency:go-offline -B

# Ab source copy karke build karo
COPY src ./src
RUN mvn clean package -DskipTests -B

# ---- Run stage ----
FROM eclipse-temurin:${JAVA_VERSION}-jre
WORKDIR /app

COPY --from=build /app/target/*.jar app.jar

# Port: Render PORT deta hai aur application.properties mein
# server.port=${PORT:${SERVER_PORT:8284}} hai.
# Yahan ENV SERVER_PORT set mat karo, wo properties file ko override kar deta hai.
EXPOSE 8284

# MaxRAMPercentage: free tier ki chhoti memory mein app crash na ho
ENTRYPOINT ["java", "-XX:MaxRAMPercentage=75", "-jar", "app.jar"]