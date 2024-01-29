# Summary

- Controller Class:

  - Creating a HelloWorldController class to expose a GET REST API (/hello).

- Security and JWT Configuration:
  - Configuring Spring Security and JWT for generating and validating JWT.
  - Adding dependencies: spring-boot-starter-security, jjwt (JSON Web Token library).

- JwtTokenUtil Class:

Handling JWT operations such as creation and validation.
Retrieving username and expiration date from a token.

- JwtUserDetailsService Class:
  - Implementing the UserDetailsService interface for fetching user details.
  - Hardcoded user details for demonstration purposes.

- JwtAuthenticationController Class:
  - Exposing a POST API (/authenticate) to authenticate and generate a JWT.
  - Using AuthenticationManager to authenticate user credentials.

- JwtRequest and JwtResponse Classes:
  - JwtRequest: Storing username and password received from the client.
  - JwtResponse: Creating a response containing the JWT.

- JwtRequestFilter Class:
  - Extending OncePerRequestFilter to check for a valid JWT in incoming requests.
  - Setting Authentication in the context if the token is valid.

- JwtAuthenticationEntryPoint Class:
  - Extending AuthenticationEntryPoint to handle unauthorized requests.
  - Sends a 401 error for unauthenticated requests.

- WebSecurityConfig Class:
  - Extending WebSecurityConfigurerAdapter for customizing WebSecurity and HttpSecurity.
  - Configuring authentication manager, password encoder, and specifying URL patterns.

- Running the Application:
  - Start the Spring Boot Application.
  - Generate a JSON Web Token by making a POST request to /authenticate.
  - Validate the token by accessing /hello with the generated token in the header.
