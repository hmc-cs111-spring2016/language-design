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

Our first quote:

> In a race, a small language with warts will beat a well designed
> language because users will not wait for the right thing; they will use the language that
> is quick and cheap, and put up with the warts. [Steele 1998]

We thought this was an interesting idea - Steele’s argument against small languages was straightforward, but we were not as convinced by this. There are certainly situations where you’ll need this kind of speed in putting out a language, but for a DSL there is not necessarily a big market of competitors that you need to beat to the punch. If there are no competitors then we thought it might make more sense to be slower and get rid of some of the warts before releasing a language. We also thought the idea of warts was interesting, and agreed with the idea that incremental design starting with a ‘warty’ language is a good solution for a lot of languages. However, this depends on the severity of the warts because some problems are less easily fixable after the language is released.

Our second quote:

> Not all programming languages have a way to code definitions, but most do. (Those that do not >are for wimps.) [Steele 1998]

It struck us how Steele characterized languages without definitions as necessarily a bad thing, and with some discussion we realized how this is especially incorrect for DSLs. While we agreed that general-purpose languages will certainly need some way to give definitions, it may be more than the user needs for many DSLs. We thought about the DSLs we had seen and many do not have any capability for user-made definitions, for instance ABC notation (which Josh saw in a peer review). Any DSLs that function like APIs will also lack this capability because you do not need to define new commands or functions to interface properly with an API.

Our third quote:

> You can always add things later, but you can't take them away. [Bloch 2007 ~20 mins?]

To us, this spoke directly to the fact that user-centered design is at the top of the priority list for a programming language. If there were no users, we could do whatever we wanted to the languages we design. However, if we put out a language or an API and then take away a feature that users have become accustomed to, they will naturally complain. They would be right to complain about this because if there is some feature being offered, then they should be able to become accustomed to using that feature. The set of available features should only ever grow, not shrink.


---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

Probably the most important and overarching symptom of a good programming language was discussed in class, and captured very well in a quote from the reading:
> It should be easy to do simple things; possible to do complex things; and impossible, or at least difficult, to do wrong things. [Bloch 2006]

All three of these are very important. If it is not easy to do simple things in a language, then users will never be willing to put in unnecessary work to do what would be easy in another language. The things that are categorized as simple may vary from language to language (or domain to domain), but there will always be simple operations that users understand should be easy. If complex things are impossible, then no one will ever be able to write more than a simple program; this may be acceptable for some little languages but is in general a sign that more features are necessary. Finally, most importantly for DSLs, the language needs to give the user a good sense of what things they should not do. If this is not the case then the language is likely poorly defined.

These themes fit with other themes that we discussed as well. Good documentation is a good sign, while bad documentation may mean that the language was not completely conceived prior to being released. On a high level, if a language has little room for users to grow the language in a manner described by Steele, then it was likely not designed with users in mind, which can be a very major flaw. More low-level language design choices can also be clear symptoms of good or poor design: for instance, poor method names that oppose the user’s expectations are a very bad sign. 



---

**Question**

How do the themes of _Growing a Language_ relate to the lab we did this week?

**Response**

The process we did in lab related to both the content and form of Steele’s paper. Content-wise, we were undertaking the process of growing a small language. We were essentially users of this language who saw features that we wanted to add, because we were given so little direction over what to do. Because the files we were given had only very skeletal definitions, they were very easy to grow and change. The language was written in a fairly intuitive manner, enough so that we could easily understand it and expand upon the basic definitions we were given.

Form-wise, it struck us that Steele only ever defined what he really needed, sometimes going out of his way to avoid defining new terms and discussing why he was making these decisions. When we designed new features to add to the sound lab, we needed to be very careful not to bloat the design with tons of unnecessary features. It would be very bad if, for instance, we defined functions for “increase-volume-and-reverse” and “increase-volume-and-swap-halves” and so on for every possible combination of things we could do to the music. Rather, like Steele did, we can avoid bloat by defining general patterns that allow us to design even more features on top of them.

Another interesting similarity is that Steele defined words in two ways: either by directly defining words, or by defining ways in which words can build into other words (such as adding -ing to verbs). Within the lab, we could do something similar with our design: we could add more building blocks (things similar to changing the volume or reversing), or we could add new ways to combine those building blocks. By doing both of these in conjunction, we can make our language as easy as possible for users to grow.



---
 
**Question**

In what way is an API a language? 

**Response**

Like a language, an API is at its core a vocabulary of words you can pass into the API, and meanings for each of those words. In both cases, what’s important is how these words are interpreted in the context of the language and how the user understands the corresponding documentation. An API is essentially a “little language.” Writing a call to an API feels like writing a call to a method in any standard language. This is much like one of the criteria we discussed for DSLs: they have to have a language feel to them [Fowler 2010]. The fact that APIs have a language feel to them is good evidence in favor of their being considered as languages on the same level as DSLs.

Just like any language, an API is growable in the way that Steele discussed, namely in his example of one syllable words and additional definitions. Like our third quote in the first question mentions, you can always add additional functionality to an API as more of a need for it becomes apparent. In fact, it may even be easier with an API because there are fewer interactions between user and language to consider. 

Another big similarity is that language design and API design are very similar processes. Like Bloch says, there are many many standard practices in the world of API design that are similar to good practices for language design. Both of them need to be very focused on what the user really needs, rather than what the language designer thinks that the user needs. Both should be as simple and elegant as possible while still having all of the functionality that they need. Likewise, languages and APIs must be properly documented in a way that makes sense to the user. If the user cannot understand the documentation, they are less likely to use the language or realize all its capabilities. 



---

**Question**

What does the post on grayscale tell us about the process of API design?

**Response**

