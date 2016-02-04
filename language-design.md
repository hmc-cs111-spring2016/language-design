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

***Quote 1***
>"I now think that I, as a language designer who helps out with the design of the Java programming language, need to ask not 'Should the Java programming language grow?’ but ‘How should the Java programming language grow?'" [Steele, 1998, 7]

When boiled down to its very essence, this quote encapsulates the overall philosophy of this paper as well as Steele’s advice to all language designers. Specifically, this quote talks of the importance of language growth and evolution. A programming language does not exist to be a rigid set of unchanging rules. Rather, it exists as a tool for enabling powerful communication between humans and machines. Therefore, if there is a way to better achieve this communication, the language needs to adapt to the needs of its users and enable maximal ease and expressiveness. For these reasons, language evolution is not optional, but a necessity that motivates Steele’s claim that the “…main goal in designing a language should be to plan for growth” [Steele, 1998, 7]. Although Steele goes on to explain ideal methodologies for growing a language, citing the Linux development model as an exemplary case, the principal goal comes back to prioritizing the needs of the users. It is for this reason that Steele advocates creating languages as a more accessible platform that enables extensibility and natural evolution through things like libraries and extendable syntax.

***Quote 2***
>"We should not make the Java programming language a cathedral, but a plain bazaar might be too loose. What we need is more like a shopping mall, where there are not quite as many choices..." [Steele, 1998, 12]

One of the challenges of language design is properly allowing room for users to extend and change the language. In this quote, Steele references and extends a metaphor that identifies the middle ground between no opportunity for user extension and too much wiggle room to provide cohesion in a language. While he talked about this idea at greater length that what we quoted, we felt that this summed up the key points. Essentially, a cathedral represents a language whose extension is inextensible by its user base. It is far too sturdy a structure and is too imposing to allow for creativity and change. Conversely, the bazaar represents the confusion of too little structure. While it has all the mobility and room for change one might desire, it does so at the cost of unity and clarity. As such, a shopping mall may be the happy middle ground. It has distinct structure as a building but allows for interchangeable parts and development.

***Quote 3***
>"That’s not Greek, it’s Klingon." [Pavlus, 2012]

This quote, while intended as a witty tongue-in-cheek comment, also manages to encapsulate the main takeaway of Pavlus’s article in one fell swoop. Specifically this comment is poking fun at the inaccessibility of popular programming language syntax, such as Java and Perl, to non-tech-savvy individuals. While Greek may be inaccessible to the average English speaker, that doesn’t mean it is inaccessible to humans as a whole. Rather, there are many Greek speakers across the globe ranging from child to scholar. More specifically, as a spoken language, Greek can be easily used by people of any walk of life to communicate. Klingon, on the other hand, is an impractical alien language that, by lore, is not intended for general humans. Rather, while humans can learn Klingon, it is a language not intended for humans as a whole and only learned by a small dedicated geek subculture, the Star Trek fan base. This parallels the truth of programming languages to the dot. The choices made in programming language syntax design, while logical to the geek subculture of programmers, is inaccessible to general public. Most importantly this quote embodies an important consideration that is mostly overlooked by expert language designers: usability. Many programs, such as the simple 10-iteration loop for the article does not require extensive technical knowledge to understand conceptually and yet the syntax does not reflect this. As the field of programming languages moves forward in the future, Pavlus and the interviewed expert Stefik think that this is something that needs to be addressed.

---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

Several features that identify a well-designed language are the following: easy to extend, comprehensible, usability, good documentation, non-bitter user base. Essentially, a well designed language won’t leave its users frustrated for hours on end as they struggle to program the basic ideas they have. In other words, since a programming language is a way of expression, a good language should be intuitive and self consistent. It will have documentation to support its design and the syntax will be readable (enough). Furthermore, as Steele highlights often in _Growing a Language_, it will have the ability to be extended and thus adapted by its user base. This evolution allows users to grow the language in a direction that best suits the needs of the masses. An example of this, as explored by Mernik, shows how the COM interface allows Excel’s limited macro language to interface with languages such as C++, Java, and Basic through a “process of componentization… called automation [Chappell 1996]” [Mernik et al., 2005, 318]. By allowing a language, while staying specific to its domain, be more accessible to other interfaces, its use cases grow. This engenders a positive user base that speaks well of the language, rather than the stink eye from the computer science community.

Conversely, a poorly designed language will feature the opposite of basically everything described above. Its documentation will be unclear, its syntax unintuitive, its design unextendable, and its user base very aggravated. Furthermore, it may lack implementation for different tasks a user may need. That being said, the symptoms of a of a poorly designed language can also be less obvious. For instance, as discussed by Steele, APL, a language the author himself admittedly loves, died primarily because “there was no way for a user to grow the language in a smooth way” [Steele, 1998, 6]. Thus, a poorly designed language can suffer from a range of shortcoming, but it takes only one major Achilles Heel to kill an otherwise good language.

