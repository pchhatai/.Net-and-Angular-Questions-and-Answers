# .Net-and-Angular-Questions-and-Answers
1. Observable vs Promise, when to use which one ?
   
Promises and Observables are both mechanisms for handling asynchronous operations in JavaScript, but they differ significantly in their capabilities and use cases.

Promises:
Single Value:

A Promise is designed to handle a single, future value or error. It represents an operation that will eventually complete, either successfully (resolved) or unsuccessfully (rejected).
Eager Execution:

A Promise starts executing immediately upon creation, regardless of whether a .then() or .catch() handler is attached.

Cannot Be Cancelled:

Once a Promise is initiated, it cannot be cancelled. The operation will run to completion.

Unicast:

A Promise is unicast, meaning it can only be consumed once. Subsequent calls to .then() on the same Promise instance will receive the same resolved value.

Observables:

Stream of Values:

An Observable can emit multiple values over time, representing a stream of data or events. It's well-suited for handling continuous asynchronous operations like real-time updates, user input events, or repeated API calls.

Lazy Execution:

An Observable is lazy; it only starts executing when a subscriber attaches to it using the .subscribe() method.

Cancellable:

Observables can be cancelled by unsubscribing from them. This allows for resource cleanup and prevents unnecessary operations.

Multicast (with Subjects):

While Observables are unicast by default (each subscription triggers a new execution), they can be made multicast using Subjects, allowing multiple subscribers to share the same execution and receive the same emitted values.

Operators:

Observables, particularly within libraries like RxJS, come with a rich set of operators (e.g., map, filter, debounceTime) that enable powerful data manipulation and transformation within the stream.
