# Movie-Booking-Application
Movie Booking
Problem statement
Project Goal



Develop a backend Movie Booking Application enabling users to view a full movie list, add new movies with unique IDs, and retrieve specific movie information by ID. Implement strong error handling for duplicate IDs and non-existent movies. The goal is to create a smooth and dependable platform for managing movie data while maintaining data integrity across the system.



Features of the Application:
The application should allow users to:

    • View a list of all the available movies.

    • Add new movies to the system.

    • Retrieve details of a particular movie by providing its unique Id.

    • Delete a movie from the system using its Id.

    • Update details of a movie by providing its Id.

    • Get error messages if I try to add a movie with an existing Id.

    • Get an error message if I try to retrieve or delete a movie that does not exist in the system.

    • Validate movie details like movie name, Id, and movie director name.


Steps:
Use the following guidelines and hints to build the project.

1. We will be utilizing the Spring version 3.0.0 for this mini-project.

2. Create a class with the name Movie in the Model package with the following attributes and the required getters and setters:

    • String id

    • String movieName

    • String movieDirector

    • long movieRating

    • String movieLanguage

    • List writers

    • List actors

    • List genre

3. Create a class with the name controller in the controller package with the following rest APIs as mentioned below:

    • GET "/ticket/movies": It fetch the list of all the movies.

    • POST "/ticket/movie" (@Valid @RequestBody Movie movie, BindingResult bindingResult): It adds a new movie and throws RuntimeException if bindingResult has errors.

    • GET "/ticket/movie/{id}" (@PathVariable String id): It fetches a movie by the given.

    • DELETE "/ticket/movie/{id}" (@PathVariable String id): It deletes a movie by the given Id.

    • PUT "/ticket/update/{id}" (@Valid @RequestBody Movie topic,@PathVariable String id):It updates a movie by the given Id.

4. Create an Interface with the name MovieServiceInterface and its implementation with the name MovieService in the service package which handles the business logic for the APIs mentioned above. 

5. Create the following Runtime Exception Handling classes in the Exceptions package for the below scenarios:

    a. IdAlreadyExist class

        • If the ID already exists

        • It returns a NOTFOUND HTTP response status.

    b. IdNotFound class
 
        • It the id is not found

        • It returns a NOTFOUND HTTP response status.

6. Implement validation for the following attributes:

    • Restrict the ‘movieName’ to have a minimum length of 3 and a maximum length of 20.

    • Restrict the ‘id’ to have a minimum value of 1.

    • The name of the movieDirector can not be null.

    • Restrict the movieRating to have a minimum value of 1 and a maximum value of 10.

7. You are supposed to throw a RuntimeException if any of the above validation criteria is failed.

End Points To Be Created:
Movie Booking Endpoints:

    • GET /ticket/movies: Retrieve the list of all movies associated with a ticket.

    • GET /ticket/movie/{id} : Retrieve a movie based on the given id.

    • POST /ticket/movie: Adds a movie in a ticket (Body: Movie movie, BindingResult bindingResult).

    • PUT /ticket/update/{id}: Updates a movie in a ticket.

    • DELETE /ticket/movie/{id}: Deletes a specific movie from the given ticket.

Testing on Postman:

