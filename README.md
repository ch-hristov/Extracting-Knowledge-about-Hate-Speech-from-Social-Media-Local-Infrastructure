# Extracting Knowledge About Hate Speech from Social Media - Docker Infastructure
This project uses Social Media sites such as Twitter to extract knowledge about the usage of Hate Speech online.

The system is developed in Java using the Spring framework, running on Amazon Web Services (AWS) and backed by a PostgreSQL database feeding data into Grafana for monitoring and visualisation.  

The full system is available online at www.suskins.co.uk.
## Getting Started 

### Prerequisites
Software:
* Java 8
* Maven
* Docker
* Docker Compose

### Installing

#### Starting Docker Infrastructure

This repository contains the docker infrastructure required to run the project.

This includes:
* Postgres (Port 5432)
* Grafana (Port 3000)

```
git clone https://cseegit.essex.ac.uk/bs16746/CE301-Human-Rights-Social-Media.git
cd CE301-Human-Rights-Social-Media
docker-compose -f docker-compose.yml up
```

[Localhost Grafana](http://localhost:3000/)

#### Starting Java Service
This [repository](https://cseegit.essex.ac.uk/ce301/suskins_b/capstone_project) contains the Java project.

Running the following command in the project root will build the project Jar and then run it.

```
git clone https://cseegit.essex.ac.uk/ce301/suskins_b/capstone_project.git
cd capstone_project
mvn clean install
java -jar suskins-hrvsm-api-app/target/suskins-hrvsm-api-app-develop-SNAPSHOT.jar
```

### Running Tests
Running the following command in the project root will run all of the Groovy Spock tests.

```
mvn test
```

### Versioning Strategy
Using Semantic Versioning:

Given a version number MAJOR.MINOR.PATCH, increment the:

    MAJOR version when you make incompatible API changes,
    MINOR version when you add functionality in a backwards-compatible manner, and
    PATCH version when you make backwards-compatible bug fixes.

My Minimum Viable Product is tagged as 1.0.0

### Version History
1.0.0 Initial Release | Twitter Integration | Grafana Visualisation | Hate Speech Trained Classifier. - 08/12/2018.

2.0.0 Reworked API | Control Interface | Retrained Hate Speech Model. - 23/01/2019.

2.1.0 Refactor to Hate Speech from Human Rights | Confidence Measure | Improved Control Interface | Improved Classifier. - 10/4/2019

## Authors
* Ben Suskins 

## References
* [Twitter Hosebird Client](https://github.com/twitter/hbc)
* [Spring Framework](https://spring.io/)
* [Apache Maven](https://maven.apache.org/)
* [Stanford CoreNLP](https://stanfordnlp.github.io/CoreNLP/)
* [Grafana](https://grafana.com/)
* [Hate Speech Training Data](https://github.com/t-davidson/hate-speech-and-offensive-language)
* [Sentiment 140 Training Data](http://help.sentiment140.com/for-students/)