# Quotes Server and Quotes Client

#### Quotes Server

https://github.com/planetaska/quote-server

A simple web server that serves inspirational quotes using Rust, Axum web framework, and Askama templating engine with SQLite database storage. Features a RESTful API with OpenAPI documentation and interactive Swagger UI.

#### Quotes Client

https://github.com/planetaska/quote-client

A simple web client that consumes a REST API to display quotes using Rust, Leptos framework, and WebAssembly. Features a responsive interface with client-side rendering for browsing and managing quotes.

## Author

Chia-Wei Hsu (chiawei@pdx.edu)

## Features & Technology Stack

- Please refer to the README in each repository

## Development Process

I started by following the example joke server from class as a foundation, then researched and studied documentation for Axum, Askama, and SQLx to understand the server-side architecture. The development followed an incremental approach, adding features piece by piece following the joke server development pattern. I then enhanced the server with an OpenAPI specification for comprehensive API documentation as demonstrated in the class.

For the client side, I read through most of the Leptos book to understand the framework and WebAssembly integration, then created the actual client application to consume the quote server's REST API. Thanks to the OpenAPI spec, this process went smoother than I anticipated.

## Challenges

I found the most challenging part to be Leptos's lack of human-friendly documentation and community resources - you can hardly find discussions online. It doesn't help that Leptos is still in active development, and old information mixes with new ones. In fact, I find many Rust fullstack crates are like this, so for me the most difficult part was to find out the "right way" to do things in the rapidly evolving ecosystem.

One particularly frustrating moment I encountered was when trying to use Leptos's `A` component. The task I was attempting was as simple as adding a "class" attribute to the `A` component, however, I got a strange error message about trait bounds. I tried "prop:class" because that was the closest thing I could find online - but it was deprecated. There was literally no documentation for this component, and it's impossible to search on Google because it interprets "A" as a common word rather than a component name. I finally gave up and asked Claude, and it turns out I should have used "attr:class" - so close! This experience perfectly highlights the documentation challenges with Leptos and many other Rust web development crates.

## Final Thoughts

I think this has been a great experience to test the waters of Rust fullstack web development. Although the toolchains are quickly changing, we can already see it has the potential for mission-critical web tasks thanks to Rust's performance and safety guarantees. The concurrency model is promising, and WebAssembly is awesome for someone who doesn't like writing in JavaScript frameworks - it provides a compelling alternative for web frontend development. I also find it pretty cool that SwaggerUI can provide interactive API documentation automatically once you have the OpenAPI specs set up.

## Future Improvements

- **Enhanced Authentication**: Move from hard-coded credentials to more sophisticated authentication methods (OAuth, user registration, password hashing)
- **Search and Filtering**: Add search functionality and tag-based filtering for quotes
- **Social Features**: Add user ratings, favorites, and sharing capabilities
