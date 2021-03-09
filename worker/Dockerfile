FROM maven:3.5-jdk-8-alpine AS builder
COPY ./ ./home/user/worker
WORKDIR /home/user/worker
RUN mvn dependency:resolve
RUN mvn package

FROM openjdk:8-jre-alpine
COPY --from=builder /home/user/worker/target/worker-jar-with-dependencies.jar ./
CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]
