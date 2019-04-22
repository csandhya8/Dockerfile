FROM java:8
VOLUME /tmp
EXPOSE 8080
#ADD http://nexusrepo-nexus.cloudapps-5957.oslab.opentlc.com/content/repositories/releases/org/mong-ci/main/mong-jar/2.234/mong-jar-2.234.jar app.jar
ADD /home/autodeployvm/worker/4/s/my-app/target/my-app-1.0-SNAPSHOT.jar app.jar
RUN bash -c 'touch /app.jar'
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]

FROM java:8
VOLUME /tmp
EXPOSE 8081
#ADD http://nexusrepo-nexus.cloudapps-5957.oslab.opentlc.com/content/repositories/releases/org/mong-ci/main/mong-jar/2.234/mong-jar-2.234.jar app.jar
ADD /home/autodeployvm/worker/5/s/target/sampledemo-0.0.1-SNAPSHOT.jar app.jar
RUN bash -c 'touch /app.jar'
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
