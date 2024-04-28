1. Install IDE in my case is IntelliJ IDEA
2. Create spring boot project in IntelliJ IDEA
    * Go to file -> new -> project
    * On "Generators" Section choose "Spring Boot"
    * You can leave anything else (type : gradle & maven, language: java, packaging: Jar, Java: 17, JDK 21.0.2) and click next
    * Under "developer tools" tab, you can select "Spring Boot Dev Tools" and under "web"  accordion menu choose "spring web" then click Create button 
3. To get started you can try to click run button, but it would caused an error as there is no controller specified to handle your routing (you can try to access the web via : localhost:8080)
    * you might faced some other errors such as jdk location is wrong, to resolve it you need to correctly specified your JAVA_HOME under your system environtment variable and also your "path"
    * Make sure it match with your Intellij IDEA setting. To check it go to file -> project structure -> platform settings -> sdk (make sure it is the same with your JAVA_HOME variable and Path in system environtment)
4. Now we can create our Controller to handle the request, In this case I create a new controller called Homecontroller by:
    * Right click on [project]->src->main->java->[package name] and choose "new->java class. I give the name HomeController
    * You can see the file in the project and change liek bellow if you just want to test it without creating index.html file.
    @GetMapping("/")
    @ResponseBody
    public String home() {
        return "Welcome to the Spring Boot app!";
        //return "index";
    }
6. Rerun your project by clicking run button once again and access localhost:8080
7. Other than that is explained in the project.