---

**Question**

How do the themes of _Growing a Language_ relate to the lab we did this week?

**Response**

In Growing a Language, Steele emphasizes the importance of extensibility in language design. In our lab, we explored actually implementing some of that extensibility. One idea presented in Growing a Language was definitely evident in our lab--the slowness of trying to grow a language all by oneself [Steele 1998, 6]. Almost everyone in the room did not feel they were able to make much progress, in part because of the difficulty of working by oneself. However, if we were to combine the progress of everyone in the room, we would have quickly expanded the music library by a quite greater magnitude.

Also, the “bazaar-vs-cathedral” idea mentioned in our response to the quote question is also relevant here. Given that the music library was much more a library than a language, it definitely had the open feel of a bazaar, without much structure to guide how it _should_ work. It felt like we had the task of creating the shopping mall structure ourselves, rather than working within an existing shopping mall.

Essentially, the music library was missing that which Steele considers key: “a pattern for growth” [Steele 1998, 12]. It did not have a basic structure for development and extension. However, because it was bare bones enough, that means that we as developers could add that pattern in as we extend and modify it. We think that’s what many of us intuitively tried to add to the language as we extended it--patterns, systems, etc. 

---
 
**Question**


In what way is an API a language? 

**Response**

According to Wikipedia, by definition an API, or application programming interface, is “a set of routines, protocols, and tools for building software and applications” [[Wikipedia]]( https://en.wikipedia.org/wiki/Application_programming_interface). When considering this definition along the comments of Joshua Bloch, it becomes clear there isn’t a big distinction between a good API and an internal DSL. In fact, these terms are even more blurred when Bloch describes an API as, “a little language, and people must learn to read and write it” [Bloch, 2006, 506]. Just as an internal DSL is a language embedded within a host language, APIs are exposed “intermodular boundaries” [Bloch, 2006, 506] written in another language for module communication. Therefore, an API, like an internal DSL, is written in a language and contains an abstracted subset of the “host language” to be used alongside other “host language” code (I quoted “host language” since this is a term usually used for the language an internal DSL is implemented in, not the language an API was written in).

Furthermore, unlike a general purpose programming language, an API has a very small focus. Convoluting an API with general functionality is almost always a detriment. It is for this reason, Joshua’s advice often follows the KISS paradigm (Keep It Simple Stupid). While Joshua’s advice of “Keep APIs free of implementation details,” “When in doubt, leave it out,” and “Minimize accessibility; when in doubt, make it private” [Bloch, 2006, 506], is all given in the context of good API design, we can also validly apply these recommendations to a focused DSL. For instance, all of these points can also be made in reference to the design philosophy of ContextFree. Specifically, although ContextFree is a powerful tool for designing digital art, it is limited to just this task. That is, ContextFree intentionally does not enable users to access low level features and implementation details or complete non-digital art tasks.

Finally, the purposes for creating an API or DSL shares many overlaps. Most notably although a DSL cannot enable a user to do something the host or implementation language cannot do, it can make it a lot easier for users. For instance, anything a user can do with a Bash Script can be done in raw C. That being said, for the specific domain of file and process manipulation, a Bash Script will often enable these tasks to be completed much easier and faster. Similarly, since an API enables code reusability and abstraction, an API can enable a developer to have a faster and easier development process since they do not have to fully re-implement the API’s content. Because of this, however, APIs need to be well designed so they actually simply the development process. In the advice of Bloch, “APIs should be self-documenting” and “Strive for intelligibility, consistency, and symmetry” [Bloch, 2006, 506]. It is for these reasons, like a good DSL, an API should be mostly intuitive making the targeted domain task simpler.


---

**Question**

What does the post on grayscale tell us about the process of API design?

**Response**

Lea Verou’s forum post on grayscale is the embodiment of several important design paradigms explored in Bloch’s API design paper. To elaborate, this forum post was created by Lea Verou to ask users to vote on the best name for an API function she was designing. Specifically, the function name was supposed to describe a routine that sets a color to an appropriate shade of gray when provided a lightness and optional alpha parameter.
 
By asking her users to vote on a function name, Verou is clearly in compliance with Bloch’s suggestion that “Names matter,” and “API design is not a solitary activity” [Bloch, 2006, 506]. For instance, if the function names or her users did not matter, why would the developer ever go through the trouble of poling users for something so trivial? It is because, like a DSL, a good API strives to be a simplification of functionality that is intuitive for users. Therefore, a good API should not be what is easiest for the designer to implement and remember, but should conform to the needs of the user base.

Furthermore, assuming Verou will name her function in correspondence to the popular vote, by quantifying the user’s opinions, Verou is also complying with Bloch’s advice that, “You can’t please everyone so aim to displease everyone equally” [Bloch, 2006, 506]. While this advice is a little bit of a joke, the essential take away is that _any_ decision made by a developer will likely benefit one user while inconveniencing another – therefore, since every decision has both good and bad consequences, a developer should strive to benefit the most users while catering to no individual in specific. For instance, none of the proposed function names in this post are illogical. In fact, they’re all _good_ since they make sense in their respective contexts and follow Bloch’s advice of “…the principle of least astonishment,” where every “…method should do the least surprising thing it could, given its name” [Bloch, 2006, 506]. Verou even shows concern for overloading the rgb() and rgba() functions for this purpose similar to Bloch’s advice of  “Overload with care.” [Bloch, 2006, 507]. Therefore, by voting Verou is essentially attempting to displease the fewest number of users, or in other words, “displease everyone equally” [Bloch, 2006, 506].

Ultimately this all boils down to the fact that there are no _objectively right_ name for these functions beyond catering to the users. This lack of altruism, however, is in direct contrast to most other aspects of computer science where a well-defined metric will usually make the decision for the developer. Since API design caters directly to humans and what _feels_ right to them, Bloch’s statement “API design is an art, not a science. Strive for beauty, and trust your gut,” [Bloch, 2006, 507] suddenly makes a lot of sense. This forum post is essentially an art exhibition where Verou is gathering feedback on her craft to better her future work.

---

**Question**

The comments on the Pavlus article seem to set up a conflict between
professional programmers and everyone else. What is the essence of this
conflict? Do you sympathize more with the substance of the article's arguments
or with the substance of the majority of the commenters' arguments? Do you
sympathize more with the tenor of the article or the tenor of the majority of
the commenters?

**Response**

The comments took on a variety of tones. Some programmers want to consider themselves as [special snowflakes](http://i.imgur.com/AfnKFeA.jpg) with superior intellects. For example, one guest user claims that the reason some people can’t understand the syntax is because, “Most likely because their brains do not process information like a real programmer does.” [Anonymous Guest](https://www.fastcodesign.com/1665735/why-arent-computer-programming-languages-designed-better#comment-2dfe2900-7795-11e2-9384-9794fc737ae8). However, other people had more reasonable approaches.

One point several commenters brought up is that any field that involves careful precision will involve difficult-to-use tools. One user, named Strengthness, compared it surgery, referencing how a surgeon would need lots of training to understand a complex system not easily graspable by the outside layman [Strengthness](https://www.fastcodesign.com/1665735/why-arent-computer-programming-languages-designed-better#comment-93e75ca0-9b5b-11e4-a3e4-4930d33952b2). This is a valid comparison, in that we do expect highly technical fields to require tools that may seem illogical to the non-technical user. However, what many commenters failed to address was that the quasi-illegible syntax creates a higher barrier to entry for aspiring programmers. Programming should be more accessible, not elitist. 

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

Intuitiveness is the underlying feature of good design, whether talking about a DSL, API, or any other product that will be used by the general masses. A quality intuitive product will work with minimal instructions and will enable non-experts to relate without a challenging barrier of entry. Therefore, it is important to note that the assumption of interfacing with natural language is inherently _good_ is _false_. Specifically, while it is true natural language is relatable to everyone, not just programmers, it is also important to remember a programming language cannot be ambiguous. The challenge highlighted in these seemingly contrary claims, however, is when does natural language stop being beneficial for a programming language’s intuitiveness. While all users can mostly relate to natural language, computers, unfortunately cannot. A program, in its most basic form, is a series of formal specifications that define a computer’s behavior. Unlike human language, a good programming language _cannot_ enable ambiguities and _should_ be consistent. Since a programming language needs to be formal and precise, by relying too heavily on natural language, a designer can accidentally trick users into thinking a language is more similar to natural language than it really is, thus hurting intuition. This seems to be the issue eluded to in Cook’s comment that the “main problem is that AppleScript only appears to be a natural language” [Cook, 2007, 1-20]. By making AppleScript be too much like natural language, the users end up hindered by erroneously equating the distinct idiosyncrasies of natural language and AppleScript. Thus, while relying on natural language to inform intuition, relying too heavily on it may ultimately induce more confusion than it relieves.

Therefore, if given the option to incorporate natural language into a DSL, I would likely include some, but do so moderately. Like all things, too much of a good thing can quickly become bad. To avoid creating a language that is “easy to read… but quite hard to write…” [Cook 2007, page 1-20] like AppleScript, I would want to avoid relying too heavily on natural language. Therefore, by using a nice compromise, like Python’s _in_ operator (in contrast to the contains() function of other languages), a programming language can simultaneously improve readability and build a user’s intuition while also keeping the boundary between natural languages and programming languages discrete.

---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**

We first met to discuss our overall response to the papers and to choose the quotes we wanted to focus on for the first question. Then, we divided the questions evenly between the two of us and wrote response independently. We reconvened to make edits to each other’s work and continued to revise and expand our answers on google docs. Finally, Andrew formatted the markdown so that Hannah could push the work. 

---
