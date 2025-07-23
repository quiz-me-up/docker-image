FROM maven:3.9.10-eclipse-temurin-21
MAINTAINER QuizMeUp <quizmeup.contact@gmail.com>

ARG SETTINGS_XML

# Écrire le contenu de SETTINGS_XML dans le fichier settings.xml
RUN if [ -n "$SETTINGS_XML" ]; then echo "$SETTINGS_XML" > /usr/share/maven/conf/settings.xml; fi