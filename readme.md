## Express.js + Typescript

* Create New User

    curl --request POST 'localhost:3030/users' \
    --header 'Content-Type: application/json' \
    --data-raw '{
        "email": "fv.david@gmail.com",
        "password": "sup3rS3cr3tPassw0rd!123"
    }'

* Update User
$USER_ID (User ID)

    curl --request PUT "localhost:3030/users/$USER_ID" \
    --header 'Content-Type: application/json' \
    --data-raw '{
        "email": "fv.david@gmail.com",
        "password": "sup3rS3cr3tPassw0rd!123",
        "firstName": "fv",
        "lastName": "david",
        "permissionLevel": 7
    }'

* Update User
PATCH, if you want to change only email or only firstName

    curl --request PATCH "localhost:3030/users/$REST_API_EXAMPLE_ID" \
    --header 'Content-Type: application/json' \
    --data-raw '{
        "lastName": "davidtbg"
    }'

* GET Users

    curl --request GET 'localhost:3030/users' --header 'Content-Type: application/json'


* Get User By ID

    curl --request GET "localhost:3030/users/$USER_ID" --header 'Content-Type: application/json'


### Next coming up features:
- MongoDB
- Security Layer with JWT
- Automated-testing for Scale