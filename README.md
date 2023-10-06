# pc-monitoring-template
Template for monitoring PC


## How to use

1. Clone the repository: 
   ```bash 
   git clone https://github.com/Ence1ad/pc-monitoring-template.git 
   ```
2. Navigate to the project directory: 
   ```bash 
   cd pc-monitoring-template 
   ```
3. For starting containers use docker compose command:
   ```bash
   docker compose -f docker-compose.yml up -d
   ```
4. For stop and delete containers use the command:
    ```bash
   docker compose -f docker-compose.yml down -v
   ```