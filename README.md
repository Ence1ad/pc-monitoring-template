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
3. Create dir for metric data:
   ```bash
   mkdir "metrics_containers_data"
   ```
4. For starting containers use docker compose command:
   ```bash
   docker compose -f docker-compose.yml up -d
   ```
5. For stop and delete containers use the command:
    ```bash
   docker compose -f docker-compose.yml down -v
   ```
6. To receive an alert notification from alertmanager, set up an email notification configs. Open the alertmanager.yml and enter your email credentials:
   ```yml
       email_configs:
        - to: '<login>gmail.com' # Enter the gmail login that will receive alert notifications
          from: '<login>@gmail.com' # Enter the gmail login that will send alert notifications
          smarthost: smtp.gmail.com:587
          auth_username: '<login>@gmail.com' # Enter the gmail login that will send alert notifications
          auth_identity: '<login>@gmail.com' # Enter the gmail login that will send alert notifications
          auth_password: 'google-app-password' # if you are using gmail create google app password -> https://support.google.com/accounts/answer/185833?hl=en
          send_resolved: true
   ```