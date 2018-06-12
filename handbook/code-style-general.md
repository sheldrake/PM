# Coding Style General Guidelines

Writing readable code is an art and following style guides is one way of ensuring our code is always clean, readable and consistent. Language specific style guides exist but general coding standards apply to all programming languages.

These are not to be blindly followed; strive to understand these and ask when in doubt.

### General

Writing code to follow best practices is at the heart of good coding practice.

- **DRY (Don’t Repeat Yourself):** code should be DRY. Just like earlier mentioned, you need to ask the question “Is there redundant or duplicate code?”. Ensure that unnecessary repetitions don’t exist within the code base.
- **Object Oriented Programming:** follow [SOLID principles](http://code.tutsplus.com/series/the-solid-principles--cms-634) for writing object oriented programs. At the very least, we should ensure that programs have high cohesion and loose coupling.
- **Documenting Code:** code is expected to be thoroughly documented. Always use doc style comments if possible but also write code in a way that you may require little or no comments.
- **Separation of Concerns:** technically, you could write an entire application code within a single file. But that would prove to be a nightmare to read and maintain. Ensure that your code is always broken into logical containers, properly arranged within folders. This makes it far easier to navigate through your codebase.

### Naming

- Make use of meaningful variable names. Avoid abbreviations.
- Avoid object types in names (`user_array`, `email_method`, `CalculatorClass`, `ReportModule`).
- Prefer naming classes after domain concepts rather than patterns they implement (e.g. `Guest` vs `NullUser`, `CachedRequest` vs `RequestDecorator`).
- Name the enumeration parameter the singular of the collection. e.g when looping over a collection of books, say for book in books and not for b in books. It’s clearer this way.
- Name variables created by a factory after the factory (`user_factory` creates user).
- Name variables, methods, and classes to reveal intent. Intent describes the function of the class, method or variable. A typical example is if we were describing a class method to sort a collection by a certain parameter. It’s preferred to define this as `obj.sort_by(param)`. It makes code more readable and require less documentation.
- Treat acronyms as words in names (`XmlHttpRequest` not `XMLHTTPRequest`), even if the acronym is the entire name (class Html not class HTML).
- Suffix variables holding a factory with `_factory` (`user_factory`)

### Formatting

- Avoid inline comments.
- Avoid deep indentation.
- Break long lines after 80 characters.
- Delete trailing whitespace.
- Don't include spaces after `(`, `[` or before `]`, `)`.
- Don't misspell.
- Don't vertically align tokens on consecutive lines.
- Do not leave commented out code within production code.
- If you break up an argument list, keep the arguments on their own lines and closing parenthesis on its own line. [Example 1](https://github.com/andela/code-review-guidelines/tree/master/style/ruby/sample.rb#L2), [Example 2](https://github.com/andela/code-review-guidelines/tree/master/style/ruby/sample.rb#L10).
- If you break up a hash/dictionary/associative array, keep the elements on their own lines and closing curly brace on its own line.
- Indent continued lines two spaces.
- Indent private methods equal to public methods.
- If you break up a chain of method invocations, keep each method invocation on its own line. Place the `.` at the end of each line, except the last. Example.
- Use 2 space indentation (no tabs) or indentation specific to your stack.
- Use an empty line between methods or the required number of spaces specified in the respective style guide.
- Use empty lines around multi-line blocks.
- Use spaces around operators, except for unary operators, such as `!`.
- Use spaces after commas, after colons and semicolons, around `{` and before `}`.
- Use [Unix-style line endings](http://unix.stackexchange.com/questions/23903/should-i-end-my-text-script-files-with-a-newline) (\n).
- [Use uppercase for SQL keywords and lowercase for SQL identifiers](http://www.postgresql.org/docs/9.2/static/sql-syntax-lexical.html#SQL-SYNTAX-IDENTIFIERS).

### Code Organization
- Ensure to always take advantage of inbuilt language functionality like packages, modules etc. to organise the different parts of your code.
- Order methods so that caller methods are earlier in the file than the methods they call.
- Order methods so that methods are as close as possible to other methods they call.

### Code Performance

We need to be observing things that can possibly make a program slow or perform sub-optimally in production. Things to watch out for include the following:

- **Complexity:** Watch out for nested for loops. It’s not always a bad thing but see if there are ways to refactor code like this to be less complex. It is important to create an awareness in the reviewee to always look for ways to optimize the running time of their code. 
- **Efficiency:** Encourage the use of better data structures or faster algorithms to solve problems. A typical example of this would be using a dictionary for grouped data instead of using multiple lists or declaring unnecessary variables.
- **Memory management:** Instill a mindset in the reviewee to always think about ways to optimize memory usage in their code. An Android Developer for instance should be encouraged as much as possible to ensure to cleanup afterwards to ensure there are no unused variables and memory leaks. Scenarios?
- **Design Patterns:** Design patterns besides being accepted ways of solving repetitive problems can also lead to more efficient programs in terms of time and space. Wherever applicable, ensure reviewees are applying design patterns to solve general repetitive problems.
 
--- 

##### Forked and adapted from https://github.com/andela/code-review-guidelines