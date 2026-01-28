# MATF-RVTECH-AWSCLOUD-2025
Projekat za stručni kurs Razvoj aplikacija u oblaku na Matematičkom fakultetu

## Koraci pre pokretanja:

### 1. Zaustavi postojeće kontejnere (ako ima nekih): 
    docker compose down -v 
### 2. Pokreni LocalStack: 
    docker compose up -d
### 3. Instaliramo serverless dependencije: 
    npm install
### 4. Deploy Serverless infrastrukture: 
    npx serverless deploy
### 5. Konfiguracija API_ID (da bismo ga videli):  
    awslocal apigateway get-rest-apis --query 'items[0].id' --output text
### 6. Potom u index.html za API_ID stavimo dobijenu vrednost
### 7. Deploy frontend na S3: 
    npm run deploy-frontend-fixed-bucket
### 8. Pristup aplikaciji: 
**http://punjaci-website.s3-website.localhost.localstack.cloud:4566/**