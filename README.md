# Korsakov [![Build Status](https://api.travis-ci.org/jjoos/korsakov.png)](http://travis-ci.org/jjoos/korsakov) [![Gem Version](https://badge.fury.io/rb/korsakov.png)](http://badge.fury.io/rb/korsakov) [![Dependency Status](https://gemnasium.com/jjoos/korsakov.png)](https://gemnasium.com/jjoos/korsakov) [![Code Climate](https://codeclimate.com/github/jjoos/korsakov.png)](https://codeclimate.com/github/jjoos/korsakov) [![Coverage Status](https://coveralls.io/repos/jjoos/korsakov/badge.png?branch=master)](https://coveralls.io/r/jjoos/korsakov)

Gem that provides entities for ruby..

### Use at your own risk, this is _EXTREMELY_ alpha and subject to changes without notice.

## Installation

Add this line to your application's Gemfile:

    gem 'korsakov'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install korsakov


## Entities

TODO

## Immutable entities
These objects can be used to simplify your design by making sure your object is always valid.
### Usage
```ruby
class User < Korsakov::Entity
  attributes :name, :username, :email
end

my_entity = User.new do
  self.name = 'jan'
  self.username = 'jjoos'
  self.email = 'jan@deelstra.org'
end

or

my_entity = User.new({name: 'jan', username: 'jjoos', email: 'jan@deelstra.org'})

my_entity = my_entity.update({name: 'joop', email: 'joop@deelstra.org'})

puts my_entity.username
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Run bundle, before starting development.
4. Implement your feature/bugfix and corresponding tests.
5. Make sure your tests run against the latest stable mri.
6. Commit your changes (`git commit -am 'Add some feature'`)
7. Push to the branch (`git push origin my-new-feature`)
8. Create new Pull Request