The post on grayscale tells us that API design is an iterative process. Throughout the design of a language, there could be multiple ways of accomplishing a task. In the Verou article, several ways of representing grayscale are mentioned and users are asked to vote on which they find to be most intuitive. Users are also asked to leave comments justifying their opinions. The article is a good example that API design is a collaborative process, a dialogue between user and developer. 

The commenters provide an insightful discussion that reflects their varied perspectives on the issue. Some argue in favor of the various methods proposed by Verou while others suggest entirely new forms of grayscale representation. This is where the domain of the language becomes important. Commenter x_addict suggests the following, 

> how about luma, lightness, value, brightness, intensity or key? All taken from the print or photography worlds.” [Verou, 2014] 

This form might be the most intuitive representation of grayscale if the language were to be used in print or photography software. However, in a different context, users may struggle to understand the format. In order to make the most successful decisions for a language, developers should take user feedback into account while simultaneously keeping in mind what they want their language to be.

After some discussion, we agreed that the most intuitive way to represent grayscale (in our opinion) was an option proposed by a user in the comments. Commenter David Moore suggests, 

> Why not grayscale(lightness [, alpha])? [Verou, 2014] 

This option was not suggested by Verou and demonstrates the impact that users should have on the process of a well-designed API. Had the developer made a decision without first consulting users, they would not have opened themselves to potentially more intuitive possibilities. 

---

**Question**

The comments on the Pavlus article seem to set up a conflict between
professional programmers and everyone else. What is the essence of this
conflict? Do you sympathize more with the substance of the article's arguments
or with the substance of the majority of the commenters' arguments? Do you
sympathize more with the tenor of the article or the tenor of the majority of
the commenters?

**Response**

The comments on the Pavlus article generally seem to suggest that the article does not take many factors into consideration when claiming that programming languages should be more semantically intuitive. Pavlus insists that existing languages are very difficult to understand and have sacrificed usability for succinctness. He cites Perl for its confusing syntax and uses it as an example of how inaccessible programming languages are to the average person. 

In order to address the conflict in the comments, we must look at the distinction between professional programmers and everyone else. Pavlus’ article says,

> Unless you’ve had specialized training, looking at lines of code is like reading hieroglyphs, only less intuitive. [Pavlus, 2012]

This defines professional programmers as those who have had specialized training and are thus able to understand code. Keeping this definition in mind, the majority of comments seemed to sympathize with professional programmers. While Pavlus mentions the need for a more intuitive programming language, the commenters cite the convenience of efficient syntax in writing professional programs. One commenter, Mjaksen, writes the following:

> True but irrelevant. C/C++ *IS* a terrible language to express oneself in, but it's pretty good at 
> organizing large software projects and interfacing with all the link libraries and shared libraries 
> that it needs to get the job done… I have *never* seen a language that is concise, contextually 
> clear, and easy to read, that can also organize code/objects/threads/errors and place nice with 
> the os/shared libs. [Pavlus, 2012]

The point made here is that it is difficult to have the best of both worlds. Programming languages are designed with efficiency in mind and make sacrifices in terms of readability.

We agreed with the majority of the commenters in the article that there is a reason why current programming languages are not easy to read. Professional programmers are trained to work in these languages to maximise their output and the effectiveness of their programs. It is also important to consider the needs of those who are not professional programmers. They may have no formal training in programming languages. Pavlus advocates for this group of people but ignores the fact that computer science is far more than syntax knowledge. Computer science involves knowing how to design programs intelligently, regardless of specific language inconsistencies. Even if an efficient and semantically accessible programming language were to exist, it would still require specialized training to be able to write complex programs. 


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

From the selected quotes, the two experiences of natural language seem to be at odds with one another. The Pavlus quote claims that users preferred working with something akin to a natural language, whereas the Cook quote says that programmers found natural language to be too ambiguous. These two experiences cannot be directly compared without examining the backgrounds of the people being quoted as well as the amount of exposure that they had to the language. 

The Pavlus article suggests that the users in the usability testing were novice programmers. They preferred the natural language replacements and did not mention the depth or duration of time that these users spent working with the language. The Cook quote labels users as programmers, but it does not specify the programming abilities of the users. In short, the two experiences could be from the perspectives of different audiences. If novice programmers had little exposure to language, they might be able to relate to natural language more easily. In contrast, users of AppleScript could have more programming experience and thus more confusion over the inconsistencies of natural language syntax. Alternatively, users of AppleScript may have been developing more complex programs and run into more cases of ambiguity. 

Regardless, these are only two examples of natural language in a DSL. The decision to include natural language in a DSL depends on the domain and the targeted user of the language. It is generally safer to avoid the ambiguous behavior that can result from the translation of natural language into programming syntax, especially when unpredictable users are involved. There are cases where the targeted user would benefit by interacting with the system through a natural language interface, especially if that language is simple enough to minimize confusion.

We both agreed that a great example of natural language implementation in a DSL is [Scratch](https://scratch.mit.edu/). This DSL is used to create animations and games and introduces users to basic programming logic through blocks of natural language. These blocks can be combined in specific configurations to create animations. The language minimizes error by limiting the ways in which the blocks can be combined. Scratch is often used as an introduction to computer programming because it largely consists of natural language describing basic concepts of program logic. By preventing excessive error, Scratch does not introduce as much ambiguity as AppleScript but solves the problem presented in the Pavlus article that:

> novices learning to program at the university or younger levels can have signiﬁcant difﬁculty 
> learning the syntax of general purpose programming languages, which may initially seem 
> arbitrary. [Pavlus, 2012]

---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**

Both parts of the team read each piece on their own. We then met up to share our thoughts. We took notes on all parts of the work while in the same place and each of us was in charge of half of the end piece (Josh wrote the first half and Em ma wrote the last half). The team met once more to fix their work and turn it in.

---
