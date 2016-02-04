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

"...Perl, a major programming language used by untold zillions of developers, is no more intuitive to novices than a language with a randomly generated syntax." [Pavlus, 2012]

I definitely disagreed with Pavlus' article, especially the claim quoted above. From my experience on the OCM project, I know that it can be hard to do studies on languages. Even though OCM was better from the standpoint of someone who was actually acquainted with parallel programming, it was hard to use novices to show this. User studies over the years have been problematic and it's very hard to teach people parallel programming over the course of half an hour or so. There are also a lot of problems with the idea of using novices to judge a language when they make up a very small portion of the userbase. Not all languages are designed to be easy to learn or to be very user friendly. In fact, I think it would be counterintuitive for most programming languages to have ease of use for novices as a primary concern. User-friendly languages will have to be more verbose than regular languages and will make doing just basic tasks a chore. In the example given in the article, a for loop in Quorum will take twice as many lines as C and about double to triple the number of characters. While languages like Quorum or Scratch may be more accessible to novices, they would likely hinder the productivity of most programmers in the long run. It's also worth noting that the paper only used a sample size of 18 people whose average age was 21 [[Stefik et al., 2011, p 5](http://ecs.victoria.ac.nz/foswiki/pub/Events/PLATEAU/2011Program/plateau2011-stefik.pdf)]. Even if the results were statistically significant, 18 people is a pretty small sample size. Their sample also probably don't represent many of the people learning to code, especially since many coding novices are significantly younger than 21.

"I stand on this claim: I should not design a small language, and I should not design a large one. I need to design a language that can grow." [Steele, 1998, p 5]

While the _Growing a Language_ article was interesting, I think the exact opposite advice applies when creating DSLs. In a general purpose programming language, growth is definitely important. You can't think of everything people will want to do with your language, and, even if you could, it would be overwhelming to include all that functionality. However, things are very different with a DSL. Since DSLs limit programmers to a specific domain, it's much easier to predict the functionality programmers will need to solve problems in that domain and to bake most of this functionality into the language from the beginning. This is highly desirable becuase people using DSLs want to work with abstractions that are natural, accurate, and relevant to them, but they don't want to (or can't) implement these abstrations themselves. While it may be useful to start off with a relatively small DSL, it will be important to have core features available from the start as programmers may not be able to add the features themselves and the DSL will likely be too limited to add the functionality from within its domain.

"APIs should be easy to use and hard to misuse. It should be easy to do simple things; possible to do complex things; and impossible, or at least difficult, to do wrong things." [Bloch, 2006, p 1]

This is something I'd like to know more about. It seems like almost every language gets something wrong that they later regret, but how do you avoid these kinds of mistakes in the first place? Some things are fairly straightforward; for example, Joshua Bloch suggests to "provide programmatic access to all data available in string form" and to "avoid return values that demand exceptional processing". However, some mistakes are much more subtle and hard to predict, especially when logic errors are already easy enough in general purpose programming languages. Is there an easy and/or straightforward way to design APIs, DSLs, and GPPLs so as to minimize some of the more complex errors that are common for programmers? Perhaps we could discuss this sometime in class.

---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

We differed slightly in our opinions on this topic, so both of us wrote a response.

Milo:

For the most part, I agree with Steele’s claim that a well-designed language will be implemented with growth in mind.  He argues that with the vast number of features that modern language users require, it is simply not possible to code comprehensive languages all at once [Steele, 1998, p 5].  Thus, the key to good general purpose language design is to design for future growth.  When developers empower users to extend a language’s functionality to suit the community’s needs, a language could theoretically never become obsolete.  A specific symptom that Steele puts forth to gauge a language’s growth potential is whether or not “new words” (i.e. data types?) defined by users look like the primitive types implemented by the original developers, like they do in Lisp [Steele, 1998, p 5].  


Steele also strongly believes that a good language will have strong library support, and a user can pick and choose the libraries they need much like one would shop at a shopping mall, “where there are not quite as many choices [as a bazaar] but most of the goods are well designed and sellers stand up and back what they sell.”   Having not too many choices is important, as it can be frustrating having to choose from multiple libraries that accomplish the same task.


Interestingly, in the article about Quorum, Pavlus makes the implicit claim that well-designed languages should have very low learning curves.  This is not a statement that we agreed with, as there needs to be a balance between ease of use and long term productivity (more on this later).


