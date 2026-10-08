\# Task 2 - Jenkins CI/CD Pipeline



\## Project Overview



This project demonstrates a simple CI/CD pipeline using Jenkins and Docker.



The pipeline automatically builds, tests, and deploys a simple web application whenever changes are pushed to the GitHub repository.



\## Tools Used



\- Jenkins

\- Docker

\- Git

\- GitHub

\- Nginx



\## Project Structure



```text

task-2-jenkins-pipeline/

├── index.html

├── Dockerfile

├── Jenkinsfile

└── README.md





Application



The application is a simple HTML page that displays:



Hello from Jenkins CI/CD Pipeline!



Jenkins Pipeline Stages

1\. Build



Jenkins builds a Docker image from the Dockerfile.



2\. Test



Jenkins verifies that the Docker image was successfully created.



3\. Deploy



Jenkins stops and removes the previous container and starts a new container using the latest Docker image.



Pipeline Flow

Developer

&#x20;   |

&#x20;   v

GitHub Repository

&#x20;   |

&#x20;   v

Jenkins

&#x20;   |

&#x20;   +---- Build

&#x20;   |

&#x20;   +---- Test

&#x20;   |

&#x20;   +---- Deploy

&#x20;   |

&#x20;   v

Docker Container

&#x20;   |

&#x20;   v

Web Application

Docker



The application uses Nginx as the web server.



The Docker container exposes port 80 internally and is mapped to port 8081 on the host.



Application URL:



http://localhost:8081



Jenkins Configuration

Pipeline type: Pipeline

Pipeline definition: Pipeline script from SCM

Source: GitHub

Branch: main

Trigger: Poll SCM

Polling schedule: Every 5 minutes

Result



The Jenkins pipeline completed successfully with Build, Test, and Deploy stages.



The deployed application was successfully accessed through:



http://localhost:8081



Learning Outcome



This project demonstrates the basic implementation of CI/CD using Jenkins and Docker, including automated build, testing, and deployment.

