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

1. "Does this mean, then, that it is of no use to design? Not at all. But in stead of
designing a thing, you need to design a way of doing. And this way of doing must make
some choices now but leave other choices to a later time." [Steele, 1998]

I liked this quote for a couple reasons. First, it seemed like an encapsulation of a lot of what Steele was trying to say in his talk; in designing a language, one shouldn't think necessarily about exactly what the users of the language need. Rather, according to Steele, one should think about how to allow the users to make the things they need and expand the language themselves. I think this is an interesting and important point, and the quote chosen describes that really well. I also liked the quote because it seems relevant to more than just programming language design. I think it applies to life in a way, and the notion that oftentimes, the process and learning gleaned from doing a task is as important (or more so) than the task itself.

2. Steele describes introducing Java as it is to a new programmer audience, saying: "Programmers would have cried, “Too big! Too much hair! I can’t deal with all that!” But in real life it has worked out fine because the users have grown with the language and learned it piece by piece, and they buy in to it because they have had some say in how to change the language" [Steele, 1998, p. 14]. In practice, we found that the second part of this claim is certainly true. Historically, to learn Java as it was developed was to learn it through experience, piece by piece. Like Steele mentioned, learning this way is natural, and models the way we actually program. At the same time though, now that Java has been fully developed and flushed out, people do need to learn it in its current size. This leads to the interesting conclusion that learning a new language that is already "large" by Steele's definition must be done by learning it piece by piece, as if it was in the process of being developed. Shoving an entire language on someone at once would be an overwhelming way to learn it. 

3. "If we add hundreds of new things to the Java programming language, we will have
a huge language, but it will take a long time to get there. But if we add just a few
things—generic types, overloaded operators, and user defined types of light weight, for
use as numbers and small vectors and such—that are designed to let users make and add
things for their own use, I think we can go a long way, and much faster. We need to put
tools for language growth in the hands of the users."

This quote is similar to the first quote, in that it encapsulates a lot of the main ideas that Steele raises in his talk. I like that he mentions specific tools that can be put "in the hands of the users" like lightweight user defined types, which are concrete examples of the idea of letting the language grow on its own. As he discusses in his APL example, even a very smart individual can't possibly grow a language as well as many people all creating the libraries and functionalities that they need and sharing them. I think this quote does a good job of summarizing this idea.


---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

Several factors influence whether or not a language is well-designed. Steele would say that the most important thing is for a language to grow. He says, 
"If one person does all the work, then growth will be slow. But if one lets the users help do the work, growth can be quick. If many persons work side by side, and the best work is added with care and good taste, a great deal can be added in a short time" [Steele, 1998]. He then gives the example of APL, a language which was well-written and powerful, but very difficult to expand upon; as such, smaller but more easily expandable languages such as Lisp were able to surpass it in time. Thus, Steele would say that the expandability of a language is a main component of good design. I tend to agree with this notion.
Steele would also way that a well-designed language defines only what is necessary. He says this in his discussion of the Java programming language. He discusses intervals, sets of games, and complex numbers as things he would love to see Java take care of for him, but eventually says he'd rather they not be in the language; he'd prefer the option to add them in as libraries, if needed. And, by extension, those libraries would definitely exist if enough people wanted that capability. The language doesn't have to implement it itself. He says, "When a language gives you the right tools, such classes can be coded by a few and then put up as libraries for other users to use, or not, as they choose; but they don’t have to be built in as part of the base language" [Steele, 1998]. With this in mind, a well-designed language gives programmers the space to add functionality, rather than have it have to be there.
I think Pavlus would argue that a well designed language is intuitive to learn and read. The experiment on which he reports shows that Perl is more difficult to learn than a randomly designed programming language; implicit in the research is that this makes Perl an inferior language in some way. As Josh discusses in his response to the Pavlus comments, difficulty to learn may increase barriers to entry for a programming language, but doesn't make it worse necessarily or poorly designed. It may be the case that the learning curve is steep, but then that having mastery gives you huge amounts of power in your programming.

---

**Question**

How do the themes of _Growing a Language_ relate to the lab we did this week?

**Response**

