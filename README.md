front end env

VITE_APP_BASE_URL = "/"
#TOPS base URL
# VITE_APP_API_ENDPOINT =
VITE_APP_API_ENDPOINT = "http://172.18.4.220"
#VITE_APP_API_ENDPOINT = "http://localhost"
VITE_APP_MOCK_API_VERSION = ''
# VITE_APP_MOCK_API_VERSION = '/v3'
VITE_APP_SECRET_CRYPTO_KEY = 'FoCKvdLslUuB4y3EZlKate7XGottHski1LmyqJHvUhs='
VITE_APP_BACKEND_SECRET_CRYPTO_KEY = "FoCKvdLslUuB4y3EZlKate7XGottHski1LmyqJHvUhs="
VITE_BASE_NAME = '/'
VITE_APP_EXISTING_BASE_URL = "/api/"
VITE_APP_AUTH_GATEWAY =  'auth'
VITE_APP_ONBOARDING_GATEWAY ='onboarding/api/v1'
VITE_APP_USER_GATEWAY = "user"
VITE_APP_PMS_GATEWAY="pms"

# VITE_APP_MS_CLIENT_ID =
VITE_APP_MS_CLIENT_ID=
VITE_APP_MS_AUTHORITY =
VITE_APP_MS_REDIRECT_URI=

VITE_APP_USER_MANAGEMENT_ENCRYPTION = true
VITE_APP_AUTO_SIGN_OUT_TIME_IN_MINUTE = 15
VITE_APP_CRYPTO_SAFE_URL_ENCODING_ENABLED = false

VITE_GATEWAY_SERVER_URL="http://172.18.4.220:8081"

PORT=3001
VITE_REACT_APP_VERSION=R001.3.0.0.125
VITE_REACT_APP_DATE=08-Jan-2026
nginx config 
location /gateway/onboarding/ {
    #rewrite ^/(.*) /$1 break;
    proxy_pass http://172.18.4.220:2025/;
    # proxy_pass http://localhost:2025/;
    proxy_set_header Host $host;
    proxy_set_header X-Real-IP $remote_addr;
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header X-Forwarded-Proto $scheme;
}
example
location /gateway/pms/proposal {
    #rewrite ^/(.*) /$1 break;
    proxy_pass http://localhost:9999/api/v1/pms/proposal;
    #proxy_pass http://172.18.4.220:1028/v1/treasury;
    proxy_set_header Host $host;
    proxy_set_header X-Real-IP $remote_addr;
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header X-Forwarded-Proto $scheme;
}
env sample of onboarding
#DB Pool Settings
# Max connections in pool
DB_MAX_CONNECTIONS=5
# (OPTIONAL, DEFAULT=0) Min connections in pool
DB_MIN_CONNECTIONS=
# pool disconnect time out on idle
IDLE_TIME=20000
# (OPTIONAL) pool reconnecting time out
ACQUIRE_TIME=

#IMT_CONFIG_READ -> used in fee module (feeplan dbservices and common db services.(old comment "COUNTRY, CURRENCY AND PARTNER, usermgmt")
IMT_CONFIG_READ_HOSTNAME=
IMT_CONFIG_READ_USER=
IMT_CONFIG_READ_PASSWORD=
IMT_CONFIG_READ_PORT=
IMT_CONFIG_READ_DATABASE=

#this one using in db.js entire application using this
#this is using in feeplanDbServices
IMT_CONFIG_WRITE_HOSTNAME=
IMT_CONFIG_WRITE_USER=
IMT_CONFIG_WRITE_PASSWORD=
IMT_CONFIG_WRITE_PORT=
IMT_CONFIG_WRITE_DATABASE=

#Only ledger is accessed using this handle
IMT_CONFIG_WRITE_HOSTNAME_LEDGER=
IMT_CONFIG_WRITE_USER_LEDGER=
IMT_CONFIG_WRITE_PASSWORD_LEDGER=
IMT_CONFIG_WRITE_PORT_LEDGER=
IMT_CONFIG_WRITE_DATABASE_LEDGER=

#Only Routing_table is accessed using this handle
IMT_CONFIG_WRITE_HOSTNAME_ROUTE=
IMT_CONFIG_WRITE_USER_ROUTE=
IMT_CONFIG_WRITE_PASSWORD_ROUTE=
IMT_CONFIG_WRITE_PORT_ROUTE=
IMT_CONFIG_WRITE_DATABASE_ROUTE=

#FEE_MODULE_DATA_HANDLER -> (With read and write access to fee module tables)All fee module apis using this handler
FEE_MODULE_DATA_HANDLER_HOSTNAME=
FEE_MODULE_DATA_HANDLER_USER=
FEE_MODULE_DATA_HANDLER_PASSWORD=
FEE_MODULE_DATA_HANDLER_PORT=
FEE_MODULE_DATA_HANDLER_DATABASE=

PORT=8000

