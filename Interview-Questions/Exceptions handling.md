## How do we handle exceptions in C#(try/catch)?

In C#, exceptions are handled using `try`, `catch`, and optionally `finally` blocks. The `try` block contains code that may throw an exception, while the `catch` block allows us to handle specific exceptions gracefully. A `finally` block is often used for cleanup tasks, such as closing files or releasing resources, and it executes regardless of whether an exception occurred.


From a best-practice perspective, I always prioritize catching specific exceptions first—for example, `FileNotFoundException` or `SqlException`—before falling back to a general `Exception` catch. This ensures that error handling is precise and avoids masking issues. I also avoid empty `catch` blocks, since they can swallow errors silently and make debugging difficult.


