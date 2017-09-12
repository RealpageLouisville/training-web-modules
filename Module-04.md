# Module 4: Test Driven Development (TDD)

***

## Getting Started

Prior to completing the module below it is highly recommended that you look at the following learning material:

- [Test-Driven PHP](http://net.tutsplus.com/sessions/test-driven-php/)
- [How to Write Testable and Maintainable Code in PHP](http://net.tutsplus.com/tutorials/php/how-to-write-testable-and-maintainable-code-in-php/)
- [Laracasts: Testing Jargon](https://laracasts.com/series/testing-jargon)
- [Easier Testing With Mockery](https://tutsplus.com/tutorial/easier-testing-with-mockery/)

***

## The Test

1. Create a new branch in your `php-final` Git repo called `TDD` and commit all the work from this module there.
2. Be sure to write your code to conform to the [**PSR-2**](http://www.php-fig.org/psr/psr-2/) spec.
3. Use Composer to install Mockery, PHPUnit and fzaninotto/Faker. Your `composer.json` and `composer.lock` files should be part of this project.
4. Add a folder called `tests` where all your test code will go.
5. Add a test class for your previous model.
6. Add a method to the test class to test model validation; use Faker to set properties:
	- Create a new object and assert that validation initially fails.
	- Assert that an error exists for each particular property where validation is failing.
	- One by one, set each required property correctly and assert that the error does not exist.
	- When all required properties are set, `assert` that validation passes.
7. Add a method that tests that the model's `save()` and `destroy()` methods are inserting, updating and deleting in the database correctly:
	- Assert that the model's database table is empty, or note the number of records.
	- Create a new object, populate the properties with Faker and call `save()`; assert that the record was inserted into the database.
	- Update the object and call `save()`; assert that the data in relevant table row has been updated correctly AND that no additional records were inserted.
	- Call the `destroy()` method on the model and assert that the record has been removed from the database table.
8. Refactor your model's code to use dependency injection and the Repository pattern:
	- Following the Repository pattern, add a database access object, and define an interface that specifies the methods and properties required.
	- Refactor your model to use dependency injection and the database access object.
	- Add a mock database access object that uses Mockery and conforms to the database access interface to return mock data.
9. Add a new test method to your test class that injects the mock database access object. Test the `create`, `find`, `update` and `delete` functionality of your model without actually hitting the database.

***

## Wrapping Up

When you are done, push your code to GitHub. Please create a tag called `v1.4` with a message of `"ready for review"`. Be sure your tags are pushed to the remote repository and are visible in GitHub.

Create an issue titled **Review Module 5 - Testing Driven Development** and `@mention` your mentor and team leader.
