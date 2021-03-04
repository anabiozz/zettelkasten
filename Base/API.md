Links: [[Computer science]]

Articles:
https://stripe.com/docs/api/errors
https://swagger.io/blog/api-documentation/api-documentation-swagger-ui/?_ga=2.32548862.1383816032.1614277595-2034367417.1610701803
https://dev.bitly.com/docs/getting-started/authentication
https://mailchimp.com/developer/marketing/docs/errors/
https://developer.spotify.com/terms/
https://developer.github.com/changes/
https://stripe.com/docs/api

APIs are only as good as their documentation. A great API can be rendered useless if people don’t know how to use it, which is why documentation can be crucial for success in the API economy. But creating and maintaining good documentation that’s easy to read, enjoyable to interact with, and sets the consumer up for success can be extremely challenging. Creating great documentation requires effort and patience, but it has direct implications on API adoption and maintainability. Documenting your APIs can be made significantly more manageable by selecting the right [API documentation tool](https://swaggerhub.com/api-documentation/).  [In a previous post](https://swaggerhub.com/blog/api-documentation/what-is-api-documentation-and-why-it-matters/), I detailed the benefits of good API documentation. But what exactly do we mean by good documentation? We’ve detailed a few good practices to help your team create great API documentation that is loved by your end consumers. But before we do so, it’s important to understand one important question...

## Who is your API documentation for?

Your API is meant to solve real world problems faced by companies in a specific industry, and will directly be integrated into applications by software engineers. As such, there are two types of potential audiences of your API, who will influence your API’s consumption and adoption curve.

### Decision Makers

These are the people who evaluate your API’s services, and decide if it makes sense for the development team to spend time exploring the service. They are looking to use your API to solve potential challenges in their product or service strategy. In many cases, they don’t directly work with your API, but are the main points of contacts for influencing an organization's decision to consume it. Examples of decision makers are CTOs or Product Managers.

### Users

These are the people who will be directly working with your API. They need to learn the ins and outs of your API, and how it applies to their use case.  This could mean learning how to call and integrate with many, or all, of the resources you expose. They are critical to the sustainability of your API. They are analytical, work on important and hard engineering problems, and have a shortage of time. Hence, your API must be easy to use, and have great documentation so these users can successfully integrate with your API as quickly as possible. Example of API users are front end and back end developers. ![](https://static1.smartbear.co/swagger/media/blog/wp/apidecisionmakers.png) Your API’s documentation needs to cater to both these personas. This can be a hard exercise to follow, but it ensures your [API documentation](https://swaggerhub.com/blog/api-resources/swagger-api-documentation/) is sustainable and complete, which ensures [long term success](https://swaggerhub.com/blog/api-strategy/building-a-successful-api/) and ROI.

# Best Practices in API Documentation

Now that we’ve understood who to document APIs for, it’s time to understand what actually goes into good API documentation.

## Fundamental API Documentation Sections

There are sections that have become fundamental to [good API documentation](https://swaggerhub.com/blog/api-documentation/what-is-api-documentation-and-why-it-matters/). These sections form the baseline for good documentation, and should be detailed based on the kind of industry and consumer your API is expected to have. These sections include:

### Authentication

This is the information about using authentication schemes to start consuming your API. Most APIs have authentication schemes,  and consumers have to authenticate before gaining access to the API. Make sure this section is properly documented, and hand-holds users to successfully authenticate against the API. [Bitly is a great example](http://dev.bitly.com/authentication.html) of concise authentication documentation.

### Error messages

Error messages are important because they tell end consumers when they're integrating with your API services in an incorrect way. Explain your error standards, and also provide solutions on how to overcome them when an end consumer gets an error. [Mailchimp does a good job](https://developer.mailchimp.com/documentation/mailchimp/guides/error-glossary/) in detailing all of their possible error codes that consumers may receive.

### Resources

Pay attention to your API’s resources and their associated request and response cycles. Resources are the core components of your API, which users will be interacting with constantly.  List all of the resources your API exposes, and understand how consumers may integrate with them. This will give you a good idea of how to better document the requests and responses under these resources.

### Terms of use

This is the legal agreement between the consumer and your organization, defining how the consumer should ideally use your services. Include API limits under best practices, with terms and conditions. Constraints also need to be clearly stated so that consumers understand what API usage and practices are permitted. Here’s an example of [Spotify’s API terms of use](https://developer.spotify.com/developer-terms-of-use/).

### Change log

Detail updates and versions of your APIs and how that might affect API consumers. This will help consumers know the stability of your API and see if any changes need to be made for an effective API call. Here’s an example of [GitHub’s API changelog](https://developer.github.com/changes/). Mapping the above sections before you start the API documentation is a good way for technical writers to ground themselves on the important priorities.

## Avoid Jargon

Keep in mind that many people working with the API may not have intimate knowledge of the domain or jargon you may be using. Documentation should cater to the “very technical” developer audience, and the less technical decision makers (like Product Managers). A big mistake technical writing teams make is assuming their audience is fully technical and have complete understanding of how to work with APIs. Start your documentation by writing in plain English, and have easy-to-understand domain explanations for every resource. Avoid using too much technical jargon, and write in a way that can be easily understood by people who are new to the API or industry. If you do have technical or domain specific jargon, link that specific item to further documentation explaining these terms. This will ensure clarity and completeness across your API, help consumers know why certain calls exist, and avoid getting too lost in the details of parameters, headers, and responses. A good example for this is [Stripe’s API documentation](https://stripe.com/docs/api), where there’s a deliberate attempt to not use technical words. Even when there is domain-based jargon, they are supported by additional pieces of content to explain what they mean. [YouTube’s API](https://developers.google.com/youtube/v3/guides/implementation) is known for completeness and clarity, and allows developers to easily understand how the API works. They also have a nice navigation left panel for easily accessing documentation of the implementation of various resources, which I personally felt was very beneficial.

## Treat Your Requests and Responses

Give the documentation of your request-response cycles the care they deserve. Having too much information available for the end consumer is never an issue, especially when they’re trying to integrate your services into their applications, so describe your request-response cycles in detail. Document every call your API could offer, with context around the parameters and responses. Responses are the guides for your consumers, indicating whether they’re on the right track, or providing guidance with error messages to help them succeed. Your API users should know exactly what to expect from a successful API call.  Describe the full sample response body in every supported format. Think of not only the format, like XML or JSON, but also of HTTP headers, error codes, and messages. Examples in parameters and responses are also important. Provide examples in every single object which your API is supposed to return, as well as examples of parameters that users can add for a successful API call. Here’s another [great documentation example of Stripe](https://stripe.com/docs/api#errors), and how they details error responses.  Another great example of good documentation of requests and responses is [Instagram](https://www.instagram.com/developer/).

## Arm your Documentation with Resources

There’s additional information and resources you can provide your consumers to be successful with your API. Great API documentation goes [beyond the basic content and Swagger UI](https://swaggerhub.com/blog/api-documentation/api-documentation-swagger-ui/?_ga=2.32548862.1383816032.1614277595-2034367417.1610701803) generated, it’s about ensuring your consumers and prospects reach success with your API as quickly as possible. You can supplement your documentation with additional resources like:

### Getting Started Guide

The Getting Started guide provides a detailed account of how to quickly start working with your API. The emphasis in the guide should be on ensuring consumers reach success with your API as quickly as possible, hand holding them throughout this journey. An example of a [good Getting Started guide is Braintree](https://developers.braintreepayments.com/start/overview), which gives a great overview on integrating and working with their API. 

### SDKs and Libraries

Code libraries help developers quickly call different resources. Having quick and easy methods in different languages to work with your API helps developers feel more comfortable working with the API. SDKs are hard to build, and aren’t crucial for launch, but can contribute greatly to improve API adoption. If your business model is a public, open API model, having SDKs are a great way to engage with the developer community. In such a scenario, if developers find value in your SDKs and APIs, there’s a good chance they will build on top of it, or add more libraries as well. The [Swagger Codegen](http://swagger.io/swagger-codegen/) project helps teams quickly generate SDKs directly from their API documentation.

### Interactive Console

Encourage prospects to immediately test what they read in the API documentation with the API console. Experimentation is powerful, and a console makes getting started easy, with limited liability from the consumer’s perspective. It’s a relatively simple effort to create a console or a sandbox environment for people to interact with your API, but can go a long way in helping developers to know the value of your API visually. A lot of companies like [GitHub](https://developer.github.com/v4/explorer/) and [Microsoft](https://developer.microsoft.com/en-us/graph/graph-explorer) offer interactive consoles to play with their API offerings. 

# Good API documentation takes work, but it’s worth it

We’ve always believed API documentation is a powerful tool to spearhead the growth and maturity of your APIs. It’s the foundations for good developer experience when consuming APIs. Hopefully your journey towards good documentation is easier with the above tips. Popular open source description formats like [OpenAPI Specification](http://swagger.io/specification/) and commercial platforms like [SwaggerHub](https://swaggerhub.com/) allow teams to automate the documentation process and work on a great overall experience consuming APIs. You can [explore the API documentation capabilities of SwaggerHub here](https://swaggerhub.com/api-documentation/?_ga=2.29986559.1383816032.1614277595-2034367417.1610701803), or [try it for yourself for free](https://app.swaggerhub.com/signup?_ga=2.29986559.1383816032.1614277595-2034367417.1610701803).