FROM inthepocket/plantuml-server:latest

# Install fonts
USER root
RUN curl -O -L -J https://www.fontsquirrel.com/fonts/download/fira-sans && \
    unzip fira-sans.zip -d /usr/local/share/fonts && \
    mv "/usr/local/share/fonts/SIL Open Font License.txt" /usr/local/share/fonts/FiraSans-LICENSE.txt && \
    rm -f fira-sans.zip && \
    curl -O -L -J https://www.fontsquirrel.com/fonts/download/fira-mono && \
    unzip fira-mono.zip -d /usr/local/share/fonts && \
    mv "/usr/local/share/fonts/SIL Open Font License.txt" /usr/local/share/fonts/FiraMono-LICENSE.txt && \
    rm -f fira-mono.zip && \
    curl -O -L -J https://www.fontsquirrel.com/fonts/download/fira-code && \
    unzip fira-code.zip -d /usr/local/share/fonts && \
    mv "/usr/local/share/fonts/SIL Open Font License.txt" /usr/local/share/fonts/FiraCode-LICENSE.txt && \
    rm -f fira-code.zip

USER jetty
ENV PLANTUML_PRE_INCLUDE_UML=/var/lib/jetty/resources/styles.plantuml

COPY styles.plantuml /var/lib/jetty/resources
