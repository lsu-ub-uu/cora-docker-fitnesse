FROM  openjdk:8-jre-alpine


COPY /fitnesse.jar /fitnesse/
#COPY /fitnesse-standalone.jar /fitnesse/
COPY /FitNesseRoot /fitnesse/FitNesseRoot
COPY /plugins.properties /fitnesse/

WORKDIR /fitnesse
#CMD java -jar /fitnesse/fitnesse-standalone.jar -p 8090 -o -a password.txt
#CMD java -classpath /fitnesse/fitnesse.jar -jar /fitnesse/fitnesse-standalone.jar -p 8090

CMD java -classpath /fitnesse/fitnesse.jar  -DsystemUnderTestUrl="http://therest:8080/therest/" fitnesseMain.FitNesseMain -p 8090


#java -jar fitnesse-standalone.jar -p 8090 -o -a password.txt

#build with:
#maven build

#start on build server with:
#docker run --network=cora-test -p 8190:8090 --name fitnesse-test --link therest-test:therest -d fitnesse

#start on external with:
#docker run --network=cora -p 8290:8090 --name fitnesse --link therest:therest -d fitnesse

