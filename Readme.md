# Learn Node.js by building a backend framework - [Velocy](https://github.com/ishtms/velocy)

<p align="center">
  <img src="./assets/imgs/cover.jpg" alt="Learn nodejs the hard way" width="500">
</p>

You can access the current version of the book in the [chapters directory](/chapters) or in PDF format (both Light and Dark modes are available) by [clicking here](https://github.com/ishtms/learn-nodejs-hard-way/releases). Note that this version includes the current release of the content, and is not the final version.

> This book is still in a very early stage. It contains an insignificant portion of the total content that the book is supposed to cover. There’s going to be 0 dependencies for our [backend framework](https://github.com/ishtms/velocy), as well as our [logging library](https://github.com/ishtms/logtar). Everything will be done using vanilla Node.js, the hard-way (the best way to learn).

---

## Note

If you're not familiar with javascript, you may also check out my other repository - [Learn Javascript - The Easy Way](https://github.com/ishtms/learn-javascript-easy-way) that takes you on a deep and a fun journey into Javascript - from the very basics to the advanced concepts that you'd ever need, without diving into too much theory. Only practical code examples.

---

To master a new concept, it's often best to begin from the ground up. This isn't just another Node.js guide; it's a comprehensive, code-along experience aimed at building a real world product that may be used by thousands of developers. The product that we're going to build will be a backend framework, that too from scratch.

You won't just learn how Node.js works, but also why it operates in a particular way. The guide also includes discussions on relevant data structures and design patterns.

The book also includes a wide range of exercises specifically created to challenge you, that may require commitment and consistent effort on your part.

This guide goes beyond the basics. We're focused on delivering a modular, optimized backend framework that is close to being production-ready. Topics like performance optimization, security measures, and various testing approaches will be covered to ensure the framework is both reliable and extendable.

I highly recommend actively coding alongside this guide, rather than just reading through it, for a full understanding of Node.js and its more intricate aspects.

The repo for our backend framework- [Velocy](https://github.com/ishtms/velocy). (W.I.P)

[![Read Next](/assets/imgs/next.png)](/chapters/ch01.0-what-is-a-web-server-anyway.md)

# Table of contents

- [(Optional) Node.js is way faster than you think](chapters/ch00-nodejs-faster-than-you-think.md#-optional-node-js-is-way-faster-than-you-think)
  - [Contenders for the test](chapters/ch00-nodejs-faster-than-you-think.md#contenders-for-the-test)
    - [Elysia - Bun](chapters/ch00-nodejs-faster-than-you-think.md#elysia-bun)
    - [Axum - Rust](chapters/ch00-nodejs-faster-than-you-think.md#axum-rust)
    - [Express - Node.js](chapters/ch00-nodejs-faster-than-you-think.md#express-node-js)
    - [Velocy - Node.js](chapters/ch00-nodejs-faster-than-you-think.md#velocy-node-js)
  - [The benchmark](chapters/ch00-nodejs-faster-than-you-think.md#the-benchmark)
  - [Source code](chapters/ch00-nodejs-faster-than-you-think.md#source-code)
    - [Elysia - Bun](chapters/ch00-nodejs-faster-than-you-think.md#elysia-bun)
    - [Axum - Rust](chapters/ch00-nodejs-faster-than-you-think.md#axum-rust)
    - [Express - Node.js](chapters/ch00-nodejs-faster-than-you-think.md#express-node-js)
    - [Velocy - Node.js](chapters/ch00-nodejs-faster-than-you-think.md#velocy-node-js)
  - [Results - Typical benchmark](chapters/ch00-nodejs-faster-than-you-think.md#results-typical-benchmark)
    - [Result: Elysia - Bun/Zig (149,047 req/s)](chapters/ch00-nodejs-faster-than-you-think.md#result-elysia-bun-zig-149-047-req-s-)
    - [Result: Axum - Rust (208,938 req/s)](chapters/ch00-nodejs-faster-than-you-think.md#result-axum-rust-208-938-req-s-)
    - [Result: Express - Node.js (28,923 req/s)](chapters/ch00-nodejs-faster-than-you-think.md#result-express-node-js-28-923-req-s-)
  - [Result: Velocy - Node.js (83,689)](chapters/ch00-nodejs-faster-than-you-think.md#result-velocy-node-js-83-689-)
  - [Graphs](chapters/ch00-nodejs-faster-than-you-think.md#graphs)
    - [Latency](chapters/ch00-nodejs-faster-than-you-think.md#latency)
    - [Requests/sec](chapters/ch00-nodejs-faster-than-you-think.md#requests-sec)
    - [Idle memory](chapters/ch00-nodejs-faster-than-you-think.md#idle-memory)
    - [Memory under constant load](chapters/ch00-nodejs-faster-than-you-think.md#memory-under-constant-load)
    - [Verdict - Typical benchmark](chapters/ch00-nodejs-faster-than-you-think.md#verdict-typical-benchmark)
  - [The real benchmark](chapters/ch00-nodejs-faster-than-you-think.md#the-real-benchmark)
    - [Updating our code](chapters/ch00-nodejs-faster-than-you-think.md#updating-our-code)
    - [Elysia](chapters/ch00-nodejs-faster-than-you-think.md#elysia)
    - [Express](chapters/ch00-nodejs-faster-than-you-think.md#express)
  - [Velocy](chapters/ch00-nodejs-faster-than-you-think.md#velocy)
  - [Results - A real-world use-case](chapters/ch00-nodejs-faster-than-you-think.md#results-a-real-world-use-case)
    - [Result: Express - Node (50,275 req/sec)](chapters/ch00-nodejs-faster-than-you-think.md#result-express-node-50-275-req-sec-)
    - [Result: Velocy - Node (138,956 req/sec)](chapters/ch00-nodejs-faster-than-you-think.md#result-velocy-node-138-956-req-sec-)
    - [Latency](chapters/ch00-nodejs-faster-than-you-think.md#latency)
    - [Latency without `max latency` bar](chapters/ch00-nodejs-faster-than-you-think.md#latency-without-max-latency-bar)
    - [Requests/sec](chapters/ch00-nodejs-faster-than-you-think.md#requests-sec)
    - [Idle memory](chapters/ch00-nodejs-faster-than-you-think.md#idle-memory)
    - [Memory under constant load](chapters/ch00-nodejs-faster-than-you-think.md#memory-under-constant-load)
  - [Final Verdict](chapters/ch00-nodejs-faster-than-you-think.md#final-verdict)
- [What the heck is a web server any way?](chapters/ch01.0-what-is-a-web-server-anyway.md#what-the-heck-is-a-web-server-any-way-)
  - [Parts of a Web Server:](chapters/ch01.0-what-is-a-web-server-anyway.md#parts-of-a-web-server-)
    - [Navigating the World of Protocols: A Quick Overview](chapters/ch01.0-what-is-a-web-server-anyway.md#navigating-the-world-of-protocols-a-quick-overview)
    - [The Relationship Between HTTP and TCP: Ensuring Reliable Web Communication](chapters/ch01.0-what-is-a-web-server-anyway.md#the-relationship-between-http-and-tcp-ensuring-reliable-web-communication)
    - [1. Data Integrity and Order](chapters/ch01.0-what-is-a-web-server-anyway.md#1-data-integrity-and-order)
    - [2. Acknowledgment Mechanism](chapters/ch01.0-what-is-a-web-server-anyway.md#2-acknowledgment-mechanism)
    - [3. Complex Interactions](chapters/ch01.0-what-is-a-web-server-anyway.md#3-complex-interactions)
    - [4. Transmission Overhead](chapters/ch01.0-what-is-a-web-server-anyway.md#4-transmission-overhead)
  - [Asking and Getting: How Web Servers Respond to Your Requests](chapters/ch01.0-what-is-a-web-server-anyway.md#asking-and-getting-how-web-servers-respond-to-your-requests)
    - [The Request:](chapters/ch01.0-what-is-a-web-server-anyway.md#the-request-)
    - [The Response:](chapters/ch01.0-what-is-a-web-server-anyway.md#the-response-)
- [Your first `node.js` program](chapters/ch02.0-your-first-nodejs-program.md#your-first-node-js-program)
  - [What exactly is node or nodejs?](chapters/ch02.0-your-first-nodejs-program.md#what-exactly-is-node-or-nodejs-)
  - [Your first node.js program](chapters/ch02.0-your-first-nodejs-program.md#your-first-node-js-program)
    - [How does `console.log()` work in Node.js?](chapters/ch02.0-your-first-nodejs-program.md#how-does-console-log-work-in-node-js-)
    - [The **`process` Object**:](chapters/ch02.0-your-first-nodejs-program.md#the-process-object-)
    - [The `stdout` **property of the `process` object**:](chapters/ch02.0-your-first-nodejs-program.md#the-stdout-property-of-the-process-object-)
- [Working with files](chapters/ch03.0-working-with-files.md#working-with-files)
  - [What will the logging library do](chapters/ch03.0-working-with-files.md#what-will-the-logging-library-do)
  - [How do you work with files anyway?](chapters/ch03.0-working-with-files.md#how-do-you-work-with-files-anyway-)
  - [Let’s get back to `files`](chapters/ch03.0-working-with-files.md#let-s-get-back-to-files-)
  - [A little more about file descriptors](chapters/ch03.0-working-with-files.md#a-little-more-about-file-descriptors)
  - [Creating our first file](chapters/ch03.0-working-with-files.md#creating-our-first-file)
  - [`path` argument](chapters/ch03.0-working-with-files.md#-path-argument)
  - [`flag` argument](chapters/ch03.0-working-with-files.md#-flag-argument)
  - [`mode` argument](chapters/ch03.0-working-with-files.md#-mode-argument)
  - [Reading from a file](chapters/ch03.0-working-with-files.md#reading-from-a-file)
  - [A small primer on `for..of` and `for await..of` in javascript](chapters/ch03.0-working-with-files.md#a-small-primer-on-for-of-and-for-await-of-in-javascript)
    - [`for..of`](chapters/ch03.0-working-with-files.md#-for-of-)
    - [`for await..of`](chapters/ch03.0-working-with-files.md#-for-await-of-)
  - [Reading the `json` file](chapters/ch03.0-working-with-files.md#reading-the-json-file)
  - [Buffers](chapters/ch03.0-working-with-files.md#buffers)
    - [Parsing the `json` file](chapters/ch03.0-working-with-files.md#parsing-the-json-file)
- [`logtar` our own logging library](chapters/ch04.0-logtar-our-logging-library.md#-logtar-our-own-logging-library)
  - [Initializing a new project](chapters/ch04.0-logtar-our-logging-library.md#initializing-a-new-project)
  - [A little about `SemVer`](chapters/ch04.0-logtar-our-logging-library.md#a-little-about-semver-)
  - [Creating a `LogLevel` class](chapters/ch04.0-logtar-our-logging-library.md#creating-a-loglevel-class)
  - [The `Logger` class](chapters/ch04.0-logtar-our-logging-library.md#the-logger-class)
    - [Encapsulation with `private` fields](chapters/ch04.0-logtar-our-logging-library.md#encapsulation-with-private-fields)
  - [The `LogConfig` class](chapters/ch04.0-logtar-our-logging-library.md#the-logconfig-class)
  - [Design patterns](chapters/ch04.0-logtar-our-logging-library.md#design-patterns)
    - [The `Builder` pattern](chapters/ch04.0-logtar-our-logging-library.md#the-builder-pattern)
  - [Using `builder` pattern with the `LogConfig` class](chapters/ch04.0-logtar-our-logging-library.md#using-builder-pattern-with-the-logconfig-class)
  - [jsdoc comments](chapters/ch04.0-logtar-our-logging-library.md#jsdoc-comments)
  - [The `RollingConfig` class](chapters/ch04.0-logtar-our-logging-library.md#the-rollingconfig-class)
    - [The `RollingSizeOptions` class](chapters/ch04.0-logtar-our-logging-library.md#the-rollingsizeoptions-class)
    - [The `RollingTimeOptions` class](chapters/ch04.0-logtar-our-logging-library.md#the-rollingtimeoptions-class)
  - [Finishing up the `RollingConfig` class](chapters/ch04.0-logtar-our-logging-library.md#finishing-up-the-rollingconfig-class)
    - [Let's recap](chapters/ch04.0-logtar-our-logging-library.md#let-s-recap)
  - [Adding more useful methods in the `LogConfig` class](chapters/ch04.0-logtar-our-logging-library.md#adding-more-useful-methods-in-the-logconfig-class)
    - [Why `readFileSync`?](chapters/ch04.0-logtar-our-logging-library.md#why-readfilesync-)
  - [Refactoring the code](chapters/ch04.1-refactoring-the-code.md#refactoring-the-code)
    - [**The Need for Refactoring**](chapters/ch04.1-refactoring-the-code.md#-the-need-for-refactoring-)
    - [**Creating Separate Files**](chapters/ch04.1-refactoring-the-code.md#-creating-separate-files-)
    - [The `index.js` file](chapters/ch04.1-refactoring-the-code.md#the-index-js-file)
    - [The `lib/logtar.js` file](chapters/ch04.1-refactoring-the-code.md#the-lib-logtar-js-file)
    - [The `lib/logger.js` file](chapters/ch04.1-refactoring-the-code.md#the-lib-logger-js-file)
    - [The `lib/config/log-config.js` file](chapters/ch04.1-refactoring-the-code.md#the-lib-config-log-config-js-file)
    - [The `lib/config/rolling-config.js` file](chapters/ch04.1-refactoring-the-code.md#the-lib-config-rolling-config-js-file)
    - [The `lib/utils/log-level.js` file](chapters/ch04.1-refactoring-the-code.md#the-lib-utils-log-level-js-file)
    - [The `lib/utils/rolling-options.js` class](chapters/ch04.1-refactoring-the-code.md#the-lib-utils-rolling-options-js-class)
  - [Writing logs](chapters/ch04.2-writing-logs.md#writing-logs)
    - [1. Re-using the File Handle](chapters/ch04.2-writing-logs.md#1-re-using-the-file-handle)
    - [2. Log Rotation](chapters/ch04.2-writing-logs.md#2-log-rotation)
    - [3. Asynchronous Logging](chapters/ch04.2-writing-logs.md#3-asynchronous-logging)
    - [4. Getting Caller Information (Module and Line Number)](chapters/ch04.2-writing-logs.md#4-getting-caller-information-module-and-line-number-)
    - [Testing our current API](chapters/ch04.2-writing-logs.md#testing-our-current-api)
    - [Implementing logging methods](chapters/ch04.2-writing-logs.md#implementing-logging-methods)
    - [DRY (Don't Repeat Yourself)](chapters/ch04.2-writing-logs.md#dry-don-t-repeat-yourself-)
    - [The `log` method](chapters/ch04.2-writing-logs.md#the-log-method)
    - [Considering the `log_level` member variable](chapters/ch04.2-writing-logs.md#considering-the-log_level-member-variable)
    - [Writing to a file](chapters/ch04.2-writing-logs.md#writing-to-a-file)
    - [Another gotcha](chapters/ch04.2-writing-logs.md#another-gotcha)
    - [Logs directory configuration](chapters/ch04.2-writing-logs.md#logs-directory-configuration)
    - [The `require` object](chapters/ch04.2-writing-logs.md#the-require-object)
    - [Adding a new helper to create log directory](chapters/ch04.2-writing-logs.md#adding-a-new-helper-to-create-log-directory)
    - [Updating the `init` method](chapters/ch04.2-writing-logs.md#updating-the-init-method)
    - [Completing the `log` method](chapters/ch04.2-writing-logs.md#completing-the-log-method)
  - [Capturing metadata](chapters/ch04.3-capturing-metadata.md#capturing-metadata)
    - [What is a Stack?](chapters/ch04.3-capturing-metadata.md#what-is-a-stack-)
    - [Examples of Stacks](chapters/ch04.3-capturing-metadata.md#examples-of-stacks)
    - [The Call Stack](chapters/ch04.3-capturing-metadata.md#the-call-stack)
    - [Getting the stack info](chapters/ch04.3-capturing-metadata.md#getting-the-stack-info)
    - [Getting the `callee` name and the line number](chapters/ch04.3-capturing-metadata.md#getting-the-callee-name-and-the-line-number)
    - [A more ergonomic way](chapters/ch04.3-capturing-metadata.md#a-more-ergonomic-way)
    - [Using the `get_caller_info` function](chapters/ch04.3-capturing-metadata.md#using-the-get_caller_info-function)
  - [A small intro to `async` vs `sync`](chapters/ch04.4-intro-to-async-vs-sync.md#a-small-intro-to-async-vs-sync-)
    - [The Balance between Opposites](chapters/ch04.4-intro-to-async-vs-sync.md#the-balance-between-opposites)
    - [Mixing Asynchronous and Synchronous Code](chapters/ch04.4-intro-to-async-vs-sync.md#mixing-asynchronous-and-synchronous-code)
    - [Faster I/O out of the box](chapters/ch04.4-intro-to-async-vs-sync.md#faster-i-o-out-of-the-box)
    - [Blocking Code](chapters/ch04.4-intro-to-async-vs-sync.md#blocking-code)
    - [Concurrency](chapters/ch04.4-intro-to-async-vs-sync.md#concurrency)
  - [Adding Rolling File Support](chapters/ch04.5-rolling-file-support.md#adding-rolling-file-support)
    - [Rolling features](chapters/ch04.5-rolling-file-support.md#rolling-features)
    - [The `rolling_check()` method](chapters/ch04.5-rolling-file-support.md#the-rolling_check-method)
    - [`file_handle.stat()`](chapters/ch04.5-rolling-file-support.md#-file_handle-stat-)
    - [Calling the `rolling_check` method](chapters/ch04.5-rolling-file-support.md#calling-the-rolling_check-method)
    - [A big gotcha!](chapters/ch04.5-rolling-file-support.md#a-big-gotcha-)
  - [Stack traces across `await` points](chapters/ch04.5-rolling-file-support.md#stack-traces-across-await-points)
    - [Testing the new Log file creation](chapters/ch04.5-rolling-file-support.md#testing-the-new-log-file-creation)
- [HTTP Deep dive](chapters/ch05.0-http-deep-dive.md#http-deep-dive)
  - [A small web server](chapters/ch05.0-http-deep-dive.md#a-small-web-server)
    - [Starting our web server](chapters/ch05.0-http-deep-dive.md#starting-our-web-server)
    - [Testing our web server](chapters/ch05.0-http-deep-dive.md#testing-our-web-server)
    - [Testing with `cURL`](chapters/ch05.0-http-deep-dive.md#testing-with-curl-)
  - [HTTP Verbs, Versioning and the benefits of `HTTP/1.1`](chapters/ch05.1-http-verbs-versioning-http1_1.md#http-verbs-versioning-and-the-benefits-of-http-1-1-)
    - [`GET` - Retrieve data](chapters/ch05.1-http-verbs-versioning-http1_1.md#-get-retrieve-data)
    - [`POST` - Create something](chapters/ch05.1-http-verbs-versioning-http1_1.md#-post-create-something)
    - [`PUT` - Replace or Create](chapters/ch05.1-http-verbs-versioning-http1_1.md#-put-replace-or-create)
    - [`HEAD` - Retrieve Metadata](chapters/ch05.1-http-verbs-versioning-http1_1.md#-head-retrieve-metadata)
    - [`DELETE` - Remove from existence](chapters/ch05.1-http-verbs-versioning-http1_1.md#-delete-remove-from-existence)
    - [`PATCH` - Partial updates](chapters/ch05.1-http-verbs-versioning-http1_1.md#-patch-partial-updates)
    - [A small recap](chapters/ch05.1-http-verbs-versioning-http1_1.md#a-small-recap)
    - [The `/` path](chapters/ch05.1-http-verbs-versioning-http1_1.md#the-path)
    - [`HTTP/0.9`](chapters/ch05.1-http-verbs-versioning-http1_1.md#-http-0-9-)
    - [`HTTP/1.0`](chapters/ch05.1-http-verbs-versioning-http1_1.md#-http-1-0-)
    - [`HTTP/1.1`](chapters/ch05.1-http-verbs-versioning-http1_1.md#-http-1-1-)
  - [User agents](chapters/ch05.2-user-agents.md#user-agents)
    - [`User-Agent` can be weird](chapters/ch05.2-user-agents.md#-user-agent-can-be-weird)
  - [MIME Type and `Content-Type`](chapters/ch05.3-mime-type-and-content-type.md#mime-type-and-content-type-)
    - [Understanding the `Accept` Header](chapters/ch05.3-mime-type-and-content-type.md#understanding-the-accept-header)
    - [Mime Type](chapters/ch05.3-mime-type-and-content-type.md#mime-type)
    - [Anatomy of a MIME type](chapters/ch05.3-mime-type-and-content-type.md#anatomy-of-a-mime-type)
    - [But why the wildcard `*/*`?](chapters/ch05.3-mime-type-and-content-type.md#but-why-the-wildcard-)
    - [The `Content-Type` header](chapters/ch05.3-mime-type-and-content-type.md#the-content-type-header)
    - [The `charset=UTF-8`: character encoding](chapters/ch05.3-mime-type-and-content-type.md#the-charset-utf-8-character-encoding)
  - [Headers](chapters/ch05.4-headers.md#headers)
    - [Header Name](chapters/ch05.4-headers.md#header-name)
    - [Colon (`:`)](chapters/ch05.4-headers.md#colon-)
    - [Header Value](chapters/ch05.4-headers.md#header-value)
    - [Whitespace](chapters/ch05.4-headers.md#whitespace)
    - [Custom `X-` based headers](chapters/ch05.4-headers.md#custom-x-based-headers)
  - [Request headers](chapters/ch05.4-headers.md#request-headers)
    - [Accept](chapters/ch05.4-headers.md#accept)
    - [Referer](chapters/ch05.4-headers.md#referer)
    - [Authorization](chapters/ch05.4-headers.md#authorization)
    - [Cookie](chapters/ch05.4-headers.md#cookie)
    - [Host](chapters/ch05.4-headers.md#host)
    - [Content-Type (request)](chapters/ch05.4-headers.md#content-type-request-)
  - [Response Headers](chapters/ch05.4-headers.md#response-headers)
    - [Content-Type (response)](chapters/ch05.4-headers.md#content-type-response-)
    - [Cache-Control](chapters/ch05.4-headers.md#cache-control)
    - [Set-Cookie](chapters/ch05.4-headers.md#set-cookie)
  - [Response and Status Codes](chapters/ch05.5-response-status-codes.md#response-and-status-codes)
    - [`Connection: close` in action](chapters/ch05.5-response-status-codes.md#-connection-close-in-action)
    - [Status Codes](chapters/ch05.5-response-status-codes.md#status-codes)
- [`Velocy` - Our backend framework](chapters/ch06.00-velocy-our-backend-framework.md#-velocy-our-backend-framework)
  - [Why Velocy?](chapters/ch06.00-velocy-our-backend-framework.md#why-velocy-)
  - [What is a backend framework/library anyway?](chapters/ch06.00-velocy-our-backend-framework.md#what-is-a-backend-framework-library-anyway-)
  - [Core features of our backend framework](chapters/ch06.00-velocy-our-backend-framework.md#core-features-of-our-backend-framework)
    - [Routing and URL Handling:](chapters/ch06.00-velocy-our-backend-framework.md#routing-and-url-handling-)
    - [Middlewares](chapters/ch06.00-velocy-our-backend-framework.md#middlewares)
    - [Building our own database](chapters/ch06.00-velocy-our-backend-framework.md#building-our-own-database)
    - [Caching](chapters/ch06.00-velocy-our-backend-framework.md#caching)
    - [Rate limiting](chapters/ch06.00-velocy-our-backend-framework.md#rate-limiting)
    - [Some other features that we will be implementing](chapters/ch06.00-velocy-our-backend-framework.md#some-other-features-that-we-will-be-implementing)
  - [A basic `Router` implementation](chapters/ch06.01-basic-router-implementation.md#a-basic-router-implementation)
    - [A Toy Router](chapters/ch06.01-basic-router-implementation.md#a-toy-router)
    - [`Transfer-Encoding: chunked`](chapters/ch06.01-basic-router-implementation.md#-transfer-encoding-chunked-)
    - [Chunks, oh no!](chapters/ch06.01-basic-router-implementation.md#chunks-oh-no-)
    - [Specifying `Content-Length`](chapters/ch06.01-basic-router-implementation.md#specifying-content-length-)
    - [Code reusability](chapters/ch06.01-basic-router-implementation.md#code-reusability)
  - [The `Router` class](chapters/ch06.02-the-router-class.md#the-router-class)
    - [Using `Router` with an HTTP server](chapters/ch06.02-the-router-class.md#using-router-with-an-http-server)
  - [`this` is not good](chapters/ch06.02-the-router-class.md#-this-is-not-good)
    - [Lexical Context](chapters/ch06.02-the-router-class.md#lexical-context)
    - [Arrow functions are not free](chapters/ch06.02-the-router-class.md#arrow-functions-are-not-free)
    - [Why should we care about memory?](chapters/ch06.02-the-router-class.md#why-should-we-care-about-memory-)
    - [Testing the updated code](chapters/ch06.02-the-router-class.md#testing-the-updated-code)
  - [Improving the `Router` API](chapters/ch06.03-improving-the-router-api.md#improving-the-router-api)
  - [The Need for a `Trie`](chapters/ch06.04-the-need-for-a-trie.md#the-need-for-a-trie-)
    - [What is a `Trie` anyway?](chapters/ch06.04-the-need-for-a-trie.md#what-is-a-trie-anyway-)
  - [Ex. Implementing a `Trie`](chapters/ch06.05-ex-implementing-a-trie.md#exercise-1-implementing-a-trie-)
    - [Root Node](chapters/ch06.05-ex-implementing-a-trie.md#root-node)
    - [End of the word](chapters/ch06.05-ex-implementing-a-trie.md#end-of-the-word)
    - [Challenge 1: Basic Trie with `insert` Method](chapters/ch06.05-ex-implementing-a-trie.md#challenge-1-basic-trie-with-insert-method)
    - [Challenge 2: Implement `search` method](chapters/ch06.05-ex-implementing-a-trie.md#challenge-2-implement-search-method)
  - [Ex. Implementing our Trie based `Router`](chapters/ch06.06-ex-implementing-router.md#exercise-2-implementing-our-trie-based-router-)
    - [Challenge 1: Implementing the `addRoute` method](chapters/ch06.06-ex-implementing-router.md#challenge-1-implementing-the-addroute-method)
    - [Challenge 2: Implementing the `findRoute` method](chapters/ch06.06-ex-implementing-router.md#challenge-2-implementing-the-findroute-method)
  - [Ex. Adding `HTTP` method support](chapters/ch06.07-ex-adding-http-methods.md#exercise-3-adding-http-method-support)
    - [Requirements](chapters/ch06.07-ex-adding-http-methods.md#requirements)
    - [More details](chapters/ch06.07-ex-adding-http-methods.md#more-details)
    - [Example](chapters/ch06.07-ex-adding-http-methods.md#example)
    - [Hints](chapters/ch06.07-ex-adding-http-methods.md#hints)
    - [Solution](chapters/ch06.07-ex-adding-http-methods.md#solution)
  - [Adding HTTP methods to the Router](chapters/ch06.08-adding-verbs-api.md#adding-http-methods-to-the-router)
    - [Update the `TrieRouter` class](chapters/ch06.08-adding-verbs-api.md#update-the-trierouter-class)
  - [Ex. Implementing Dynamic Routing](chapters/ch06.09-ex-dynamic-routing.md#exercise-4-implementing-dynamic-routing)
    - [Why Dynamic Routing?](chapters/ch06.09-ex-dynamic-routing.md#why-dynamic-routing-)
    - [Anatomy of a dynamic route](chapters/ch06.09-ex-dynamic-routing.md#anatomy-of-a-dynamic-route)
    - [Challenge: Enhance the `TrieRouter` Class to Support Dynamic Routing](chapters/ch06.09-ex-dynamic-routing.md#challenge-enhance-the-trierouter-class-to-support-dynamic-routing)
    - [Visualisation of our `TrieRouter` structure](chapters/ch06.09-ex-dynamic-routing.md#visualisation-of-our-trierouter-structure)
    - [Summary](chapters/ch06.09-ex-dynamic-routing.md#summary)
  - [Running Our Server](chapters/ch06.10-running-our-server.md#running-our-server)
    - [Refactoring the `TrieRouter` class](chapters/ch06.10-running-our-server.md#refactoring-the-trierouter-class)
    - [Type Aliases](chapters/ch06.10-running-our-server.md#type-aliases)
    - [The `run` function](chapters/ch06.10-running-our-server.md#the-run-function)
  - [Building our first web-server](chapters/ch06.11-building-a-web-server.md#building-our-first-web-server)
    - [More refactoring](chapters/ch06.11-building-a-web-server.md#more-refactoring)
    - [Your first web server](chapters/ch06.11-building-a-web-server.md#your-first-web-server)
