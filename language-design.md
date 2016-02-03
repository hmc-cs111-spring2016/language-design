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

"...Perl, a major programming language used by untold zillions of developers, is no more intuitive to novices than a language with a randomly generated syntax."

I definitely disagreed with Pavlus' article, especially the claim quoted above. From my experience on the OCM project, I know that it can be hard to do studies on languages. Even though OCM was better from the standpoint of someone who was actually acquainted with parallel programming, it was hard to use novices to show this. User studies over the years have been problematic and it's very hard to teach people parallel programming over the course of half an hour or so. There are also a lot of problems with the idea of using novices to judge a language when they make up a very small portion of the userbase. Not all languages are designed to be easy to learn or to be very user friendly. In fact, I think it would be counterintuitive for most programming languages to have ease of use for novices as a primary concern. User-friendly languages will have to be more verbose than regular languages and will make doing just basic tasks a chore. In the example given in the article, a for loop in Quorum will take twice as many lines as C and about double to triple the number of characters. While languages like Quorum or Scratch may be more accessible to novices, they would likely hinder the productivity of most programmers in the long run. It's also worth noting that the paper only used a sample size of 18 people whose average age was 21. Even if the results were statistically significant, 18 people is a pretty small sample size. Their sample also probably don't represent many of the people learning to code, especially since many coding novices are significantly younger than 21.

"I stand on this claim: I should not design a small language, and I should not design a large one. I need to design a language that can grow."

While the _Growing a Language_ article was interesting, I think the exact opposite advice applies when creating DSLs. In a general purpose programming language, growth is definitely important. You can't think of everything people will want to do with your language, and, even if you could, it would be overwhelming to include all that functionality. However, things are very different with a DSL. Since DSLs limit programmers to a specific domain, it's much easier to predict the functionality programmers will need to solve problems in that domain and to bake most of this functionality into the language from the beginning. This is highly desirable becuase people using DSLs want to work with abstractions that are natural, accurate, and relevant to them, but they don't want to (or can't) implement these abstrations themselves. While it may be useful to start off with a relatively small DSL, it will be important to have core features available from the start as programmers may not be able to add the features themselves and the DSL will likely be too limited to add the functionality from within its domain.

"APIs should be easy to use and hard to misuse. It should be easy to do simple things; possible to do complex things; and impossible, or at least difficult, to do wrong things."

This is something I'd like to know more about. It seems like almost every language gets something wrong that they later regret, but how do you avoid these kinds of mistakes in the first place? Some things are fairly straightforward; for example, Joshua Bloch suggests to "provide programmatic access to all data available in string form" and to "avoid return values that demand exceptional processing". However, some mistakes are much more subtle and hard to predict, especially when logic errors are already easy enough in general purpose programming languages. Is there an easy and/or straightforward way to design APIs, DSLs, and GPPLs so as to minimize some of the more complex errors that are common for programmers? Perhaps we could discuss this sometime in class.

---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

There are a lot of characteristics to a well-designed language. Although, I think pretty much all of them can be boiled down to one thing: productivity. Many of the properties of programming languages (or lack thereof) that Guy Steele supports would enhance user productivity, including starting them small and designing them to be able to be grown by their users. However, this may be quite unintuitive as many people would suspect that it would be easier to get more things done if you spent less time adding features. However, when a languages has too many features built in, it can become overwhelming to understand. Modern versions of C++ have become this way to some degree. There are so many advanced features now that C++ can do pretty much anything. Some of it looks like Python, some of it looks like C, and some of it is hard to decipher without already being familiar whith what the code is supposed to do. This actually hinders productivity because it becomes harder to maintain code as users are free to implement their programs in a wide variety of ways. One solution to this is to move functionality out of the core language and into standard libraries that are easily accessible. This way users can still access these features if they need them, but there is almost an implicit discouragement to do so if the libraries are not necessary. While C++ is pretty good about this, it can make it hard to include all but the simplest of external libraries. This has encouraged people to put all of their library code into a single, easy-to-include file rather than breaking it down into files and folders like they normally might. The ability to grow a language also contributes to productivity. By making it easy to extend a language's core functionality, programmers can better integrate libraries into their code and take advantage of the features they bring without having to sacrifice readability. Other features that Guy Steele mentioned, like generics and method overloading, also help to simplify and speed up the process of integrating more functionality into the language, therefore increasing programmer productivity.

Many of Joshua Bloch's tips on how to create a well-designed API would also increase user productivity. If we made APIs "easy to use," "hard to misuse," and "self-documenting", programmers would save time on doing basic tasks, fixing bugs, and looking up method names and parameters. While there are plenty of other tips other than these three, if you look at his list, almost all of them will clearly increase user productivity in one way or another.

