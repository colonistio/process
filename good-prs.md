# Good PRs

Here are the most common reasons for edit requests on PRs, try not to repeat them: 

1. If you're changing logic, run tests before and after to make sure nothing broke
2. If you're changing logic, add it to patch note, find if there is a relevant suggestion and paste it's link: https://colonist.featureupvote.com/ . If you're a contributor add Thanks (your_colonist_username) in there
3. Branch naming convention: `your_short_name/feature-description`
4. Run linter on all files you edited before pushing the PR
5. If you just remembered a line of code that should've been added to the last commit, you should amend that line to last commit here: https://prnt.sc/v0t4ld
6. Complex if cases: https://prnt.sc/2012517 https://github.com/colonistio/katan/pull/2241#discussion_r460682386
7. When you're putting in temporary, optional or confusing code, leave a comment like this: https://prnt.sc/20125e9 https://github.com/colonistio/katan/commit/9a6c69fba1cc078e77d67c58ca3171d6749da887
8. If you're doing a big refactor add it to patch notes as hidden
9. After completing a PR, search github issues to see if there are duplicates
10. When making UI changes, add a picture/gif/video to the PR. Examples: https://gyazo.com/4997de6899c05cf1502cc84caff95ca3 https://gyazo.com/8b4f824090490fcd72a33e0b2cc5bd35 https://github.com/colonistio/katan/pull/2687#issue-503748145 https://github.com/colonistio/katan/pull/2648#issue-500907194
11. Try to use static variable types when you can
12. Aim to reduce code complexity, prioritize: read time > write time
13. Think hard on variable and function names 
14. Make sure each function has a specific purpose, if you find you can’t name a function easily it is often a sign that it is not cohesive enough
15. Write tests if your code has nested for loops: https://prnt.sc/20127k6 https://prnt.sc/20127s7 https://github.com/colonistio/katan/pull/2745/files#r512132539
16. Try to break multiple PRs into smaller ones: https://prnt.sc/20128hp https://github.com/colonistio/katan/pull/2856#issuecomment-723824822
