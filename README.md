### Quick Start

Fork this repository to your github account and clone it to your machine. Then install the dependencies:
```bash
> git clone https://github.com/makersacademy/birthdays.git
> cd birthdays
> bundle
```

### Instructions

- Test-drive an implementation of the requirements
- Make sure your code is [linted](https://github.com/rubocop-hq/rubocop)
- [Open a PR](https://services.github.com/on-demand/github-cli/open-pull-request-github) when you've finished

### Requirements

I want a program that I can load in IRB that allows me to
- Store all of my friends’ birthdays so I can keep track of them
- See them all at once with their names and birthdays each on a line in a tidy format
- Check whose birthday it is today - the program can check through the birthdays I have stored and check each one to see if it’s someone’s birthday, and tells me something like "It's Mary Poppin's birthday today! They are 124 years old!" - otherwise it won't say anything.

More requirements:
- Test-drive extracting a birthday class
- Isolate your birthday list class using a mock for Birthday

### TDD resources

- https://github.com/makersacademy/course/blob/master/pills/tdd.md
- https://github.com/makersacademy/course/blob/master/pills/tdd_quality_discussion.md

### Mocking

- https://relishapp.com/rspec/rspec-mocks/docs/basics/test-doubles


# My notes of wot I did

### User stories

> As a user  
> in order to keep track of my friends' birthdays  
> i want a way to store them

> As a user  
> so that I can see all my friends' birthdays  
> I want a way to print out their names and birthdays in a tidy format

> As a user  
> so that I can tell if it's someone's birthday  
> I want a way to search through the stored birthdays for ones which match today's date

### Imagine how to use it for these stories

```
> birthdays = FriendsBirthdays.new
=> #<FriendsBirthdays:0x0.........>
> birthdays.add("Snoop Dogg", 20, 10, 1971) # Snoop Dogg's birthday is 20th October 1971
=> "Added Snoop Doggy Dogg's birthday"
> birthdays.add("Jacob Rees Mogg", 24, 5, 1969) # Jacob Rees Mogg's birthday is 24th May 1969
=> "Added Jacob Rees Mogg's birthday"
> birthdays.add("Mary Poppins", 8, 3, 1900) # Mary Poppins's birthday is 8th March 1969
=> "Added Jacob Rees Mogg's birthday"
```

```
# after having entered the birthdays in the previous block
> birthdays.print
=> Snoop Dogg: 20/10/1971
   Jacob Rees Mogg: 24/5/1969
   Mary Poppins: 8/3/1900
```

```
```