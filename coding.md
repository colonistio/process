# Coding

### General Rules

1. Never work on the master or staging branches
2. Always work on a custom branch dedicated to your feature
3. Name branches in this format `your_short_name/branch-name` ex: [goktug/new-docs](https://github.com/colonistio/katan/pull/2877)
4. Create a PR (Pull Request) for every change and request a review from either /demiculus (for frontend) or /goktugyil (for backend) or both
5. Try to play around the code and discover how it works by yourself as much as possible
6. Use the discord contributors section to ask your questions. Make sure to have exhausted all your options before asking questions. I.e. googled the problem, tried out the code in various ways etc.. we're always around to help out when you're stuck.
7. Write unit tests whenever you can
8. If a code/logic is hard to understand first create a PR that refactors that part of the code, once its approved create the new feature
9. Create Issues for projects changing significant parts of the code or is a mid & long term project. The aim of issues is to let others know that something is being worked on and discussing about its design. There is no need to create an issue for a small PR you're going to fix quickly that won't effect others code. 
10. Follow your notifications on github and make sure to check out their type so you don't miss anything important https://prnt.sc/w3kshv

### Pull Request Rules

1. Huge commits are unreadable. Small commits are hard to follow the flow. https://github.com/colonistio/katan/pull/4357#issuecomment-857285851
2. Each commit needs to have minimum amount of changes, so it is readable and reviewable. Ideally only 1 function or file should change in a commit https://vm.tiktok.com/ZSpbnDGP/
3. Try to find the smallest standalone piece you can can commit (Import deletion, small utility function, changing a parameter name, add a new parameter, etc..)
4. We want clean PRs. So any `whops forgot ..`, `fix typo` etc. should be (cleaned locally)[https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History] before pushed to github PR. 
5. Every change that you do should be added to PatchNoteData.ts under your name. When we are creating a new build we organize them. 
6. If a PR has been active for 14 days and not been merged it should be closed and opened a new one.

### Large Update Rules

1. If you're doing a big feature, first create a branch, do a rough version of the feature that works, without worrying much about commit readability and architecture
2. Push that branch to Github as a draft PR
3. Review your commit at PR UI from the eye of reviewer 
4. Give yourself stuff to fix, like change var name, separate variables, split function into multiple, do better architecture, etc..
5. Then create a todo list, and how could the architecture have been done cleanly
6. Create a new branch
7. Start moving code to new branch and rewrite everything but in a clean, final way
8. If this feature will require multiple PRs, then create a general PR, then write code in parts in the PRs. Example: https://github.com/colonistio/katan/pull/3946

### Code Complete Tips

Program defensively: recognize that mistakes will be made and program in such a way that catches and handles those mistakes as quickly as possible
- Anticipate change
- Aim to reduce complexity so that the code chunk you are working on can be handled in memory easily 
- Limit for/if/completion nesting to three levels
- Use familiar widely accepted conventions
- Avoid global data
- Consider multiple designs before settling on one, don’t go with the first
- Avoid using while loop

Ways to manage complexity:
- Prioritize read time over write time
- Make sure each function has a specific purpose, if naming is hard, function is bad
- Think hard about public interfaces
- Think about parts that are likely to change and hide the details away through an interface
- Hierarchy (when possible, structure code in such a way that the more general code sections cover more specific parts. e.g: data stores class, which includes db connector objects to mysql, redshift, etc)
- Separate conceptually different parts into different code sections (like ui, db, etc.)
- Modularize more
- Try to shift names from cs internal implementations to semantic meaning (valid_db_entry > status flag)
- Make sure routine names holistically capture the purpose of the method
- When possible, prefer specific names instead of typical loop variable names (index > i)

