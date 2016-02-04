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
"We have to do this a lot when we write real computer programs: a thought that seems like a primitive in our minds turns out not to be a primitive in a programming language, and in each new program we must define it once more." [Steele, 1998]

I chose this quote because I thought it was epecially true and interesting. It highlights the differences in various programming languages. Perhaps if you take some primitives to be more important than others then you will perfer languages with those defined primitives. -Daniel

I've certainly found this to be the case in my experience programming. I'd also add that what does or doesn't turn out to be a primitive, as well as what you might expect to be a primitive, depends in some capacity on what you're used to. For a while after taking CS5, for example, I'd tend to want languages like Java to have as primitives bits of functionality that are primitives in Python. One specific example that comes to mind is that in Python, the built-in max (and min) function can be called
on lists and other collections, whereas Java's Math package only has max and min methods that take two numbers as arguments. -Aaron

"In a race, a small language with warts will beat a well designed language because users will not wait for the right thing; they will use the language that is quick and cheap, and put up with the warts." [Steele, 1998]

I chose this quote for two reasons. First, I think it's true but second it is a frustrating concept to me as I am somewhat of a perfectionist. I also do not think that choosing a poorly designed but easy to adopt language is better in the long run. In other words, I think it is the wrong choice. But people seem to choose it all the same. -Daniel

I think the fact that people choose it is a matter of practicality, and maybe expectation that the language _will_ get better. If people had, say, chosen to wait until Fortran had else statements (which it didn't for about 20 years, if Wikipedia is to be believed) then they would need to make a different choice or be stuck writing in assembly the whole time. -Aaron

"In Lisp, new words defined by the user look like primitives and, what is more, all primitives look like words defined by the user! In other words, if a user has good taste in defining new words, what comes out is a larger language that has no seams." [Steele, 1998]

I chose this quote becuase I am a firm belever in the 'no seams' language quality. I beleive that there should be as few exceptions to the language rules as possible. And if there are exceptions, they should only seem like exceptions on the surface but when unpacked, they actually do follow the rules. I am also a beleiver in a small set of rules. -Daniel

---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**
I think one of the symptoms of a well designed language is that, as Guy Steele says, "new words defined by a library should look just like primitives of the language." In other words, the language should be seamless.

I think a symptom of a poorly designed language is that there are many exceptions to the language rules. -Daniel

I would agree that the potential to grow seamlessly is quite important, because it can facilitate faster growth in languages. After all, "Lisp grew much faster than APL did, because many users could try things out and put their best code out there for other users to use and to add to the language." [Steele 1998] And the faster a language grows, potentially anyway, the sooner the icky bits get dealt with. One might determine whether a language is "seamless" by looking, but this isn't
completely foolproof and depends on what is classified as a primitive. For example, if everything in the Java standard library is a primitive, then Java is a pretty seamless language, but if not, then the standard library and all user libraries look a bit different than the primitives.

I would also say that intuitiveness is important as well (though I have to say that Quorum, as mentioned in the the Pavlus article, is intuitive because it's verbose, and I'm sure it would be a pain to actually write code in). Based on the large response to the proposed change in CSS in the Verou post, I would imagine that many people other than myself value intuitive languages; a language that is not intuitive will probably not get used very much and as a consequence won't grow much either.

One symptom of a poorly designed language is if it is distinctly not intuitive (although I admit this is by no means an objective measure). Even if a language can (or even does) grow, I would not consider it a well-designed language if it does things that don't make any sense (looking at [you](https://bugs.php.net/bug.php?id=45647) [PHP](https://bugs.php.net/bug.php?id=41523)) (for those who don't feel like following the link, the date/time 0000-00-00 00:00:00 is an error, but the
date/time 00-00-00 00:00:00 is actually November 30, 1999. I would not expect this, and would not consider it a good design decision.) -Aaron

---

**Question**

How do the themes of _Growing a Language_ relate to the lab we did this week?

**Response**
In the lab we had everyone in the class working to improve the same 'language'. I think that that speaks to the bazaar way of building a language. -Daniel

Agreed, although it was mostly the beginning stages of the bazaar style, since we didn't combine the best of all our work into a final language. -Aaron

---
 
**Question**


In what way is an API a language? 

**Response**
An API is a languge in that it has a predefined vocabulary and syntax. -Daniel

I don't think API's typically have syntax, although I guess chaining a few methods together could be part of an API and is kind of like syntax. In that case an API might resemble an internal DSL but still have the host language's flavor. In any case, as far as I understand, APIs are just the method (or function) names for a library, and Steele says "[a] true library does not change the rules of meaning for the language; it just adds new words." [Steele 1998] -Aaron


---

**Question**

What does the post on grayscale tell us about the process of API design?

**Response**
API design is like other types of design in that you need to get user feedback to find the best option and vocabulary. -Daniel

Agreed. Also, the widely varied opinions people expressed in the comments show that this tip is quite relevant: "You can't please everyone, so aim to displease everyone equally." [Bloch 2006] -Aaron


---

**Question**

The comments on the Pavlus article seem to set up a conflict between
professional programmers and everyone else. What is the essence of this
conflict? Do you sympathize more with the substance of the article's arguments
or with the substance of the majority of the commenters' arguments? Do you
sympathize more with the tenor of the article or the tenor of the majority of
the commenters?

**Response**
The essence of this conflict I think is logical vs non-logical syntax. Personally, I find some solace in programming because it is completely logical. The English language is not completely logical but I still enjoy using it for exactly that reason. English is a language all the same as any programming language. We could imagine that eventually, English will be a programming language and we will be able to speak it to computers and have them understand it. But technology is not that far along yet so as of now we have to speak to computers in a more logical language. This is solely because computers think with electrical circuits and bit (purely logical) and humans think with brain cells (which leaves room for interpretation). Some people would prefer computers think more like humans, but other technical minded people may always prefer to think like computers. -Daniel

I'm somewhat inclined to agree with the less arrogant and condescending commenters, for example the commenter who suggested that the tools of programming are no more complicated than those of any other technical profession. But there does seem to be a sense of elitism among many of them that I really can't get behind, and I can only agree with the above sentiment so far as general-purpose programming languages are concerned. I think that telling a computer what to do is something that is
useful for everyone to be able to do, and (I can't say with full confidence since I've only been in this class for a couple of weeks, but...) I think that's where DSLs come in. So I guess I'd say I agree with the commenters that things like Quorum shouldn't be general-purpose programming languages, but I would say that good DSLs might look a lot like Quorum does. -Aaron

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
I do not think they are at odds with eachother. Most people undeniably prefer to use natural language. However, the problem arises when they start to confuse a pseudo-natural language with actual natural language. Computers are not yet advnaced enough to actually interpret natural language so when you try to put natural language into a programming language, you are basically lying to the user. You are saying, I can understand natuaral language when really you cannot. This can cause the user errors. I most likely would not use natural language in the design of a DSL for exactly this reason. -Daniel

I don't think they're necessarily at odds with each other, but really what makes a natural-like programming language easy or difficult depends a lot on how much it looks like natural language. AppleScript, apparently, looks too much like natural language even though it is much less flexible. On the other hand, one of the things I like about Python is that code which would be "abstruse" in other languages (say, "for(int i = 0; i < foo.length; i++)" in Java) is more like natural language
(e.g. "for f in foo"). But Python is still recognizably not a natural language, and maybe that helps. I guess the short version is that I basically agree with Daniel. -Aaron


---

**Question**

Briefly describe how you split up the work for this assignment.

**Response**

We both responded to each prompt separately, but in the context of each other's responses in addition to the original prompt.


---