I think the methodology of adding functionality is probably the biggest similarity between the two. Steele introduces words only as needed, and some of the words he introduces (like "woman") are only introduced in order to introduce other words or ideas. He starts with an existing framework -- what he calls Basic English, and only expands on it based on the use cases that he needs. I think this is quite similar to what we did in the lab. We looked at the existing framework that we had, which is the sample solution to the CS5 sounds lab, and introduced features as we needed them. First we added a playSound function and a global variable storing the sound, which gave us the ability to delay the playing of the sound until all the transformations had been done. We only introduced features and functionality as needed, and didn't add things that would have been nice to have but weren't crucial (similar to the "-ly" which Steele decided not to include in the end).
The other thing that I found similar to Steele's talk was the idea that a poorly implemented but intuitive language is better than a well-implemented but difficult to expand language. Steele talks about this with his discussion of APL, which was created by "a very smart man" [Steele, 1998], but didn't have staying power because adding to the language was extremely difficult. He compares this with Lisp and Java, which gave the power to the programmers and as such has been able to stay around until this day. I think this is similar to the lab in that we tried to make thing easy to understand and expand upon rather than making things perfect. For example, we made a saveSound function which allowed users to save sounds and name their files. While we could have been much more expansive in this process, or perhaps made the syntax for saving sounds require less keystrokes, we intended to make it as intuitive as possible for the user to simply save and name a sound.
---
 
**Question**


In what way is an API a language? 

**Response**

Based on the principles of good APIs from the Bloch paper, as well as the elements of a language that Steele defines, its clear that APIs can at least be thought of as languages. First, Steele mentions that languages have their own sets of vocabulary and grammar rules for putting the vocabulary together. This is exactly what APIs are, new definitions of things that the user can do. These definitions are exactly the vocabulary that Steele talks about. Further, since APIs exist on top of existing languages, they already contain the language rules of the base language in most cases. Some complicated APIs define additional ways to use vocabulary elements, but they still have the existing framework. Bloch's article enforces this notion, saying that APIs need to maintain things that are generally considered coding practices of languages, like maximizing mutability, subclassing only when necessary, and reducing coupling [Bloch, 2006]. So, its pretty clear that APIs can be thought of as languages in the literal sense - they have vocabulary and grammar, and work like languages should. Additionally, according to Bloch, APIs should "feel" like languages as well. Bloch mentions the importance of names for API methods over and over [Bloch, 2006]. He does this to stress that APIs should feel intuitive to use and read. Methods should do what you would expect based on the names, and so reading and writing in APIs should feel logical, like reading and writing in a familiar language. Many APIs that we've used feel like writing in prose because the method names flow together naturally. At the same time, bad APIs don't feel like languages for this reason, even if they have vocabularies and language rules.

---

**Question**

What does the post on grayscale tell us about the process of API design?

**Response**

This post is fairly minimal, but it does provide some insight into what an API needs, and more importantly, doesn't need, to succeed. Neither of us was too familiar with using various notations for rgb, but it was clear enough what the different notations were trying to do. Overall, the general theme seemed to be best described by the quotes "The idea is that people are familiar thinking that way from grayscale printing", and "The benefit is that authors are already accustomed to using rgb() for colors, and this would just be a shortcut." [Verou, 2014]. In both cases where these quotes were used, the author was trying to justify the use of the notation by relating it to things that people already know how to do. In the first case, it was people with domain-specific knowledge about printing, and in the second it was building off of already used notation. The important thing here to us was that these proposals weren't trying to create something new and exciting, just to make something that is commonly done easier. This is exactly what an API should be. Both Steele and Bloch mentioned that languages and APIs respectively don't need to be large and all-encompassing, but rather focused on the tasks that actually need to be done. Bloch specifically says that "When designing an API, first gather requirements - with a healthy degree of skepticism" [Bloch, 2006]. The first thing that needs to be done is identify the use case, which in this example is improving greyscale notation. However, this is not sufficient. He adds that skepticism is necessary, because without it one might settle on the first solution to the use case that they could come up with. This example shows this by providing not one, but several different solutions to the use case, and trying to determine which is best. In this way, the goal of the API is met, not just by creating a new method in a language, but by creating a method that solves a common problem in the right way. 

---

**Question**

The comments on the Pavlus article seem to set up a conflict between
professional programmers and everyone else. What is the essence of this
conflict? Do you sympathize more with the substance of the article's arguments
or with the substance of the majority of the commenters' arguments? Do you
sympathize more with the tenor of the article or the tenor of the majority of
the commenters?

**Response**

