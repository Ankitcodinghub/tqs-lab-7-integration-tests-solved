# tqs-lab-7-integration-tests-solved
**TO GET THIS SOLUTION VISIT:** [TQS Lab 7-Integration tests Solved](https://www.ankitcodinghub.com/product/tqs-lab-7-integration-tests-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;93899&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;TQS Lab 7-Integration tests Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 19">
<div class="layoutArea">
<div class="column">
Integration tests (Test Containers, REST Assured)

</div>
</div>
<div class="layoutArea">
<div class="column">
Note that:

</div>
</div>
<div class="layoutArea">
<div class="column">
Context and key points

Key Points

While unit tests should focus on using the code with minimal dependencies on collaborators, integration tests focus on interactions and, as such, usually require additional test setup. The Test Containers framework makes it easy to deploy and run a container for the specific objective of running a test and then dispose it. The lifecycle of the container is integrated in the rest runner environment. A common use case is setting a dockerized database to run the test on a specific database.

The integration tests class also includes testing an API. Spring Boot offers a good support, as seen in Lab 3, but you can also resort to more generic testing libraries focused on REST API. A popular framework is RestAssured.

7.1 REST Assured

RestAssured can be used as a REST-client library and we will use it in the context of integration testing, e.g.:

given().

<pre>        param("x", "y").
</pre>
when().

then().

Consider that we want to “test” the https://jsonplaceholder.typicode.com/todos API.

a) Be sure to include the Rest-Assured dependencies in maven and that you are using the

these static imports as presented in the documentation. b) Create tests to verify that:

<ul>
<li>– &nbsp;the endpoint to list all ToDos is available (status code 200)</li>
<li>– &nbsp;when querying for ToDo #4, the API returns an object with title “et porro tempora”</li>
<li>– &nbsp;When listing all “todos”, you get id #198 and #199 in the results.</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>get("/lotto").
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>statusCode(400).
body("lotto.lottoId", equalTo(6));
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
Note: you may explore related examples from documentation or Baeldung.

</div>
</div>
<div class="layoutArea">
<div class="column">
TQS LABS | 19

</div>
</div>
</div>
<div class="page" title="Page 20">
<div class="layoutArea">
<div class="column">
7.2 Cars

Consider the integration tests developed in Lab 3 for the Cars project.

Let us create a new version of the RestController test, using RestAssured.

Create a new test with @WebMvcTest(CarController.class) to minimize the contexts loading.

Since you are only loading the context for the controller, you should mock the required service implementation (e.g. @MockBean CarManagerService service; )

RestAssured has a special support to work with Spring MockMvc. Be sure to add the following dependency:

Then set a MockMvc instance that RestAssured will use when making requests:

RestAssuredMockMvc.mockMvc(mockMvc); Invoke with:

RestAssuredMockMvc.given()…

Note that, in this example, we are using RestAssuredMockMvc instead of RestAssured.

You do not provide a full URL since the MockMvc sliced environment is being used, not the full web environment (the test is faster).

7.3 Test Containers

Test Containers (TC) can be integrated in the test cases to prepare ephemeral docker containers required to run integration tests. A common scenario is to prepare a database server with a well- known state.

TC are not specific to Spring Boot but there is a good support available, which we will use in this example.

<ol>
<li>a) &nbsp;Create a simple SpringBoot project to manage a simple entity (e.g: Book, or Employee, or Student,…) to be persisted into a PostgreSQL database. Suggested dependencies for Spring Initialzr →</li>
<li>b) &nbsp;Be sure to create the entity and the repository.</li>
<li>c) &nbsp;Create an initialization script for the database in which you add a few sample entries.
Suggestion: place the SQL file in test/resources/db/migration/V001__INIT.sql to be picked automatically by Flyway (the Flyway dependency should have been declared).
</li>
<li>d) &nbsp;Create an integration test that prepares a postgres database, inserts some content and reads it back.
Notes:

<ul>
<li>– &nbsp;you may learn from this code example, which is discussed in this video.</li>
<li>– &nbsp;you may want to define a predefined execution order for the JUnit tests.</li>
</ul>
</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
&lt;groupId&gt;io.rest-assured&lt;/groupId&gt; &lt;artifactId&gt;spring-mock-mvc&lt;/artifactId&gt; &lt;scope&gt;test&lt;/scope&gt;

</div>
</div>
<div class="layoutArea">
<div class="column">
20 | TQS LABS

</div>
</div>
</div>
<div class="page" title="Page 21">
<div class="layoutArea">
<div class="column">
45426 Teste e Qualidade de Software

</div>
</div>
<div class="layoutArea">
<div class="column">
7.4 Cars with integration test

Let us create a different version of the full integration test (as in the last task in Lab 3), by using a database in a test container. In addition, use RestAssured as the REST client.

Be sure to:

– launch the test in full web environment this time: @SpringBootTest(webEnvironment = SpringBootTest.WebEnvironment.RANDOM_PORT)

<ul>
<li>– &nbsp;launch the database in a [test] container (e.g.: Postgres)</li>
<li>– &nbsp;use RestAssured to invoke the API.
Note:

You may use a database initialization library or not:
</li>
</ul>
<ul>
<li>– &nbsp;you may use Flyway, for example, as in #7.3, adapting to this new scenario. An initialization script should be included in the project.</li>
<li>– &nbsp;or you can rely on Spring Boot context loading tasks to initialize the database (as it normally does). Take note that addition configuration may be needed [in the test class], as exemplified in this base project [gs_cars_containers].</li>
</ul>
</div>
</div>
</div>