A poorly designed language is one that does not design for growth.  A symptom would be that the language requires intensive and very low-level hacking in order to make changes to the language that look natural.  Steele uses APL as an example, complaining that there was “no way for a user to grow the language in a smooth way” [Steele, 1998, p 6]. 



Joshua:

There are a lot of characteristics to a well-designed language. Although, I think pretty much all of them can be boiled down to one thing: productivity. Many of the properties of programming languages (or lack thereof) that Guy Steele supports would enhance user productivity, including starting them small and designing them to be able to be grown by their users. However, this may be quite unintuitive as many people would suspect that it would be easier to get more things done if you spent less time adding features. However, when a languages has too many features built in, it can become overwhelming to understand. Modern versions of C++ have become this way to some degree. There are so many advanced features now that C++ can do pretty much anything. Some of it looks like Python, some of it looks like C, and some of it is hard to decipher without already being familiar whith what the code is supposed to do. This actually hinders productivity because it becomes harder to maintain code as users are free to implement their programs in a wide variety of ways. One solution to this is to move functionality out of the core language and into standard libraries that are easily accessible. This way users can still access these features if they need them, but there is almost an implicit discouragement to do so if the libraries are not necessary. While C++ is pretty good about this, it can make it hard to include all but the simplest of external libraries. This has encouraged people to put all of their library code into a single, easy-to-include file rather than breaking it down into files and folders like they normally might. The ability to grow a language also contributes to productivity. By making it easy to extend a language's core functionality, programmers can better integrate libraries into their code and take advantage of the features they bring without having to sacrifice readability. Other features that Guy Steele mentioned, like generics and method overloading, also help to simplify and speed up the process of integrating more functionality into the language, therefore increasing programmer productivity.

Many of Joshua Bloch's tips on how to create a well-designed API would also increase user productivity. If we made APIs "easy to use," "hard to misuse," and "self-documenting", programmers would save time on doing basic tasks, fixing bugs, and looking up method names and parameters. While there are plenty of other tips other than these three, if you look at his list, almost all of them will clearly increase user productivity in one way or another.

Finally, even the discussion on Verou's post has to do with user productivity, whether the commenters knew it or not. Users brought up how it was ambiguous what 0% and 100% gray meant (i.e. which was black and which was white) and suggested method names like rgb, luma, or grayscale because they were already familiar with them and they had established meanings (which would result in less errors when using them and potentially less time spent looking through documentation to find their method name). The post itself takes Joshua Bloch's advice to "show your design to as many people as you can, and take their feedback seriously. Possibilities that elude your imagination may be clear to others." What's intuitive to those who took the survey and/or commented on the article will likely be intuitive to a good number of the programmers using CSS as well. And, when programming languages are more intuitive, programmers save time because they make less mistakes and can read code faster and more accurately, thus increasing their productivity.

---

**Question**

How do the themes of _Growing a Language_ relate to the lab we did this week?

**Response**

An overarching theme of Growing a Language was of limited development time.  Because developers cannot predict all the requirements that users of their language might have, some development choices must be left to a later time [Steele, 1998, p 9].  Trying to accomplish everything with a language out the gate would take so long that your language would likely become obsolete before it’s complete.  In our lab we were similarly constrained by time, as we had only thirty minutes to design our approach and implement whatever we could.  In order to achieve anything in such a short amount of time, an approach that we discussed was starting with small pieces and building up (the lab guidelines urged us to “use a limited set of tools”).  This relates to general language design where, simply put, one must “add to the small language to make a language that is more large” [Steele, 1998, p 4]. 


