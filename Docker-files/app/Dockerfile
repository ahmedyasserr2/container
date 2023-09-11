From openjdk:11 AS BUILD_IMAGE
Run apt update && apt install maven -y 
Run git clone https://github.com/ahmedyasserr2/vprofile-project.git
Run cd vprofile-project && git checkout docker && mvn install

From tomcat:9-jre11
Label "Project"="Vprofile"
Label "Author"="Yasser" 
Run rm -rf /usr/local/tomcat/webapps/*
COPY --from=BUILD_IMAGE vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war


EXPOSE 8080
CMD ["catalina.sh", "run"]