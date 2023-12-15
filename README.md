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
 php artisan serve
```


## Sample Graphql Query and Mutation

- Use this to get the authorization Bearer 
```bash
mutation {
    login(email:"ookuneva@example.org",password:"password", device:"web")
}
```

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
