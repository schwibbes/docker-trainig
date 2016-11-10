FROM openjdk:8
#FROM frolvlad/alpine-oraclejdk8
WORKDIR /work
ADD http://repo1.maven.org/maven2/org/clojure/clojure/1.8.0/clojure-1.8.0.zip /work/
RUN unzip clojure-1.8.0.zip && rm clojure-1.8.0.zip

#CMD ["/bin/sh"]
CMD ["java","-cp","clojure-1.8.0/clojure-1.8.0.jar","clojure.main"]
