# Weekly Tech Round Up 8/26/24
## DARPA Proposes AI powered migration to Rust
In what is possibly the most trendy move of 2024, DARPA (Defense Davanced Research Projects Agency)
proposes a solution to memory based vulnerabilities using LLMs(Large Language Models) to turn
legacy C code into idiomatic Rust code.
### Why Rust?
Rust has been hailed as the solution to memory safe
systems level programming language for it's innovative memory management system. It lives in a middle land
languages like C require developers to explicity allocate and deallocate memory from the heap, opening the
program to a plethora of security vulnerabilities like free after use or the classic buffer over flow.
Rust is not garbage collected, but instead operates with a system called the borrow checker.
In theory it is an incredibly intuitive system that almost gaurentees memory saftey at compile time.
It forces developers to think of memory and memory pointers as a real resource. If I want to create
a new variable I am it's owner and if I want to loan it to my friend (another function/scope) I allow them
to borrow it. It would be very rude if my friend threw it in the trash when I expected them to return it.
This is the essence of the borrow checker, but the rust documentation has a great step by step guide to
learning rust if you are interested in more.
### Rusts's Potential?
While many developers are excited to use rust, with  83% of stack overflow annual survey
respondees indicating they would like to work with the language in the future [src.](https://survey.stackoverflow.co/2024/);
The issue remains that rust is complicated, that borrow checker analogy makes sense for a hello world program,
but imagine thinking through concurrent or mutable examples. Many companies are moving towards Rust, but
when it comes to systems level programming C or C++ is still king. It in essence boils down to the fact that
rust is 9 years old, so your most senior rust engineer will have 9 years of most likely non-professional experience
While C is literally older than my own dad meaning plently of C experts have already retired. C has been
battle tested while rust is the new kid on the block that seems to be turning a lot of heads, but will
the hype last?
### DARPA's Proposal
DARPA's newest proposal indicates it could have some staying power. Writing,

> "DARPA's Wallach thinks that LLMs will almost certainly be part of the solutions." [src](https://www.darkreading.com/application-security/darpa-aims-to-ditch-c-code-move-to-rust).


Citing that LLMs make a transition from functioning C code to rust easier than it has ever been.
They do note that a lack of Rust code has provided some errors in LLMs like Chat GPT and Co-Pilot.
So make sure to keep comitting high quality rust code to private github repos (allegedly).
Anyone who has
used LLM's as a coding companion can attest they can at times provide amazing speed ups that improve effciency,
however, they can also be a foot gun that causes huge slow downs when the language model just pretends
methods on a class exist especially with the lack of Rust code examples in exsistance things like concurrency
can become a real problem to deal with. The first time I had to use a Box or Arc which are common data types
for handling pointers in concurrent Rust chat gpt lost it's mind and couldn't even get it to compile by itself.

## End of React?
A stir was caused on web development communities online(when isn't it) when an article was released proposing a new era of
javascript may be approaching. Stating companies may begin leaving giants like react behind.
This is exciting news, many companies that will save a lot of time migrating enterprise website that still ran
jquery and vanilla js.
### What's the alternative?
This can be seen as new technology like HTMX has generated a lot of intrigue for
what C#'s MVC Core has been doing for years, server side rendering. The era of the Single Page Application
with a 10mb javascript file seems to be approaching an end in the trendier circles of tech with solutions
with Angular and react implementing server side rendering solutions.
### Wait what were we doing before? I haven't written HTML since flash player
A SPA is a site that loads HTML with a reference to a
javascript tag which then loads all the javascript required to run the page. This javascript then makes API calls
to a server and parses the data into whatever information the HTML needs to show and changes the HTML accordingly.
That's 3 separate network calls to get a single page. Server side rendering allows smaller javascript bundles
as only interactive pieces use javascript i.e. search bars or buttons, however, next.js's server actions has
even turned these into server only interactions. A server side rendered page only makes 1 call to the server to grab the HTML
if you make a search a new call is made to the sever which behind the scenes queries the DB, performs the business logic,
and returns the appropiate HTML for you. In theory faster over slower connections and potentially safer by reducing the code
ran on the client(I'm sure I'll be proven wrong in a year's time).


## Bun ups their speed
For the past few years a battle has been warring between the titan of backend javascript runtimes, node.js
a plethora of modern alternatives like bun and deno. Node has provided an easy to use, scalable solution that
handles concurrency well for years. However, in recent times many developers have been frustrated with
slow speeds when compared to compiled or especially non garbage collected languages. Typescript a type "safe"
alternative to javascript which has been defacto industry standard is also not supported by Node.JS without
a intermediary compiler. Which can often times be complicated to set up. New improvements are being made by Bun
a node.js alternative as they released v1.1.26.
Bun has now released v1.1.25 that can reportedly process 1.29 million HTTP requests per second.
These benchmarks were reported by Bun so I would take them lightly, but if they are true it is over 10x
the number of Node.JS. In the cloud dominated web development environment a 10x speed up, could easily
save thousands a month. While alternatives like go-lang or rust may be even faster, it's hard to argue
with Bun's backwards compatability.

