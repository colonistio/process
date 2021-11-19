# Common Coding Mistakes

### Avoid Using While Loop

Read this: https://stackoverflow.com/questions/3875114/why-use-a-for-loop-instead-of-a-while-loop/3875142#3875142

### PR Too Long

An ideal PR size is between 5-10 commits. It can go up to 20. Expect any PR above 20 commits to be closed without being merged. https://vm.tiktok.com/ZSpbnDGP/

To better manage large pull requests or new edits for a pull requests, use a [squash merge](https://docs.microsoft.com/en-us/azure/devops/repos/git/merging-with-squash?view=azure-devops#what-is-a-squash-merge). A good example of this can be seen [here](https://github.com/colonistio/katan/pull/4629). Notice how each commit is from a separate branch with multiple commits of its own. A squash merge allows us to pack those commits into one, making the main pull request easier to manageable and to follow.

### PR Does Multiple Things

Always follow the "Single Responsibility Principle"

> The single responsibility principle is a computer programming principle that states that every module or class should have responsibility over a single part of the functionality provided by the software, and that responsibility should be entirely encapsulated by the class.

Just like classes and modules, pull requests should do only one thing.

Before submitting a PR for review, try applying the principle of single responsibility. If this code is doing more than one thing, break it into other Pull Requests.

Source: https://medium.com/@hugooodias/the-anatomy-of-a-perfect-pull-request-567382bb6067

### PR Not Descriptive

Imagine that the code reviewer is arriving in your team today without knowing what is going on, and even so, they should be able to understand the changes.

Title:

- Make a self-explanatory title describing what the pull request does.

Description: 

- Describe what was changed in the pull request.
- Explain why this PR exists.
- Make it clear how it does what it sets out to do. E.g: Does it change a column in the database? How is this being done? What happens to the old data?
- Use screenshots to demonstrate what has changed.

Good examples: https://github.com/colonistio/katan/pull/2960

Source: https://medium.com/@hugooodias/the-anatomy-of-a-perfect-pull-request-567382bb6067

### Use early breaks instead of if/else

Read: https://jamesmonger.com/2019/08/06/return-early-return-often.html
Read: https://raquo.net/2016/01/guard-statement-swift/

### Request review

When you edit something in a PR always re-request review https://prnt.sc/vk2shw

### Resolve conversation

After you finish implementing a suggestion resolve the conversation https://prnt.sc/vo06a2


### Commit Too Big

Break down your commits into the smallest commit that represents a cohesive feature that is in a build-able state.

Example: https://github.com/colonistio/katan/commit/d2c69b7ecd7aa7eaf822e493b09422b3d1668b34

This commit can be broken down into 

- Renaming the function
- Moving function elsewhere
- Changing where it was called from
- Cleaning it up
- Writing a patchnote

Merging big commits result in

- Extending review time
- Possibility of missing a problem during review
- Lower code quality

### Duplicate commit

When you want to move a certain code from one place to another never separate the commit into `add commit` and `remove commit`. They should be in a single commit which is a `move commit`

When the developer does an `add commit` in hopes of deleting the original code in the future, what they are actually doing is a `duplicate commit`. This makes the reviewers job harder by making him need to jump back and forth increasing the likely hood of him missing a potential flaw. This results in a bad code quality overtime resulting in bad product.

Example: https://github.com/colonistio/katan/pull/5033#discussion_r702648574

### Add Patch Note

- If you are changing logic, add it to PatchNoteData.ts. 
- If there is a relevant suggestion on [featureupvote](https://colonist.featureupvote.com), paste its link.
- If you're a contributor add Thanks (your_colonist_username) in there.
- If you're doing a big refactor add it to patch notes as hidden

Patch Notes allow the testers & players see what has changed, what to expect from the update. 

Hidden patchnotes help in 2 ways 
- making sure testers test those before releasing 
- if something breaks later on, its easier to search in the patchnote file and find the potential problem

### Other Resources
- [Clean Code](https://github.com/trantuyen1998/clean-code-javascript). A summarize version of the Clean Code book adapted to JavaScript.
- [Pull Requests and Commits](https://faun.pub/the-art-of-a-well-composed-pull-request-3815fc7e9610). Read this if you're having difficulty with commits or pull requests.