# Module 6: Codeception

Prior to completing the module below it is highly recommended that you look at the following learning material.  

* [How to Write Testable and Maintainable Code in PHP](http://net.tutsplus.com/tutorials/php/how-to-write-testable-and-maintainable-code-in-php/)
* [Modern Testing In PHP With Codeception](https://tutsplus.com/course/modern-testing-in-php-with-codeception/)
* [Codeception Documentation](http://codeception.com/docs/01-Introduction)

Before you can run codeception on your Mac, you'll need to add a `date.timezone` configuration to your `/etc/php.ini.default` and rename it to `php.ini`.

## The Test


Create a new branch in your 'php-final' git repo called 'codeception' and commit all the work from this module there.  Again be sure to write any code to conform to the PSR-2 standard.

1.  Install Codeceoption using Composer
2.  Using Codeception and your basic MVC application create at least 1 of each of the following tests:
	a.  Unit Test
	b.  Acceptance Test using the PhpBrowser back-end
	
3.  => Stage, Commit and push your code to GIT.
4.  Refactor your Acceptance test settings to use Selenium2 as the back-end.  (Note you may need to use the selenium 2.33 other users have had issues with 2.34)


----------

When you are done, push your code to GIT under this branch, then merge this branch back into 'master' (but don't delete this branch).  Please create a tag called **v1.6** with a message of 'ready for review'.  Be sure your tags are pushed to the remote repository and are visible in GitLab.

Any required communication will again be done on the "issues" feature for the project so this feature **MUST** be enabled in the settings for each repo.  Once your work from this module has been accepted move on to the next module.  You **can** move on to the next module prior to approval, but be aware that some modules build on others output so you may be creating more work for yourself if one module's output needs modification to be accepted.