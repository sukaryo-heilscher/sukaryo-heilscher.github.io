---
layout: essay
type: essay
title: "The Restraint of Standards"
# All dates must be YYYY-MM-DD format!
date: 2022-09-22
published: true
labels:
- Programming
- Code Standards
---

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

