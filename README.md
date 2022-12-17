# Rails API Quiz

**Using whatever resources you like (e.g., Google, Stack Overflow, lectures, labs, notes, etc.), answer the following questions.**

1. Write the command to create a new Rails application in API mode with a Postgresql database.

```
rails new myapp --api --d=postgresql
```

2. What are 5 other options that can be passed in to the `rails new` command and what do they do?

```
rails new myapp -d  // to use database mysql/postgresql/sqlite3/oracle
rails new myapp -T // to skip test file creation
rails new myapp -c // to choose css framework tailwind, bootstrap, bulma, postcss, sass
rails new myapp -g // to skip git
rails new myapp -q // to install quiettly
```

3. What one line of code can be put into `routes.rb` to get all the RESTful routes for a given resource (e.g., dogs)?

```
resource :post
```

4. In the context of API development, what is versioning? How do we implement versioning in a Rails API?

```
// versioning strategy using v words
namespace :api do
  namespace :v1 do
    resource :post
  end

  namespace :v2 do
    resource :post
  end
end
```

5. What is serialization in reference to a Rails API?

```
Serialization using two step data preparation where we using ActiveModel::Serializer and, data transformation where we consume json data using javascript/typescript client.
```

6. Imagine a dog walking domain in which a walker has many dogs. Write the `index` action from the `WalkersController`. Remember, your endpoint should return JSON.

```
dog = Dog.joins(:puppies).first
DogSerializer.new(dog).as_json
```

7. Change the code from the question above so that the walkers' dogs get embedded in the JSON being returned from the `index` endpoint.

```

```

8. Again, change the code above to exclude the timestamps from the data being returned in the JSON.

```
```

9. What does CORS mean? Why do we have to think about it when making an API?

```
```

10. What changes do we have to make in our application to allow CORS?

```
```

11. In our dog walking app, what needs to be added to the following class to allow method calls like `Dog.create(name: "Neikko", breed: "mostly rat", age: 13)` and `Dog.find_by(name: "Neikko")` to function properly?

```
class Dog < ApplicationRecord
end
```

```
```