On the theme of growth, however, Growing a Language and our lab differ.  Steele is adamant that “designing a language should be a plan for growth” [Steele, 1998, p7].  During our lab, however, rather than focusing on growth we were told to design with a specific user base in mind and to think about what exactly that user base want to do with our DSL.  This difference in designing DSLs and general purpose programming languages makes a lot of sense.  While a DSL is meant to solve a specific problem present at the time of the making of the DSL, general purpose programming languages are supposed to be able to solve unforeseeable problems that might arise in the future.  While DSLs can certainly grow to meet the changing needs of their users, growing in certain ways can put the DSL in danger of becoming general purpose.  An example is Context Free, which [incorporated loops](http://www.contextfreeart.org/mediawiki/index.php/Control_flow_elements) in a recent update.  By becoming more general purpose-y, DSLs lose some of their domain specificity, which according to Fowler is what makes them worthwhile in the first place [Fowler, 2010, p 28].


---
 
**Question**


In what way is an API a language? 

**Response**

APIs are actually a lot like DSLs, especially internal ones. In fact, they actually match Fowler's definition of a DSL quite well [Fowler, p 27-28]. They are used by people to give instructions to computers. Good APIs should also have the fluency and feel of a programming languages. This is backed up by Joshua Bloch, who wrote "strive for intelligibility, consistency, and symmetry [in APIs]. Every API is a little language, and people must learn to read and write it. If you get an API right, code will read like prose" [Bloch, 2006, p 1]. APIs generally have limited expressiveness. Even if they are pretty flexible, APIs usually to carry out their operations through another piece of software or on another computer, which is kind of a limited domain in and of itself. I think it would follow that APIs will also have the domain focus that Fowler mentions as his last characteristic of a DSL. The whole purpose of using an API is because it's better at what you're trying to than the GPPL that it's implemented in.

APIs also fit some of the descriptions of DSLs that we talked about in class. While some APIs may be Turing complete, they generally focus on making only specific tasks easy. This is because they are both designed (and generally used) for doing these particular tasks. Since APIs are commonly implemented as libraries, this also means they have a host language (which is the language they are a library for).

I think it's also pretty intuitive that APIs are a (programming) language. They have their own vocabulary, which is made up of the names of their public methods, and they have their own syntax, which may be limited and/or determined by the host language. Good APIs will also have their own grammar and/or style that makes the methods coherent and work well with each other. As Joshua Bloch wrote, a good API should "use consistent parameter ordering across methods" and "should rarely require documentation to read code written to [it]. In fact, it should rarely require documentation to _write_ it" [Bloch, 2006, p 1].

---

**Question**

What does the post on grayscale tell us about the process of API design?

**Response**

First and foremost, the post and its comments show us that it’s extremely important to ask for feedback during the design process.  Almost every comment provided valuable feedback, either pointing out pros and cons of the suggested names or suggesting new names entirely.  The commenters were generally in agreement that they wanted the name that felt most intuitive (7 separate commenters even used the word “intuitive” in their posts).  However, they could not seem to agree on what that name was.  Out of the 756 respondents of the [poll]( https://docs.google.com/forms/d/1pp3RY-A4MAs7b-gmqFx6bKn52_G_WLoPFkV0vueiWP4/viewanalytics?usp=form_confirm), at least 9% voted for each of the five options, meaning that for every possible name, a sizable portion of users found it to be the most intuitive.  More importantly, the most popular choice, “rgb(x) and rgba(x, a),” received only ~47% of the vote, meaning that at least half of the users would not be fully satisfied no matter what name the developers choose.  A takeaway from this, I think, is that when designing an API you may come across situations where it’s impossible to please everyone.  When each possible name has a legitimate list of pros and cons, there won’t be one right solution.  Accepting this fact and not pandering to vocal minorities is important.


One commenter put forth the print/photography terms “luma, lightness, value, brightness, intensity, or key” as possible names, and implied that users with backgrounds in print or photography might appreciate the constancy.  This brings up an interesting point, which is that the intuitiveness of a name will vary greatly depending on the user’s background.  This would help to explain the mixed poll results, and reinforces the fact that, as a developer of an API, it is important to always keep in mind the backgrounds of your users.


The mixed responses bring to mind the advice of Joshua Bloch, who suggests that “if it’s hard to find good names, go back to the drawing board” [Bloch 2006].  One comment was in line with this advice and asked the developers, “Why the need for this function at all? Seems unnecessary.”


---

**Question**

The comments on the Pavlus article seem to set up a conflict between
professional programmers and everyone else. What is the essence of this
conflict? Do you sympathize more with the substance of the article's arguments
or with the substance of the majority of the commenters' arguments? Do you
sympathize more with the tenor of the article or the tenor of the majority of
the commenters?

**Response**

The problem that came up in the comments in Pavlus article is actually present in a variety of different situations. For instance, in academic paper writing, authors often have to choose between using disciplie-specific jargon (which allows them to quickly and succinctly convey their ideas to individuals in their field) or language that is accessible to a general audience (which will be much more verbose and will therefore take much longer to write). While it would be great if everyone could understand scientific papers, it's not very efficient for scientists to have to explain concepts that most of their peers already know if their papers will largely be read by their peers. While this can be taken to an extreme (where authors rely so heavily on using terms specific to their kind of work that they isolate themselves from all but a handful of colleagues in their field), this practice generally helps save a significant amount of time on what is often already a quite lengthy process. The key is to find a balance that allows for quick writing but that maintains readability for most of the target audience.

This is what I think should be the case for programming languages. Most PLs should not cater to the lowest denominator (and read like a self-contained book). It is already hard enough to navigate code and making it more verbost will not help that. However, creators of PLs should strive to encourage readability and clarity so that it is easy for programmers who are familiar with the language to understand each other's code. If code in a language easily becomes too dense or "WORN" (write once, read never), then its maintainability (and therefore efficiency) will be severely impacted.

I think [Strengthiness' comment](https://www.fastcodesign.com/1665735/why-arent-computer-programming-languages-designed-better#comment-93e75ca0-9b5b-11e4-a3e4-4930d33952b2) does a good job of summarizing my opinion on this issue: "...there's a reason why programming languages professional programmers use are precise and terse (-ish…). A language like Quorum may be good for learning programming concepts, but as an everyday tool for a professional programmer it would be so overly verbose as to just slow one down. Our languages may be esoteric and the tools hard to master, but show me any other technical profession where tools are straightforward to learn and mastery comes easily." I also agree with [Mjaksen](https://www.fastcodesign.com/1665735/why-arent-computer-programming-languages-designed-better#comment-f3521300-7b3d-11e2-9387-9794fc737ae8) that even if we tried to make programming languages more approachable, it would cause more complications, leading them to conclude "there \*really\* is no pleasing everyone" (which Joshua Bloch agrees with when it comes to APIs). [Simon](https://www.fastcodesign.com/1665735/why-arent-computer-programming-languages-designed-better#comment-95ed5400-5bc1-11e1-921b-9794fc737ae8) also makes an excellent point that reafirms what Strengthiness wrote above: "The issue with writing software is not being able to program; it's being able to program \*well\*. There are a number of languages out there which have been specifically designed to be easier to write for novice programmers. What generally ends up happening is that novices then end up writing software, and the quality of the end product suffers as a result. I'm not knocking novices -- we were all novices at one point -- but I guess most companies have got somewhere an Access database system or simple VB6 program that they rely on for some task but which is woefully inadequate, or worse, a security minefield, because it was written by someone who didn't really understand the technical issues." Perhaps the problem is not that programming languages are too hard, but that there currently isn't enough technical training on how to use them (and especially on how to use them well).

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

These experiences are not necessarily at odds with each other.  Based off the Quorum [documentation]( http://quorumlanguage.com/syntax.php) and the above quote about Applescript, a key difference between the two languages seems to be that, while both languages incorporate natural language, Applescript is loose in its syntax while Quorum is strict.  This is where Applescript goes wrong.  Cook states that it was the “syntactic variations and flexibility” that confused users, not the fact that the words themselves were taken from natural language.  The potential for confusion when loose syntax is allowed is summarized well in the following stackexchange [thread](http://programmers.stackexchange.com/questions/49623/should-programming-languages-be-strict-or-loose):
“Every place where there's some ambiguity, the compiler needs to have some way to guess what the programmer really meant. Every time this happens, there's the chance that the programmer really meant something different, but didn't have the ambiguity-resolution rule down.”


For this reason, I would definitely keep my syntax strict when designing a DSL.  I would, however, include natural language.  Every language I can think of incorporates natural language to some extent (“for” and “if” are words from natural language), and I can’t imagine why I’d make up gibberish words when English would work just fine.  I would favor terseness when choosing names and syntax for control structures (if my DSL includes them).  While a language like Quorum might be easier for complete beginners than languages like Java and Python, I think the long term productivity boost that terse syntax provides is worth a steeper learning curve.



---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**

After reading and taking notes on the articles separately, we met to discuss the questions and outline our responses.  Each of us then wrote up 4 responses each excluding this one (we both wrote a response for the second question).

---