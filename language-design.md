_Fill in each this file with your responses, placing each response after its
corresponding question._

---

**Question**

Pick three quotes from the readings about language design. Good candidates 
are:

   + Something you agreed with / resonates with your own experience
   + Something you disagree with
   + Something that is interesting, a new idea or perspective you'd like to remember
   + Something you didn't understand

For each quote, describe what it was about the quote that led you pick it.

**Response**

"Does this mean, then, that it is of no use to design? Not at all. But in stead of
designing a thing, you need to design a way of doing. And this way of doing must make
some choices now but leave other choices to a later time."

"If we add hundreds of new things to the Java programming language, we will have
a huge language, but it will take a long time to get there. But if we add just a few
things—generic types, overloaded operators, and user defined types of light weight, for
use as numbers and small vectors and such—that are designed to let users make and add
things for their own use, I think we can go a long way, and much faster. We need to put
tools for language growth in the hands of the users."


---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

-- steele: language has to GROW
-- steele: defines only what you need
-- pavlus: intuitive to learn and read
-- bloch: things are named correctly/easily

---

**Question**

How do the themes of _Growing a Language_ relate to the lab we did this week?

**Response**

-- you introduce features/ideas as you need them
-- you start in an existing framework and expand based on the use case you want
-- poorly implemented but intuitive > well implemented and difficult to expand (APL example)

---
 
**Question**


In what way is an API a language? 

**Response**

JOSH

---

**Question**

What does the post on grayscale tell us about the process of API design?

**Response**

JOSH

---

**Question**

The comments on the Pavlus article seem to set up a conflict between
professional programmers and everyone else. What is the essence of this
conflict? Do you sympathize more with the substance of the article's arguments
or with the substance of the majority of the commenters' arguments? Do you
sympathize more with the tenor of the article or the tenor of the majority of
the commenters?

**Response**

JOSH

---

**Question**

The Pavlus article mentions the researchers' comments that people preferred
"natural-language replacements for some of the more abstruse syntax". In other 
words, people found it easier to work with code that looks more like a human language (e.g.,
English). Consider the following quote by William R. Cook, one of the creators
of AppleScript:


> The experiment in designing a language that resembled natural languages (English
> and Japanese) was not successful. It was assumed that scripts should be
> presented in “natural language” so that average people could read and write
> them. … In the end the syntactic variations and flexibility did more to confuse
> programmers than to help them out. It is not clear whether it is easier for
> novice users to work with a scripting language that resembles natural language,
> with all its special cases and idiosyncrasies. The main problem is that
> AppleScript only appears to be a natural language: in fact, it is an artificial
> language, like any other programming language. … even small changes to the
> script may introduce subtle syntactic errors that baffle users. It is easy to
> read AppleScript, but quite hard to write it.
[[Cook 2007, page 1-20]](https://dl.acm.org/citation.cfm?doid=1238844.1238845)

Are these two experiences of natural languages at odds with one another? Would
you choose to include natural language in the design of a DSL? If so, how might
you do so? If not, why not?

**Response**

-- the closer you get to natural language, the more of an expectation you have to use it LIKE natural language
	- in that way, it seems that you should be careful with how much natural language you want to use
		- i would want to avoid associations with phrases and really common words
			- counter: loop. we don't use loop often so its ok as a programming word
-- i would be VERY careful using natural language in the design of a dsl
	- wouldn't go further than a word that evokes a certain feeling or purpose
	- don't want to create false expectations
-- verbose method names etc are good programming practice, but the language itself shouldn't be projecting its expectations of natural language

---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**



---
