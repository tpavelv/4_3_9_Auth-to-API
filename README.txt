1. РЕГИСТРАЦИЯ

request:

POST  https://blog-platform.kata.academy/api/users

    headers: "Content-Type":"application/json"

    body:
    {
    "user": {
        "username": "pavelT",
        "email": "pafka1801@mail.ru",
        "password": "qwer1234"
    }
    }

response:

{
    "user": {
        "username": "pavelt",
        "email": "pafka1801@mail.ru",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY3YjU3MDY0NjRkYjQ0MWQwMDJkMTQzNCIsInVzZXJuYW1lIjoicGF2ZWx0IiwiZXhwIjoxNzQ1MTI4MDM2LCJpYXQiOjE3Mzk5NDQwMzZ9.DUYDxREHxlsz7FZ4NhmbnqgCrql79tAqantOurk6G08"
    }
}

2. ЛОГИНИМСЯ

request:

POST  https://blog-platform.kata.academy/api/users/login

    headers: "Content-Type":"application/json"
   
    body:
    {
    "user": {
        "email": "pafka1801@mail.ru",
        "password": "qwer1234"
    }
    }

response:

{
    "user": {
        "username": "pavelt",
        "email": "pafka1801@mail.ru",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY3YjU3MDY0NjRkYjQ0MWQwMDJkMTQzNCIsInVzZXJuYW1lIjoicGF2ZWx0IiwiZXhwIjoxNzQ1MTI4ODgzLCJpYXQiOjE3Mzk5NDQ4ODN9.U0U2VhZdDAz8DF-GwirtTZiRTs3QKgd7UZP4OKr_i90"
    }
}

3. ПОЛУЧАЕМ ДАННЫЕ ТЕКУЩЕГО ПОЛЬЗОВАТЕЛЯ

request:

GET https://blog-platform.kata.academy/api/user

    headers: "Content-Type":"application/json"
             "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY3YjU3MDY0NjRkYjQ0MWQwMDJkMTQzNCIsInVzZXJuYW1lIjoicGF2ZWx0IiwiZXhwIjoxNzQ1MTMwNzY3LCJpYXQiOjE3Mzk5NDY3Njd9.XzCAYoRkW8NqoFSXaeBEa4csAlWj0tfaBgHJKumebBw"


response:

{
    "user": {
        "username": "pavelt",
        "email": "pafka1801@mail.ru",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY3YjU3MDY0NjRkYjQ0MWQwMDJkMTQzNCIsInVzZXJuYW1lIjoicGF2ZWx0IiwiZXhwIjoxNzQ1MTMxMDA2LCJpYXQiOjE3Mzk5NDcwMDZ9.D92vjynSMkuxn9QA2HQ9TvlfMIeQ-MYJvYsryu2WLIc"
    }
}