location /gateway/onboarding/ {
    # Local development - proxy to localhost
    proxy_pass http://localhost:2025/;
    # Dev server
    #proxy_pass http://172.18.4.220:2025/;
    
    proxy_set_header Host $host;
    proxy_set_header X-Real-IP $remote_addr;
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header X-Forwarded-Proto $scheme;
}


# Server Configuration
PORT=2025
BASE_PATH="/api/v1/onboarding"

# Database Pool Settings
DB_MAX_CONNECTIONS=10
DB_MIN_CONNECTIONS=0
IDLE_TIME=5000  # 5 seconds
ACQUIRE_TIME=10000  # 10 seconds

# IMT Config Read (for country, currency, partner, user management)
IMT_CONFIG_READ_HOSTNAME='localhost'
IMT_CONFIG_READ_USER='postgres'
IMT_CONFIG_READ_PASSWORD='root'
IMT_CONFIG_READ_PORT='5432'
IMT_CONFIG_READ_DATABASE='terra_config_db'

# IMT Config Write (main application database)
IMT_CONFIG_WRITE_HOSTNAME='localhost'
IMT_CONFIG_WRITE_USER='postgres'
IMT_CONFIG_WRITE_PASSWORD='root'
IMT_CONFIG_WRITE_PORT='5432'
IMT_CONFIG_WRITE_DATABASE='terra_config_db'

# Ledger Database
IMT_CONFIG_WRITE_HOSTNAME_LEDGER='localhost'
IMT_CONFIG_WRITE_USER_LEDGER='postgres'
IMT_CONFIG_WRITE_PASSWORD_LEDGER='root'
IMT_CONFIG_WRITE_PORT_LEDGER='5432'
IMT_CONFIG_WRITE_DATABASE_LEDGER='terra_ledger_db'

# Routing Table Database
IMT_CONFIG_WRITE_HOSTNAME_ROUTE='localhost'
IMT_CONFIG_WRITE_USER_ROUTE='postgres'
IMT_CONFIG_WRITE_PASSWORD_ROUTE='root'
IMT_CONFIG_WRITE_PORT_ROUTE='5432'
IMT_CONFIG_WRITE_DATABASE_ROUTE='terra_route_db'

# Fee Module Database Handler
FEE_MODULE_DATA_HANDLER_HOSTNAME='localhost'
FEE_MODULE_DATA_HANDLER_USER='postgres'
FEE_MODULE_DATA_HANDLER_PASSWORD='root'
FEE_MODULE_DATA_HANDLER_PORT='5432'
FEE_MODULE_DATA_HANDLER_DATABASE='terra_fee_db'

# Security & Encryption
SECRET_KEY='neolotex'
TOKEN_PRIVATE_KEY='your_token_private_key_here'
BACKEND_SECRET_CRYPTO_KEY="FoCKvdLslUuB4y3EZlKate7XGottHski1LmyqJHvUhs="
TOKEN_EXPIRE_TIME='24h'

# Email Configuration
EMAIL_SERVICE='gmail'
EMAIL_HOST='smtp.gmail.com'
EMAIL_PORT='587'
EMAIL_FROM_ADDRESS='your-email@example.com'
EMAIL_USER_ID='your-email@example.com'
EMAIL_USER_PASSWORD='your-app-password'
SEND_EMAIL_USING_PEARL='No'
OTP_EXPIRATION_TIME_IN_MINUTE='5'

# Perl Configuration (if needed)
PERL_EXECUTABLE_PATH='/usr/bin/perl'
PERL_SCRIPT_PATH='/prd/sendEmail.pl'

# Logging Configuration
LOGGER_SIZE='1023k'
PRINT_CONSOLE='True'
LOGS_FOLDER='logsFolder'
LOGGER_LEVEL=3  # 0=error, 1=warn, 2=info, 3=debug

# Environment Configuration
RUNNING_ENVIRONMENT='Dev'
FROENTEND_URL='http://localhost:3001'
ISLINUX=False

# File Upload Paths
PARTNER_IMAGE='partner_images'
UPDATED_PARTNER_IMAGE='partner_images/updated_partner_images'
USER_IMAGE='user_images'
UPDATED_USER_IMAGE='user_images/updated_user_images'
LOCAL_PATH_NEW='/backend/email_Attachments_files'
UPLOADED_FEE_DOCUMENT_PATH='uploaded_documnets/fee_documents'

# Microsoft Azure AD Configuration
MICROSOFT_LOGIN_URL='https://graph.microsoft.com/v1.0/me'
MS_CLIENT_ID='your-client-id'
MS_TENANT_ID='your-tenant-id'
MS_REDIRECT_URI='http://localhost:2025/api/v1/onboarding/microsoftLogin'
MS_SECRET_ID='your-client-secret'

# Google OAuth
GOOGLE_CLIENT_ID='your-google-client-id'

# External Service URLs
USER_MANAGEMENT_SERVER='http://localhost:8080'
NOTIFICATION_BASE_URL='http://localhost:8001/api/v1/notification'
IGNORE_NOTIFICATION_ERROR=true

# Redis Configuration (if used)
REDIS_URL='redis://localhost:6379/0'

# CORS Configuration
CORS_ALLOWED_ORIGINS="*"
DISABLE_CORS="yes"
