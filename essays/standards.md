---
layout: essay
type: essay
title: "Coding Standards: Juice Not Worth the Squeeze"
# All dates must be YYYY-MM-DD format!
date: 2022-09-22
published: true
labels:
- Programming
- Code Standards
- ESLint
---

<img width="150px" class="rounded float-start pe-4" src="../img/juice.jpg">

_Tedium_

That simple word alone adequately describes my experience with the code analyzing tool ESLint. Just when I've wrapped up coding a program and am preparing to submit it, ESLint has to rear their ugly head to point out the three spaces I didn't bother to place. Yeah, thanks mate. We really avoided a catastrophe there. My code would've been utterly incomprehensible otherwise. 

Now I know this seems strange coming from the guy who was [yapping up a storm](https://sukaryo-heilscher.github.io/essays/javascript.html) about the lack of structure in Javascript compared to Java. The difference is that in Java, the structure served a clear purpose, but with ESLint, the juice just isn't worth the squeeze.

## The Juice

Nitpicks's are all that ESLint has to say to me. Now, I can admit that my code does look a little nicer with the extra space before the curly braces and around some operators. However, it's only a _little_ nicer. It was still perfectly readable beforehand, and I'd argue that some things actually looked better.

```
Pre-ESLint:

  for (let i = 2; i < 50; i++) {
    fibNums.push(fibNums[i-2] + fibNums[i-1]);
  }

Post-ESLint:

  for (let i = 2; i < 50; i++) {
    fibNums.push(fibNums[i - 2] + fibNums[i - 1]);
  }
```

Here, having no spaces in "[i-1]" makes it clear that it serves as a singular index rather some complex operation. It's similar to how negative x is written as "-x" rather than "(-1) * x". Of course, if there really were some complex operation being conducted on i involving multiple operators, then the spaces would be justified. For singular operators though, it's better without.

## The Squeeze

In the opening paragraph, I detailed the tedium induced by ESLint at the end of a project, complaining about various menial errors. However, clicking through and accepting the proposed solutions is nothing compared to getting ESLint set up in the first place. 

First, 3 files need to be added to the project: .eslintrc.js, package.json, and .gitignore. Then run "npm install" in order to get some additional files set up, except now there's some strange errors popping up. After a bit of Googling, turns out the NPM installed is too recent so "npm install eslint@8.22.0 --save-exact"  has to be run instead. Certainly doesn't help that the built-in terminal on IntelliJ has no idea what the Helvetica Standard npm is, necessitating the use of Windows Powershell to navigate to the project location and finally run the accursed line of code.

Now, I'll confess, it's really not that bad. After getting familiar with the process, it takes maybe a minute or two. BUT, it is tedious. So bloody tedius. And for what? To be told I'm missing a few space? Even though the squeeze isn't all that bad, it's still not worth the effort.
