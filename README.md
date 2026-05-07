# mi-proyecto

En esta actividad, el estudiante implementará un flujo básico de DevOps utilizando Git y GitHub, simulando el desarrollo, mantenimiento y despliegue de un proyecto web estático. 



graph TD
    subgraph "CI/CD Pipeline (GitHub & DevOps)"
        A[GitHub Repository: main/develop] -->|Push / PR| B(GitHub Actions)
        B -->|Build| C[Docker Containers]
        B -->|Deploy| D[AWS CloudFormation]
    end

    subgraph "AWS Infrastructure (Management & Logic)"
        D --> E[AWS Cloud9 / EC2]
        E -->|Python + Boto3| F{Logic Layer}
        F -->|Concurrencia: 10| G[AWS Lambda]
        G -->|Rollback Logic| F
    end

    subgraph "Data Layer (Lambda Architecture)"
        F -->|Batch Layer| H[(Amazon S3)]
        F -->|Speed/Serving Layer| I[(Amazon DynamoDB)]
        
        H -->|Lifecycle Rules| J[Auto-Deletion/Archive]
        H -->|Security| K[SSE-S3 Encryption & Versioning]
    end

    subgraph "Security Perimeter"
        L[Security Groups] -->|Allow My IP Only| E
        L -->|Restricted Access| G
        M[LabRole] -.->|Temporary Credentials| F
    end
