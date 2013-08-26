# Module 9: REST

In completing this module you may use 3rd party libraries to help you accomplish your goals if you wish to do so.

For this module, create a new GIT branch for your laravel application from Module 8 and call the branch 'rest'.

The link below may provide some valuable insight.

[Designing a Secure REST (Web) API without OAuth](http://www.thebuzzmedia.com/designing-a-secure-rest-api-without-oauth-authentication/)

### Part 1: Integrating a REST API

1.1) Create a new __resourceful__ controller that obeys proper REST conventions for managing CRUD operations for any Model that you already have in your application.  Alternativley if you'd like you can create a new model for this purpose.  We'll refer to this controller as your 'api controller'.

1.2) Your api controller should output JSON along with the propper HTTP status code for each request / response.  Any responses should contain relevant data about the outcome or condition of the request that was made.


### Part 2: API Authentication

2.1) Create a new __resourceful__ controller, model and associated views for managing multiple api consumers.  Each api consumer should at a minimum have attributes for api_key and shared_secret.  You'll use these attributes later to authenticate the api client.

---

_Most APIs require some sort of query authentication: a method of signing API requests with an API key and signature. The signature is usually generated using a shared secret. When you're consuming an API, there should be easy to follow steps to create signatures and authenticate your API requests. When you're writing your own API, you have to create both server-side signature validation and a client-side signature creation strategy._

---

2.2) Modify the api controller you created in part 1 to to handle server-side signature validation of the API request.  You'll need to integrate the api consumer records with their key and shared secret attributes that you created in 2.1 above.

### Part 3: An API Client

Create a new git repo called 'rest-client-ex'.  In this repo you will create a collection of PHP code which will consume your API.  Use your own judgement on how you'd like to setup this client application.  You could make another laravel app, or plain PHP files, you be the judge.

3.1) Create rest-client code that executes each REST endpoint of your API controller.  In doing this you'll need to handle the client-side (api / rest client) signature creation.


----------

When you are done, push your code to GitLab.  Please create a tag called **rest** with a message of 'ready for review' in both your laravel app repo, and the new 'rest-client-ex' repo.  Be sure your tags are pushed to the remote repository and are visible in GitLab.

Create a new "issue" for each repo with the message of Ready for Review and assign it to Brian Webb.

Any required communication will again be done on the "issues" feature for the project so this feature **MUST** be enabled in the settings for each repo.  Once your work from this module has been accepted move on to the next module.  You **can** move on to the next module prior to approval, but be aware that some modules build on others output so you may be creating more work for yourself if one module's output needs modification to be accepted.