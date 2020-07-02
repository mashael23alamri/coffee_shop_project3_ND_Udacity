# Coffee Shop Full Stack in udacity

The coffee shop project is a project that has a coffee maker ^_^
Mangers can see and modify drinks, add and delete new drinks
Presta can only see and adjust drinks.

## First, you must create an account at [Auth0](https://manage.auth0.com/)
1- Then update the information in a file auth.py

``` bash
AUTH0_DOMAIN = 'mashaelalamri.us.auth0.com'
ALGORITHMS = ['RS256']
API_AUDIENCE = 'http://localhost:5000'
```
2- I've created two dummy accounts on my Auth0 profile, both of them are verified and functional.

#### Barista account
``` bash
 eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCIsImtpZCI6Im16bm1lelRlUmZEQTNpRXFOVmYxZCJ9.eyJpc3MiOiJodHRwczovL21hc2hhZWxhbGFtcmkudXMuYXV0aDAuY29tLyIsInN1YiI6Imdvb2dsZS1vYXV0aDJ8MTEyNTUwOTcyODU5OTg0ODY0NjU4IiwiYXVkIjpbImh0dHA6Ly9sb2NhbGhvc3Q6NTAwMCIsImh0dHBzOi8vbWFzaGFlbGFsYW1yaS51cy5hdXRoMC5jb20vdXNlcmluZm8iXSwiaWF0IjoxNTkzNzEyMDkzLCJleHAiOjE1OTM3MTkyOTMsImF6cCI6Ik9wZ1JHaTl1cFZCQzV5TFZRZ1p2a2hFWGlVM0RzdEQ5Iiwic2NvcGUiOiJvcGVuaWQgcHJvZmlsZSBlbWFpbCIsInBlcm1pc3Npb25zIjpbImdldDpkcmlua3MtZGV0YWlsIl19.nh5E3WGXjqKCF8OtxmE0J9B9p4S8pUrY3wx565wQndU4j1uR1ao2N18p5XqTQCEScEoVY0UID-IaS7EvNowljXg_52mk-MNuix6Yy_5gRiZNwGCSXV0KaHojwtsCtpNpi_iBxgL1xCdLe3N0KDoO_3ffBa6v1usH5VCE5oD2g040rWHkN_ZJ3Hkc97XpMEc5vLMebXvh6aUTk7XHVFJlHJg5TgVKC5FgttGeu8SbzrlWm3fzaKo8fgzHzNVwUSCD612KJi44YprfoIm_d1pRVBUW-tjFd9GATbnsKFcYZ_i6GMzRo5CIcBt3Ul_pST40i2S4BBJzP6SmQ8WPAOtoDQ
```

#### Manager account
``` bash
eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCIsImtpZCI6Im16bm1lelRlUmZEQTNpRXFOVmYxZCJ9.eyJpc3MiOiJodHRwczovL21hc2hhZWxhbGFtcmkudXMuYXV0aDAuY29tLyIsInN1YiI6Imdvb2dsZS1vYXV0aDJ8MTA3NTk4MTU1NzMyNTMzMzIzOTkwIiwiYXVkIjpbImh0dHA6Ly9sb2NhbGhvc3Q6NTAwMCIsImh0dHBzOi8vbWFzaGFlbGFsYW1yaS51cy5hdXRoMC5jb20vdXNlcmluZm8iXSwiaWF0IjoxNTkzNzEyNTY0LCJleHAiOjE1OTM3MTk3NjQsImF6cCI6Ik9wZ1JHaTl1cFZCQzV5TFZRZ1p2a2hFWGlVM0RzdEQ5Iiwic2NvcGUiOiJvcGVuaWQgcHJvZmlsZSBlbWFpbCIsInBlcm1pc3Npb25zIjpbImRlbGV0ZTpkcmlua3MiLCJnZXQ6ZHJpbmtzLWRldGFpbCIsInBhdGNoOmRyaW5rcyIsInBvc3Q6ZHJpbmtzIl19.aa9KTmqBb8FZb-BV9y8bRQzkJrKET8VSRt_ncOipYtacg69JHiSDEKlv3gVi8-L1N5BxWGyKwA_vWzJY2cjBgaodJ82gNHJB9S_FbNwyGikTD6sTwVqzo2zoNk6TbnBAFcjgNsvw_T2A1hmhRksQrLsa9gl5p_vjv9_8XK0BTEogIXN9rx1T8NIUUcj3ILrMuDORWDRa4FM82kDMiW_N2uPe0-DXK4TNuWI2tABHi7yFGmtFyKvNpLdZQ1eSK0IjQieeuNx0yBiFzVvAFuGgWlLazpYIxg2zIvybgDwLhbhtBy6zkjUVU5EEoTxiB2jVyHcHjtLTccVbCrqey7ZJfg
```

## Now , POSTman
1-Exported collection with configured tokens can be found at: /backend/udacity-fsnd-udaspicelatte.postman_collection_STUDENT_TOKEN.json
2-Test results containing 20 successful cases: /backend/udacity-fsnd-udaspicelatte.postman_collection_test_run.json


# Backend
1-Added Auth0 functionalities on auth.py
2-Implemented RESTful endpoints on api.py
3-Implemented error handlers 400, 404, 422

## Install dependencies in backend, coffee_shop/env/backend/...

```bash
pip3 install -r backend/requirements.txt
```

## Running the server
From within the `./src` directory first

```bash
export FLASK_APP=api.py;
```

To run the server, execute:

```bash
flask run --reload
```

#### NOTE urlopen has a common certificate error described here:
[SSl-certificate](https://stackoverflow.com/questions/50236117/scraping-ssl-certificate-verify-failed-error-for-http-en-wikipedia-org)

# Frontend
1-Added the Auth0 variables on environment.ts
2-Guarantee that the frontend can be launched upon an ionic serve command and the login/token retrieval are functional

## Installing project dependencies
This project uses NPM to manage software dependencies. NPM Relies on the package.json file located in the `frontend` directory of this repository. After cloning, open your terminal and run:

```bash
npm install
```

## Running Your Frontend in Dev Mode
```bash
ionic serve
```
## .gitignore
1-enviornment
2-node_modeules

### References
1-[Auth0](https://manage.auth0.com/)
2-[jwt](https://jwt.io/)
3-[Postman](https://www.postman.com/)
4-[SSl-certificate](https://stackoverflow.com/questions/50236117/scraping-ssl-certificate-verify-failed-error-for-http-en-wikipedia-org)
5-[json.dumps()](https://www.educative.io/edpresso/what-is-the-difference-between-jsonloads-and-jsondumps?aid=5082902844932096&utm_source=google&utm_medium=cpc&utm_campaign=edpresso-dynamic&gclid=CjwKCAjwi_b3BRAGEiwAemPNU8tPcUHkCM2Tn6-hFSWlftodRjp-brXVNuCZ3GUpYyCC-P5ONutnohoCPsEQAvD_BwE)
