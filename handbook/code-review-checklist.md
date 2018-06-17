# Code Review Checklist

## Items to be checked in a code review

Reviewing code is difficult, and in fact, it's a very broad task. According to my bosses, I'm considered a good code reviewer, but still, I think my effectiveness could be improved a lot. I think that following checklists, just in most of the cases, can be a huge help.

Now obviously, some of those checklists and/or tasks will be language specific. However what makes a review a good one are most of the time the same concepts, regardless of the language used.

These lists are mostly here to give you some ideas, they are far from complete. Feel free to use them, update them, personalize them or just let them inspire you to come up with completely new ones.

I think that one reviewer shouldn't use them all, but maybe just a few. But if you have separate checklists, it's easy to share the tasks.

Please, consider that not all the checklists are there to be used for all the code reviews. If the pull request is a really small bugfix, just correcting an off-by-one in a condition, it will not require checking the design of the whole domain.

### Full process checklist

- [ ] Are new unit/regression tests added?
- [ ] Are there new compiler warnings?
- [ ] Does the change functionally make sense?
- [ ] Are there a lot of dependencies?
- [ ] Are the commit message clean?

### SOLID (object-oriented design) principles checklist

- [ ] Single responsibility principles
- [ ] Open/closed principle
- [ ] Liskov substitution principle
- [ ] Interface segregation principle
- [ ] Dependency inversion principle

### Security checklist

- [ ] Is external input handled properly?
- [ ] Are C-style interfaces used?
- [ ] Is the `new` operator superfluously used instead of stack allocation?
- [ ] Are there lots of (error-prone) size calculations?
- [ ] Are pointers used a lot?
- [ ] Are shared_ptrs used a lot?
- [ ] Are there any threads?

### Testing best practices checklist

- [ ] Are there enough unit tests?
- [ ] Are there enough non-regression tests?
- [ ] Do tests test one thing?
- [ ] Do they have assertions? (A test might have multiple assertions, still logically they assert one thing)
- [ ] Are they readable?
- [ ] How dates are used? (Fixed vs. generated)

### Code readability checklist

- [ ] Are names meaningful?
- [ ] Are classes/functions small enough?
- [ ] Does the code "read like a prose"?
- [ ] Is the code well-formatted?
- [ ] Is there duplicated code?

### Resource handling checklist, a.k.a. 

- [ ] Is object ownership clarified?
- [ ] Are objects properly destroyed/ is the memory correctly deallocated?
- [ ] Are new fields properly handled?
- [ ] Are Fields correctly initialized in the constructors?
- [ ] Are comparision operators updated?

--- 

##### Forked and adapted from https://github.com/sandordargo/code-review-guidelines