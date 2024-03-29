# ASP.NET Core Practice Projects
This repository includes projects I wrote while learning <span>ASP.</span>NET Core. I learned <span>ASP.</span>NET MVC and Web Forms prior to Core, so I will document all the differences I found noteworthy.

## Key Takeaways
* <span>ASP.</span>NET Core added Razor Pages as an alternative to MVC.
    * <span>ASP.</span>NET MVC uses the [Front Controller](https://martinfowler.com/eaaCatalog/frontController.html) software design pattern, where a controller is responsible for handling requests to the application. Razor syntax is used for templating its views.
    * Razor Pages uses the [Page Controller](https://www.martinfowler.com/eaaCatalog/pageController.html) software design pattern, which combines the responsibilities of the View and the Controller into each page. This is a bit like Web Forms's .aspx files in that they have backing scripts that handle the logic for the page. https://docs.microsoft.com/en-us/aspnet/core/razor-pages/
* <span>ASP.</span>NET Core added Tag Helpers as an alternative to HTML Helpers to reduce the amount of C# code in Razor views. https://docs.microsoft.com/en-us/aspnet/core/mvc/views/tag-helpers/
* When creating a new <span>ASP.<span>NET Core MVC project, Visual Studio 2019 adds a _ValidationScriptsPartial.cshtml file that adds client-side validation.

## Other Things I Learned
* The HTML Helper extension method DisplayNameFor can retrieve the display name of a model property even through an empty collection. For example:
    ```
    @Html.DisplayNameFor(model => model.Movies[0].Title)
    ```
    The above line will still return the display name of Movie.Title even if the Movies collection is empty.

## Projects
### aspnetcoreapp
Setting up and running an <span>ASP.</span>NET Core web application using the command line. 

Tutorial: https://docs.microsoft.com/en-us/aspnet/core/getting-started/

### RazorPagesMovie
A simple web application that uses Razor Pages and Visual Studio's SQL Server Express LocalDB.

Tutorial: https://docs.microsoft.com/en-us/aspnet/core/tutorials/razor-pages/

### MvcMovie

Tutorial: https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app/