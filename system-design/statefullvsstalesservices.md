does the server need to remeber an earlier interaction to handle your next request

A stateless backend can work with saved data. It just doesn’t require a particular backend instance to remember your previous requests.

Also, more CPU cores do not automatically make every program faster. For example, a single Node.js process generally executes your JavaScript on one main thread. To use additional cores for JavaScript execution, you may need multiple processes or worker threads.