Finally, even the discussion on Verou's post has to do with user productivity, whether the commenters knew it or not. Users brought up how it was ambiguous what 0% and 100% gray meant (i.e. which was black and which was white) and suggested method names like rgb, luma, or grayscale because they were already familiar with them and they had established meanings (which would result in less errors when using them and potentially less time spent looking through documentation to find their method name). The post itself takes Joshua Bloch's advice to "show your design to as many people as you can, and take their feedback seriously. Possibilities that elude your imagination may be clear to others." What's intuitive to those who took the survey and/or commented on the article will likely be intuitive to a good number of the programmers using CSS as well. And, when programming languages are more intuitive, programmers save time because they make less mistakes and can read code faster and more accurately, thus increasing their productivity.

---

**Question**

How do the themes of _Growing a Language_ relate to the lab we did this week?

**Response**



---
 
**Question**


In what way is an API a language? 

**Response**

APIs are actually a lot like DSLs, especially internal ones. In fact, they actually match Fowler's definition of a DSL quite well. They are used by people to give instructions to computers. Good APIs should also have the fluency and feel of a programming languages. This is backed up by Joshua Bloch, who wrote "strive for intelligibility, consistency, and symmetry [in APIs]. Every API is a little language, and people must learn to read and write it. If you get an API right, code will read like prose." APIs generally have limited expressiveness. Even if they are pretty flexible, APIs usually to carry out their operations through another piece of software or on another computer, which is kind of a limited domain in and of itself. I think it would follow that APIs will also have the domain focus that Fowler mentions as his last characteristic of a DSL. The whole purpose of using an API is because it's better at what you're trying to than the GPPL that it's implemented in.

APIs also fit some of the descriptions of DSLs that we talked about in class. While some APIs may be Turing complete, they generally focus on making only specific tasks easy. This is because they are both designed (and generally used) for doing these particular tasks. Since APIs are commonly implemented as libraries, this also means they have a host language (which is the language they are a library for).

I think it's also pretty intuitive that APIs are a (programming) language. They have their own vocabulary, which is made up of the names of their public methods, and they have their own syntax, which may be limited and/or determined by the host language. Good APIs will also have their own grammar and/or style that makes the methods coherent and work well with each other. As Joshua Bloch wrote, a good API should "use consistent parameter ordering across methods" and "should rarely require documentation to read code written to [it]. In fact, it should rarely require documentation to write it."

---

**Question**

What does the post on grayscale tell us about the process of API design?

**Response**



---

**Question**

The comments on the Pavlus article seem to set up a conflict between
professional programmers and everyone else. What is the essence of this
conflict? Do you sympathize more with the substance of the article's arguments
or with the substance of the majority of the commenters' arguments? Do you
sympathize more with the tenor of the article or the tenor of the majority of
the commenters?

**Response**

The problem that came up in the comments in Pavlus article is actually present in a variety of different situations. For instance, in academic paper writing, authors often have to choose between using disciplie-specific jargon (which allows them to quickly and succinctly convey their ideas to individuals in their field) or language that is accessible to a general audience (which will be much more verbose and will therefore take much longer to write). While it would be great if everyone could understand scientific papers, it's not very efficient for scientics to have to explain concepts that most of their peers already know if their papers will largely be read by their peers. While this can be taken to an extreme (where authors rely so heavily on using terms specific to their kind of work that they isolate themselves from all but a handful of colleagues in their field), this practice generally helps save a significant amount of time on what is often already a quite lengthy process. The key is to find a balance that allows for quick writing but that maintains readability for most of the target audience.

This is what I think should be the case for programming languages. Most PLs should not cater to the lowest denominator (and read like a book). It is already hard enough to navigate code and making it more verbost will not help that. However, creators of PLs should strive to encourage readability and clarity so that it is easy for programmers who are familiar with the language to understand each other's code. If code in a language easily becomes too dense or "WORN" (write once, read never), then its maintainability (and therefore efficiency) will be severely impacted.

I think user Strengthiness does a good job of summarizing my opinion on this issue: "...there's a reason why programming languages professional programmers use are precise and terse (-ish…). A language like Quorum may be good for learning programming concepts, but as an everyday tool for a professional programmer it would be so overly verbose as to just slow one down. Our languages may be esoteric and the tools hard to master, but show me any other technical profession where tools are straightforward to learn and mastery comes easily." I also agree with User Mjaksen that even if we tried to make programming languages more approachable, it would cause more complications, leading Mjaksen to conclude "there \*really\* is no pleasing everyone" (which Joshua Bloch agrees with as well when it comes to APIs). User Simon also makes an excellent point that reafirms what user Strengthiness wrote above: "The issue with writing software is not being able to program; it's being able to program \*well\*. There are a number of languages out there which have been specifically designed to be easier to write for novice programmers. What generally ends up happening is that novices then end up writing software, and the quality of the end product suffers as a result. I'm not knocking novices -- we were all novices at one point -- but I guess most companies have got somewhere an Access database system or simple VB6 program that they rely on for some task but which is woefully inadequate, or worse, a security minefield, because it was written by someone who didn't really understand the technical issues." Perhaps the problem is not that programming languages are too hard, but that there currently isn't enough technical training on how to use them (and especially on how to use them well).

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



---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**



---
