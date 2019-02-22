FROM sogis/java:8
LABEL maintainer="Stefan Ziegler, stefan.ziegler@bd.so.ch" description="Tomee Plume"
ENV ARCHIVE apache-tomee-plume-8.0.0-M2
ENV INSTALL_DIR /opt
ENV SERVER_HOME ${INSTALL_DIR}/${ARCHIVE}
RUN curl -o ${SERVER_HOME}.zip -L http://repo.maven.apache.org/maven2/org/apache/tomee/apache-tomee/8.0.0-M2/apache-tomee-8.0.0-M2-plume.zip \
    && unzip ${SERVER_HOME}.zip -d /opt \
    && rm ${SERVER_HOME}.zip
ENV DEPLOYMENT_DIR ${SERVER_HOME}/webapps/
ENTRYPOINT ${SERVER_HOME}/bin/catalina.sh run
EXPOSE 8080



