## Laravel Phonebook API

## Installation

- clone the repo https://github.com/killerboduk1/Laravel-PhonebookAPI
- cd to Laravel-PhonebookAPI
- rename or copy .env.example to .env then update your Database credentials
- runs these commands

```bash
 composer install
 php artisan migrate
 php artisan db:seed
```
- run these to generate the key

```bash
php artisan key:generate
php artisan optimize
php artisan config:cache
```

- run the project

```bash
php artisan serve
```

## Sample Graphql Query and Mutation

- First we need to Use this to get the authorization Bearer 
  i added the " graphql-playground " package so that we can test the graphql API
  replace the email with your Users data
```bash
mutation {
    login(email:"ookuneva@example.org",password:"password", device:"web")
}
```

- Copy the generated token and add the token to the HTTP HEADERS it should look like this

![Alt text](https://i.ibb.co/tQJyg95/Screenshot-at-Dec-15-15-02-43.png "Optional Title")



-  View Contact with id filter
```bash
{
  viewContact(id:4){
    name
  }
}
```

-  List all Contact with pagination by 5
```bash
{
  listContacts(first:5, page:1){
    data{
      name,
      contact_no
    }
  }
}
```

-  Create Contact
```bash
mutation {
  createContact(name:"john doe 002", contact_no: "002-002-002"){
    name
  }
}
```

-  Update Contact filter by ID
```bash
mutation {
  updateContact(id:11, name:"john doe 2"){
    name
  }
}
```

-  Delete Contact by ID
```bash
mutation {
  deleteContact(id:11){
    name
  }
}
```
