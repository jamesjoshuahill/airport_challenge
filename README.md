Airport Challenge
=================

```
        ______
        _\____\___
=  = ==(____MA____)
          \_____\___________________,-~~~~~~~`-.._
          /     o o o o o o o o o o o o o o o o  |\_
          `~-.__       __..----..__                  )
                `---~~\___________/------------`````
                =  ===(_________)

```

Instructions
------------

* Challenge time: all day.
* Feel free to use Google, your notes, books, etc. but please work on your own.
* If you refer to the solution of another coach or student, please put a link to that in your README. s
* If you have a partial solution, **still check in a partial solution**.
* You must submit a pull request to this repo with your code by **9am on Monday**.

Preparation
-----------

1. Fork this repo, and clone to your local machine.
1. Run the command `gem install bundler` (if you don't have bundler already).
1. Run `bundle`.

Task
----

We have a request from a client to write the software to control the flow of planes at an airport. The planes can land and take off provided that the weather is sunny. Occasionally it may be stormy, in which case no planes can land or take off. Here are the user stories that we worked out in collaboration with the client:

```
As an air traffic controller
So I can get passengers to a destination
I want to instruct a plane to land at an airport

As an air traffic controller
So I can get passengers on the way to their destination
I want to instruct a plane to take off from an airport and confirm that it is no longer in the airport

As an air traffic controller
To ensure safety
I want to prevent takeoff when weather is stormy
```

Your task is to test drive the creation of a set of classes/modules to satisfy all the above user stories.

### Weather

You will need to use a random number generator to set the weather (it is normally sunny but on rare occasions it may be stormy). In your tests, you'll need to use a stub to override random weather to ensure consistent test behaviour.

For overriding random weather behaviour, please read the documentation to [learn how to use test doubles](https://www.relishapp.com/rspec/rspec-mocks/docs). There’s an example of using a test double to test a die that’s relevant to testing random weather in the test.

### Edge cases

Your code should defend against [edge cases](http://programmers.stackexchange.com/questions/125587/what-are-the-difference-between-an-edge-case-a-corner-case-a-base-case-and-a-b) such as inconsistent states of the system. For example:
- planes can only take off from airports they are in
- planes that are already flying cannot take off, or be in an airport
- planes that are landed cannot land again and must be in an airport

### Development notes

* Please follow the TDD process to test-drive your code.

* Please create separate files for every class, module and test suite.

* Don’t overcomplicate things. This task isn’t as hard as it may seem at first.

Submission
----------

Please submit a pull request before **Monday at 9am** with your solution or partial solution. However much or little amount of code you wrote *please please please* submit a pull request before Monday at 9am.

This is a practice 'tech test' of the kinds that employers use to screen developer applicants.

Please follow the [submission requirements and guidelines](CONTRIBUTING.md).

BONUS
-----

When you have completed the first set of user stories and opened a pull request, then you can try some bonus material if you wish.

Please don't forget to update your README.

### Bonus stories

Here are some more user stories that we worked out in collaboration with the client:

```
As an air traffic controller
To ensure safety
I want to prevent landing when weather is stormy

As an air traffic controller
To ensure safety
I want to prevent landing when the airport is full

As the system designer
So that the software can be used for many different airports
I would like a default airport capacity that can be overridden as appropriate
```

### Bonus tasks

* Write an RSpec **feature** test that lands and takes off a number of planes.
