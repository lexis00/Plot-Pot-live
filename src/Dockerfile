# Use Java 21 JDK slim image
FROM openjdk:21-jdk-slim

# Set working directory in container
WORKDIR /app

# Copy all project files into the container
COPY . .

# Compile Java source files
RUN javac -cp lib/json.jar com/plotnpot/*.java -d .

# Expose the port your server will run on
EXPOSE 8080

# Command to run your server
CMD ["java", "-cp", ".:lib/json.jar", "com.plotnpot.AppServer"]
