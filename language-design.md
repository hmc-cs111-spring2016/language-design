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

   In “Growing a Language” by Guy Steele, the author argues: “In a race, a small language with warts will beat a well designed language because users will not wait for the right thing; they will use the language that is quick and cheap, and put up with the warts. Once a small language fills a niche it is hard to take its place.” [Steele, 1998]. We found this interesting and compelling. When we dream about creating our own programming language, we want everything to be perfect. We are tempted to spend countless hours pouring over our code trying to make it perfect, scoffing at “bad programmers” who have create ugly, error-prone and unintuitive languages or programs. But when we consider this quote, it’s difficult to deny its truth. Creating a perfect programming language is impossible, and even making a very good language is in some ways doomed to failure. No one will wait for you to build the perfect system. Even if you succeed, by the time you do, people will have adopted a different language, become accustomed to its quirks, and found ways to work around them. They will not want to invest the time and energy in learning to use a “better” programming language if the language they already have works well enough for their purposes.
   However, while designing the perfect programming language may be an impossible task, there are some good design principles that any successful programming language should follow. Joshua Bloch, writing specifically about API design writes: “**Obey the principle of least astonishment.** Every method should do the least surprising thing it could, given its name. If a method doesn’t do what users think it will, bugs will result.” [Bloch, 2006]. Most programmers’ immediate reaction to this quote is a small laugh and a murmured “Ugh, yes”. A function called max() must return the maximum number out of some list of numbers, if it doesn’t, users will assume it does, use it that way, and then spend hours searching their code for the bug. If they find it, they will only be more frustrated that a fault in the language made them waste so much time. Programming languages may seem cryptic to novices, but they follow general rules and guidelines that should be true across all languages even if they vary in the exact way they implement things. Programmers will not put up with languages that break these rules in too many ways.
   John Pavlus argues: “The broad computer science academic community has not paid a tremendous amount of attention to programming language usability” [Pavlus, 2012]. We absolutely disagree. Programming languages are first and foremost, languages. To an outsider who does not know the language, it may look incomprehensible, in the same way that Spanish may look incomprehensible to someone who only knows English. However, it has meaning, it follows general rules. When programming languages are written, they are written to be used by programmers. Creators do think about usability. They attempt to follow rules like “**The principle of least astonishment**” but they make tradeoffs between usability and other goals. Usability is not the only thing to consider when writing a language, but that doesn’t mean that programmers do not care about it at all.

---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

   Steele provides great insight on the qualities of a well-designed language: “I should not design a small language, and I should not design a large one. I need to design a language that can grow. I need to plan ways in which it might grow -- but I need, too, to leave some choices so that other persons can make those choices at a later time” [Steele, 1998]. Steele stresses two major points which we felt were fundamental for a well-designed language: scalability and user involvement. A well-designed language should start small with a plan for growth. As its users become accustomed to it, their wants and needs may expand and the language must have a plan to grow to meet these needs. The language designers must find a balance between the Cathedral approach, in which the developer decides on all design choices, and the bazaar approach, in which the developer relies on user feedback for all design choices [Steele, 1998]. A well-designed language is not one that necessarily is perfect from conception, but rather one that provides a foundation for continual improvement. Steele makes a compelling argument for user involvement by invoking a well known fishing metaphor with a twist: while it is useful to teach a man to fish rather than give him a fish, it would be even better to provide him with the tools necessary to create fishing poles such that he can help others catch fish [Steele, 1998]. In the same sense, a well designed language should provide enough working vocabulary for users to seamlessly expand the language. For instance, when adding additional features to a language, the syntax for doing so should be similar enough such that the user does not need to more or less learn a new language. 
   A poorly designed language is, in simplest terms, all the things a well-designed language is not. Symptoms of a poorly designed language include lack of flexibility in design and lack of scalability. These symptoms tends to stem from focusing too much on either the Cathedral approach or the bazaar approach. Using the Cathedral approach to language design results in a lack of user contributions and design too large to implement. In fact, Steele says languages too grandiose in nature during the planning stages are doomed to inevitable failure, as some other smaller language will fill the niche [Steele, 1998]. In a similar sense, using the bazaar approach results in a lack of structure and lack of foresight. Although user contributions are great, it is ultimately up to the language designer to plan for growth.

---

**Question**

How do the themes of _Growing a Language_ relate to the lab we did this week?

**Response**

   In the lab this week, we were given very limited time in which to work. Some of us tried to plan everything before we modified the code and therefore had very little time to implement our ideas. Other people began modifying the code, without first developing a plan for the growth and modification and so the changes they made were not always well thought out. The lab forced each of us to wrestle with how to divide our time between planning and implementing--a question that language developers must continually wrestle with. “Languages have now reached that large size where they can not be designed all at once, much less built all at once” [Steele, 1998]. We must plan the broad pattern and then alternate between planning and implementing so that we do not get so caught up in one or the other that we lose sight of the big picture. The broad pattern give us a consistency across methods without requiring the detail of a full plan for how we will implement everything. As Steele wrote, “A pattern should give hints or clues as to when and where it is best put to use” [Steele 1998]. The code we were given had no pattern, the methods seemed to take arbitrary arguments, each one stood separately and there was no fluid way to put them together. Each of us intuitively realized that it was not good. We had different ideas about what the pattern should be, but everyone began modifying the code to make function calls and parameters follow a more consistent, intuitive pattern. In doing so, we were mainly growing the language by changing the rules rather than by changing the vocabulary, the two ways to grow a language that Steele discusses, [Steele, 1998]. We were not trying to develop whole new methods, but rather trying to modify the input and output for many of the existing methods and only then perhaps add to the vocabulary.