EMAIL_SERVICE=
EMAIL_HOST=
EMAIL_PORT=
EMAIL_FROM_ADDRESS=
#Above email id and password is for 'gmail.com'. Below user id and password is for 'sendinblue.com'. Please note the minor difference in id.
EMAIL_USER_ID=
EMAIL_USER_PASSWORD=
PERL_EXECUTABLE_PATH='/usr/bin/perl'
PERL_SCRIPT_PATH='/prd/sendEmail.pl'
#If we have to send email using pearl script use valuefor below variable as 'Yes' else make it 'No'
SEND_EMAIL_USING_PEARL='No'
OTP_EXPIRATION_TIME_IN_MINUTE='5'
FROENTEND_URL=
LOGGER_SIZE='1023k'
#If we need to print console make below varitabl 'True'. If not make it 'False'
PRINT_CONSOLE='True'
LOGS_FOLDER='logsFolder'
SECRET_KEY=
TOKEN_EXPIRE_TIME=
LOGGER_LEVEL=3
# LOGGER_LEVEL 0=error, 1=warn, 2=info, 3=debug

TOKEN_PRIVATE_KEY=
GOOGLE_CLIENT_ID=

LOCAL_PATH_NEW='/backend/email_Attachments_files'
# To send email to actual email id's in production make below variable as 'Prod'.
RUNNING_ENVIRONMENT=
#line 103 to 106 partner and user saved images folder path
PARTNER_IMAGE='partner_images'
UPDATED_PARTNER_IMAGE='partner_images/updated_partner_images'
USER_IMAGE='user_images'
UPDATED_USER_IMAGE='user_images/updated_user_images'
ISLINUX=False
FROENTEND_URL='*'

DB_MAX_CONNECTIONS=10
DB_MIN_CONNECTIONS=0
ACQUIRE_TIME=10000 #30000 = 30 seconds If a connection request cannot be fulfilled within this time limit, Sequelize will throw an error indicating that the connection acquisition has timed out.
IDLE_TIME=5000 #10000 = 10 seconds If a connection remains idle for longer than this duration, Sequelize may close the connection to free up resources

UPLOADED_FEE_DOCUMENT_PATH='uploaded_documnets/fee_documents'
BACKEND_SECRET_CRYPTO_KEY = "FoCKvdLslUuB4y3EZlKate7XGottHski1LmyqJHvUhs="


# ---------------- MS CONFIG ----------------
MICROSOFT_LOGIN_URL='https://graph.microsoft.com/v1.0/me'
MS_CLIENT_ID='{{CLIENT_ID}}'
MS_TENANT_ID='{{TENANT_ID}}'
MS_REDIRECT_URI='http://localhost:<port>/api/v1/app/microsoftLogin'
MS_SECRET_ID='{{CLIENT_SECRET}}'
USER_MANAGEMENT_SERVER=
REDIS_URL='redis://<user>:<password>@<host>:6379/0'








# SQL Injection File
# Country
# Bank
# CSS
# CURRENCY
# FI MAP
# Global Properties
example env of pms

PORT = 9999
BASE_PATH="/api/v1/pms"

SECRET_KEY = 'neolotex'

# config DB write
#IMT_CONFIG_WRITE_HOSTNAME='172.16.1.49'
IMT_CONFIG_WRITE_HOSTNAME='localhost'
IMT_CONFIG_WRITE_USER='postgres'
IMT_CONFIG_WRITE_PASSWORD='root'
IMT_CONFIG_WRITE_PORT='5432'
#IMT_CONFIG_WRITE_DATABASE='IMT_CONFIG_Dev'
IMT_CONFIG_WRITE_DATABASE='terra_config_db'

#FEE_MODULE_DATA_HANDLER -> (With read and write access to fee module tables)All fee module apis using this handler
#FEE_MODULE_DATA_HANDLER_HOSTNAME='172.16.1.49'
FEE_MODULE_DATA_HANDLER_HOSTNAME='localhost'
FEE_MODULE_DATA_HANDLER_USER='postgres'
FEE_MODULE_DATA_HANDLER_PASSWORD='root'
FEE_MODULE_DATA_HANDLER_PORT='5432'
#FEE_MODULE_DATA_HANDLER_DATABASE='FeeModule_TransData_DEV'
FEE_MODULE_DATA_HANDLER_DATABASE='terra_fee_db'

DB_MAX_CONNECTIONS=10
# (OPTIONAL, DEFAULT=0) Min connections in pool
DB_MIN_CONNECTIONS=0

BACKEND_SECRET_CRYPTO_KEY = "FoCKvdLslUuB4y3EZlKate7XGottHski1LmyqJHvUhs="

LOGS_FOLDER = 'logsFolder'
CORS_ALLOWED_ORIGINS = "*"
DISABLE_CORS="yes"
NOTIFICATION_BASE_URL=http://localhost:<notification_port>/api/v1/notification
IGNORE_NOTIFICATION_ERROR=true
#REDIS_URL='redis://<user>:<password>@<host>:6379/0'
