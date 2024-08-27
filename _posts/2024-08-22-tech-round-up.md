# Weekly Tech Round Up 8/26/24
## DARPA Proposes AI powered migration to Rust
In what is possibly the most trendy move of 2024, DARPA (Defense Davanced Research Projects Agency)
proposes a solution to memory based vulnerabilities.
> "DARPA's Wallach thinks that LLMs will almost certainly be part of the solutions." [src](https://www.darkreading.com/application-security/darpa-aims-to-ditch-c-code-move-to-rust).


Citing that LLMs make a transition from functioning C code to rust easier than it has ever been.
They do note that a lack of Rust code has provided some errors in LLMs like Chat GPT and Co-Pilot.
So make sure to keep comitting high quality rust code to private github repos (allegedly).

## End of React?
A stir was caused on web development twitter/youtube when an article was released proposing a new era of
javascript may be approaching. Stating companies may begin leaving giants like react behind.
This is exciting news, many companies that will save a lot of time migrating enterprise website that still ran
jquery and vanilla js.


## Bun ups their speed
For the past few years a battle has been warring between the titan of backend javascript runtimes, node.js
a plethora of modern alternatives like bun and deno. Node has provided an easy to use, scalable solution that
handles concurrency well for years. However, in recent times many developers have been frustrated with
slow speeds when compared to compiled or especially non garbage collected languages. Typescript a type "safe"
alternative to javascript which has been defacto industry standard is also not supported by Node.JS without
a intermediary compiler. Which can often times be complicated to set up. New improvements are being made by Bun
a node.js alternative as they released v1.1.26.
Bun has now released v1.1.25 that can reportedly process 1.29 million HTTP requests per second.
Now your 1 user b2b SAAS will scale evern better. Bun also sports features like native typescript support,
backwards compatability with node APIs and
