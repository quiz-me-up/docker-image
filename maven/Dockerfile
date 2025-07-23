FROM maven:3.9.10-eclipse-temurin-21
MAINTAINER QuizMeUp <quizmeup.contact@gmail.com>

ARG SETTINGS_XML_PATH

# Créer le répertoire .m2 s'il n'existe pas
RUN mkdir -p /root/.m2

# Copier le fichier settings.xml si il existe dans le contexte de build
COPY settings.xml* /root/.m2/

# Renommer le fichier si nécessaire (au cas où il aurait un nom différent)
RUN if [ -f "/root/.m2/settings.xml" ]; then \
        echo "Settings.xml found and configured"; \
    else \
        echo "No settings.xml provided, using Maven defaults"; \
    fi
