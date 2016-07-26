# BCrypt in Ruby

> How to use BCrypt in Ruby

Using BCrypt in Ruby is just as easy - probably easier - than using it in JavaScript. There are about 4 methods you need to know to successfully hash passwords and compare them for authentication.

## Setup

As with all Ruby gems you need to add it to your `Gemfile`. Search Rubygems.org for the BCrypt gem and then add it to your Gemfile.

If you're using Bundler and have a `Bundler.require` line in your `config.ru` then you're good to go. If not, you'll need to `require 'bcrypt'` in whichever file you use it.

## Hashing Passwords

Here's how to hash a password and save it to your database in Ruby. We assume we're in some sort of UsersController here.

```ruby
class UsersController < ApplicationController
  post '/?' do
    password = BCrypt::Password.create(params['password'])

    user = User.create username: params['username'], password: password

    if user
      'User was created!'
    else
      'Error creating user'
    end
  end
end
```

## Comparing passwords

To compare a password a user enters from an input field to one stored in the database you create a new instance of a BCrpyt password and compare it to the plain text. __The order of the comparison matters a lot!!!__ So pay attention to what is `==` to what.

```ruby
class UsersController < ApplicationController
  post '/login/?' do
    user = User.find_by username: params['username']

    if user
      password = BCrypt::Password.new(user.password)

      if password == params['password']
        'You are logged in'
      else
        'You entered the wrong password'
      end
    else
      'No user with that username exists'
    end
  end
end
```

Simple. We get the user from the database. Then we run their password through Bcrypt to create a new instance of a BCrypt object. Then we compare it to the plain text password the user entered into the login field. If true we let them through. If false we kick them out.

> Bcrypt: It's simple!
