# Start
`docker-compose up --scale keycloak=3`

# Testing

1. Get access and refresh tokens:

`curl --location --request POST 'http://localhost:8080/auth/realms/master/protocol/openid-connect/token' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'username=admin' \
--data-urlencode 'password=Pa55w0rd' \
--data-urlencode 'grant_type=password' \
--data-urlencode 'client_id=admin-cli'`

2. Get a new assess token by refresh token from the previous step:

`curl --location --request POST 'http://localhost:8080/auth/realms/master/protocol/openid-connect/token' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'grant_type=refresh_token' \
--data-urlencode 'client_id=admin-cli' \
--data-urlencode 'refresh_token=<REFRESH_TOKEN_FROM_STEP_1>'`

3. Then, one by one, we stop one KeyCloak instance and check the operability through the request of step 2 (see above)


