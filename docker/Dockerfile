FROM  openjdk:8-jre-alpine


COPY /fitnesse.jar /fitnesse/
#COPY /fitnesse-standalone.jar /fitnesse/
COPY /FitNesseRoot /fitnesse/FitNesseRoot

WORKDIR /fitnesse
#CMD java -jar /fitnesse/fitnesse-standalone.jar -p 8090 -o -a password.txt
#CMD java -classpath /fitnesse/fitnesse.jar -jar /fitnesse/fitnesse-standalone.jar -p 8090
CMD java -classpath /fitnesse/fitnesse.jar  fitnesseMain.FitNesseMain -p 8090


#java -jar fitnesse-standalone.jar -p 8090 -o -a password.txt

#build with maven build
#start with:
#docker run -p 8090:8090 --name fitnesse --link therest:localhost -d fitnesse