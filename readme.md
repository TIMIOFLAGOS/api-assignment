
1. Difference  betwen http and https

1. HTTP vs. HTTPS (In Simple Terms)
Think of HTTP like sending a postcard through the mail. Anyone who handles it along the way can see exactly what you wrote on the back. It’s fine for public information, but you wouldn't write your password or credit card number on it.

HTTPS is like putting that postcard inside a secure, indestructible, locked metal box before mailing it. Only you and the recipient have the key to open it. Even if someone intercepts it, they just see a locked box they can't open. The S stands for Secure (using encryption).



2. Generate a json objec representing a student enrolled at marusoft technologies


Student JSON Object (Marusoft Technologies)
{
  "studentId": "MS-2026-8941",
  "fullName": "Alex Rivera",
  "email": "alex.rivera@example.com",
  "enrollmentStatus": "Active",
  "institution": "Marusoft Technologies",
  "enrolledCourses": [
    "Full-Stack Web Development",
    "Database Management Systems"   
  ],
  "performanceMetrics": {
    "attendancePercentage": 94.5,
    "currentGpa": 3.8
  }
}

3. list five real word apis you use everyday

Five Real-World APIs Used Daily
While I don't physically "use" apps like a human, the digital ecosystem relies on these five massive APIs every single day to function:

Google Maps API: Powers location searches, address autocomplete, and delivery tracking in apps like Uber, DoorDash, or logistics platforms.

Stripe API: Handles secure, behind-the-scenes credit card processing for millions of e-commerce websites.

OpenWeatherMap API: Feeds real-time weather forecasts directly to smartphone widgets and smart home devices.

Twilio API: Sends those automated SMS verification codes (OTPs) and text notifications to your phone.

Spotify API: Allows third-party apps, websites, and smart speakers to display playlists and stream music.


4. compare rest and graphql in a table

REST vs. GraphQL: Architectural Comparison
Choosing the right API architecture is critical for system performance, developer velocity, and long-term maintainability. Below is an objective breakdown of how Representational State Transfer (REST) and GraphQL differ across core technical areas.

1. Data Fetching and Network Efficiency
REST API:
In a REST architecture, the server defines the structure of the data returned from an endpoint. This frequently leads to over-fetching (receiving more data than your application actually needs) or under-fetching (not receiving enough data). To get related pieces of information, a client may need to make multiple sequential round-trips to different endpoints.

GraphQL:
GraphQL completely eliminates over-fetching by allowing the client to request exactly the specific data fields it needs—nothing more, nothing less. It can fetch deeply nested, complex, and related resources across multiple domains in a single network request.

2. Endpoints and Routing
REST API:
REST is resource-oriented, meaning it operates through multiple distinct endpoints representing different entities. For example, to load a social media feed, your application might need to call /users, /posts, and /comments separately.

GraphQL:
GraphQL operates via a single "smart" gateway endpoint (typically just /graphql). The client sends its structured query to this single URL, and the GraphQL engine handles compiling the different pieces of data on the backend.

3. Request Structure and Querying
REST API:
REST relies strictly on standard HTTP methods to determine the action being performed: GET (read), POST (create), PUT (update), and DELETE (remove). The structure is implicit based on the endpoint design.

GraphQL:
GraphQL introduces its own custom query language. Instead of relying on various HTTP methods for routing, it primarily uses POST requests where the body contains a specific query (for reading data) or a mutation (for changing data) parsed natively by the server runtime.

4. API Versioning
REST API:
When data structures change in REST, developers typically must introduce explicit version numbers into the URL path or headers (such as /api/v1/users transitioning to /api/v2/users) to avoid breaking existing frontend applications.

GraphQL:
GraphQL APIs evolve continuously without standard version numbers. Because clients only ask for specific fields, developers can safely add new fields to the schema without affecting old clients. Unused fields are simply marked as deprecated over time.

5. Caching Support
REST API:
Because REST uses unique URLs for unique resources, it integrates seamlessly with native web infrastructure. It leverages robust, built-in standard HTTP caching mechanisms (like CDNs, proxies, and browser caches) effortlessly.

GraphQL:
Caching is significantly more complex in GraphQL at the network layer. Because all requests go to a unified POST endpoint, standard CDNs cannot easily cache the responses. Instead, GraphQL heavily relies on specialized, complex client-side caching libraries (like Apollo Client or Relay).

6. Learning Curve and Ecosystem
REST API:
REST has a low-to-moderate learning curve. It has been the industry standard for decades, making it highly intuitive and universally understood by web developers across all programming language ecosystems.

GraphQL:
GraphQL has a steeper learning curve. Teams must master defining strong schemas, writing type definitions, setting up resolvers on the server, and configuring specialized client tools before writing their first feature.

Summary Guidelines: When to Choose Which?
Opt for REST when:
Your application heavily relies on robust web/network infrastructure and CDN caching.

The data and resource definitions are simple, highly static, and strictly structured.

Your team wants immediate compatibility with standard tooling without onboarding overhead.

Opt for GraphQL when:
You need to aggregate data from multiple backend microservices or databases into a single, unified query layer.

Your application operates heavily on mobile devices or in low-bandwidth conditions where minimizing payload size is critical.

Your frontend UI changes rapidly and requires highly dynamic field variations without constantly modifying backend code.




























 5. explain the request responce cycle using a banking application as an example 


The Request-Response Cycle (Banking Example)
The Request-Response Cycle is the fundamental way the internet works: a client asks for something (Request), and a server delivers an answer (Response).

Let's look at how this plays out when you check your account balance on a mobile banking application:

Step 1: The Trigger
You open your banking app and tap the "Check Balance" button.

Step 2: The Request (The Client Asks)
Your banking app (the Client) packages your request into a secure digital envelope. This HTTP Request contains:

An endpoint/URL (e.g., GET /api/v1/account/balance)

Your authentication token (proves it's actually you)

Browser/device information.
The app sends this request over the internet to the bank's computers.

Step 3: The Processing (The Server Thinks)
The bank's computer (the Server) receives the request. It checks your credentials to make sure you're logged in, talks to the bank's secure database to look up your exact balance, and prepares the data.

Step 4: The Response (The Server Answers)
The bank's server packages the answer into an HTTP Response. It includes a Status Code (like 200 OK to show everything went perfectly) and a body containing the data in JSON format:

JSON
{ "balance": 1500.50, "currency": "USD" }
Step 5: The Render
Your banking app receives this response, unpacks the data, and displays "$1,500.50" beautifully on your screen. The cycle is now complete.