---
 
**Question**


In what way is an API a language? 

**Response**

   Languages are collections of vocabulary and rules [Steele 1998]. We use languages to describe specific domains: natural languages describe the world around us, programming languages describe the domain in which we want a computer to perform tasks. Mernik describes an Application Programming Interface (API) as “a domain specific vocabulary of class, method, and function names” [Mernik et al., 2005]. We agree. This falls under our categorization of language because the API gives us all the tools necessary to describe the domain of the application. Additionally, APIs share several qualities of what we understand to be a well-designed language. For example, Bloch describes several must-haves in a good API, which include consistent naming conventions, ease of use, and self-documentation. When describing API naming conventions, Bloch explicitly says, “Strive for intelligibility, consistency, and symmetry. Every API is a little language, and people must learn to read and write it” [Bloch, 2006]. As in any well-designed language, API naming conventions call for a strong working vocabulary such that the users need make only a minimal effort to use it. Bloch explains how, “it should rarely require documentation to read code written to a good API. In fact, it should rarely require documentation to write it” [Bloch, 2006]. The API, like any other good language should make sense and be intuitive to use for anyone with some experience in it.

---

**Question**

What does the post on grayscale tell us about the process of API design?

**Response**

   The post on grayscale demonstrates several things about API design that Bloch articulated as rules in his paper, “How to Design a Good API and Why It Matters.” Bloch states that “**API design is not a solitary activity**” [Bloch 2006]. The grayscale post is reaching out to the entire community requesting feedback on their API design, it is decidedly not a solitary design process. The question they ask the community is about how to name a particular function, because “**Names matter**” [Bloch, 2006]. The designers want to find the best name for their function based on the domain in which it will be used as part of their “domain analysis” to find the best “domain-specific terminology and semantics” [Mernik et al., 2005]. Any of the suggested names would work, but they want input on which is the best and why some people would favor one over another. The name is important, because they want it to be “**Self-documenting**” [Bloch, 2006]. They want people to be able to use it without having to look up what the function does, and try to make the functions misuse unlikely, by making its input and output easy to infer from its name. They do this to enable its use by “users with less domain and programming expertise, or even by end-users with some domain, but virtually no programming expertise” [Mernik et al., 2005].

---

**Question**

The comments on the Pavlus article seem to set up a conflict between
professional programmers and everyone else. What is the essence of this
conflict? Do you sympathize more with the substance of the article's arguments
or with the substance of the majority of the commenters' arguments? Do you
sympathize more with the tenor of the article or the tenor of the majority of
the commenters?

**Response**

   The essence of the conflict is between non-programmers who recognizing the difficulty of most programming languages and professional programmers who arguing that if the code is difficult it is for a good reason. While there is truth behind the professional programmer argument, most of the comments demonstrated some degree of hindsight bias. Several of the professional programmers claimed syntax was not hard to pick up, or it was minor in the grand scheme of programming; however, much like how very few native English speakers recognize the difficulty in learning our language because we use it everyday, programmers can just as easily forget how difficult some programming languages can be to learn because they use it everyday. 
   We sympathize more with the tenor of the article, in that the learning curve for programming can be extremely frustrating because the syntax and features of the language can be so obtuse and abstract. Additionally, it does at times feel as if some programming languages are unnecessarily complicated. For instance, a commenter in the article cited web applications as an instance where the language was unnecessarily complicated. Web applications, as described by the commenter, are a collection of languages and technologies MacGuyver-ed together, which it really does not have to be. It might be a nicer alternative to have the collection of languages amalgamated in some object interface with a more natural syntax.  We believe it is necessary to find sensible ways of making it easier for novice programmers to being learning. However, we sympathize with the substance of the majority of commenters’ arguments, and not the article’s argument. The article appears to argue for translating programming languages into natural language without understanding the underlying reasons behind the design of a programming language. If anything, the article makes it seem as if the syntax of some programming languages are made haphazardly. There are reasons why a programming language is its own language, whether it be for organizational purposes or for domain specific purposes. As its own language, a programming language is distinct from natural languages and therefore will require the same work of learning a new language. 

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

   These two experiences of natural languages seem extremely at odds with one another. While Pavlus argues that natural language is preferable to the typical syntax in programing languages, Cook has anecdotal evidence that says the contrary. Both experiences seem to agree that natural language is significantly easier to read, but they disagree on the ease of actually writing programs with natural language. However, we found it unclear whether or not the subjects in Cook’s experiment were novice or professional programmers. Had they been professional programmers, it would be more difficult to argue that natural language does not have a place in programming, as we felt natural language would be particularly helpful for those just learning how to program. It makes sense that professional programmers accustomed to the “abstruse” syntax would find AppleScript to be far more troublesome. Additionally, each experiment seemed to differ with respect to the context of the situation: in the experiment cited by Pavlus, it seems the subjects were given no instructions, whereas in Cook’s experiment, the subjects seemed to have some form of guidance. 
   We would choose to include natural language, in a very limited scope. Our incorporation of natural language in a DSL would be in very local instances, such as function or method names and the names of built in types or objects, these names are useful to the humans interacting with the code in making it clear what such things do, but when we write something that is a less concrete idea in a natural language, such as a for loop, we would use traditional computer programming idioms.

---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**

   We read all five articles independently. We then met to discuss and write outlines for the questions together. Rebekah wrote up the answers to questions 1,3,5 and William wrote up the answers to questions 2,4,6 and 7. We then read over each others’ answers, edited them, put them into the markup file and submitted.

---