Based on the Pavlus article itself, one would think that the main conflict is between the old, experienced programmers who have learned Perl (or whatever language) the hard way, and are now wizards, able to do whatever they want in a short amount of time, and new programmers looking to learn a language. However, looking at the comments reveals what seems to be a much more nuanced conflict. There seem to be three main groups of people in this debate. First, there are certainly some people who agree with the article, saying that programming languages are overly complicated and too hard for new programmers to learn. One rather verbose response concludes with "I'm not saying lets get rid of frameworks and efficient code, I'm saying lets find ways of getting anyone we can into programming. I genuinely believe it will make a world a better place. We need a planet of thinkers, not deadweight lever pullers" [Pavlus, 2012]. This person is essentially claiming that the languages as they are are not written with this goal in mind, though they do acknowledge that some of the complications are necessary. We felt sympathy for this argument in the sense that we feel as if the barrier to programming entry should be as low as possible, and looking at Perl is a great way to not want to learn programming. 

On the other hand, there are also people who take the complete opposite approach, that languages *should* be as complex as they are. These people range from making arguments in favor of this, to simply making claims that we both found elitist. An example of the former is "I don't understand.  You wouldn't want random untrained joes to wire your house, why would you (or those Southern Illinois folks) think it's ok to let them *program*" [Pavlus, 2012]?. One person even said just "Who's the author... an Arts Major" [Pavlus, 2012]? Both of these people, though presenting their arguments in different ways, seem to be making the same point. Languages are hard because programming is hard. If its a professional occupation, then it should be hard to learn. To some extent, we also understand this point of view. We don't see a problem with c++ being hard, because the thing that it does are hard. However, this particular argument isn't quite right, as it ignores any chance that the languages are hard in the wrong ways.

With this, the third group of commenters seemed to have a more balanced point of view. One excellent example that we both liked was someone who used c/c++ as an example, mentioning that, of course, the language has drawbacks, its hard to manage large amounts of c code, but c++ has tons of convenient libraries that interface with each other on a low level. They go further to give examples of the tradeoff between syntactically logical code, using a conventional "for" loop, and logically readable code, using method calls inside an "each" loop. The two present different ways to think about what hte program is doing. We think this gets at the core of the issue. Some things are intuitive to learn, while some things are intuitive to actually use with experience. Thus, we sympathize with this group of commenters, which is to say we acknowledge that there is an issue with entry barriers to coding, but some of it is just due to the inherent difficulty of programming, as well as the fact that intuitive ways to code are not necessarily intuitive ways to learn. 

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

I think there is a lot of truth in what Cook is saying. The closer you get to natural language, the more of an expectation you have to use it _like_ natural language. I think this is problematic because it creates cognitive disonnance from programmers, as their experience in programming (which, at this point, is nothing like talking) is too similar to their experience in using natural language every day. For this reason, it seems to me that on eshould be extremely careful in how much natural language is included in the design of a language. Personally, I would want to avoid associations with phrases and really common words, things like "do thing x times" or something like that. Instead, I would want to use words like "loop" or "do while," which are not as common in our everyday and as thus can form their own identities as words within a programming context.
In designing a DSL, I would be very careful using natural language. I think I wouldn't go further than using a certain word that evokes a certain feeling or purpose, or can very simply be connected to the task that it completes in the concext of that language. I would be hesitant to create false expectations or cognitive dissonance among the users of my DSL. There is a testing language that works with Ruby called Cucumber, which uses a lot of natural language in the asserting and testing of features; For me, it was extremely frustrating to use Cucumber because it would error at the smallest of deviations from the syntax, despite feeling as though it should work fine if it isn't exactly in the correct syntax. I think this frustration stems from the fact that Cucumber made me feel like I was talking in English to my computer, when in truth, I was simply using syntax that felt like "syntax" I use every day.
All that said, I think that intuitive and/or verbose method names are good programming practice, because they help the programmer contextualize the intentions of specific programs or functions. However, the language itself shouldn't be projecting its expectations of natural language onto the programmer, when in truth it expects a particular syntax in order to work correctly. 

---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**

We read the articles separately, then met up to discuss the work to do. We then decided to split up questions more or less arbitrariliy by going through them and picking ones that seemed interesting. Once we had the questions that we wanted to answer, we went though and made outlines of our responses and went over them together to make sure we agreed on what we were saying. We finished the actual responses separately. 

---
