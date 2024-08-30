# Dev Tools I couldn't live without

Developer experience is often talked about when discussing libraries or programming languages.
However for me my tools are entirely what make my development experience enjoyable.
For me any language with suffcient time can have an enjoyable developer experience (besides python, but we'll get to why)
It's the environment I've created on my machine that defines my productivity. I feel most comfortable
using neovim to work on typescript and go-lang projects, however, I'm sure with enough time I'd feel just
as productive in rust, C++, or even java. So I want to talk about how I found my ideal dev environment,
and the tools that make me more productive in my day to day. We'll start from the bottom and go to the top.

## Operating System
For my daily coding at home I use Arch btw, but for my work machine I just want something that
will work 100% of the time so I don't log in at 8am ready to work some tickets and have to debug some
new arch release. To be honest I don't really care about distro and mainly chose Arch for my home machine
to teach myself more about the low level concepts of linux. The main reason I choose linux is the control and shell. I can stomach using mac
since I can still install zsh but I can't live without pacman or yum. I've tried brew on mac, but nothing
beats linux's package manager support. And insert some moral pontificating about open source software here

## Shell
Like I mentioned above I use zsh which for me is just too good to go without especially when paired
with the extension (Oh My Zsh)[https://ohmyz.sh]. Features like showing what git branch I'm in on my prompt
line, auto complete and history are huge time savers for me.

## Terminal Emulator
This one is mainly asthetic I just love the rose-pine theme so I like a terminal I can configure to use
premade themes like the classy demure rose-pine. But some things I cannot live without is a terinal
with tabs. The projects I work on all require me to have atleast 2 tabs open, but my regular setup is in a monorepo
with 1 tab for running the backend/frontend in split windows. One window with neovim editing the backend code and a third window editing the frontend code.

## Neovim (btw)
The absolute biggest jump in productivity I have seen in my workflow is using a well configured neovim setup.
I first gave neovim a try around a year and a half ago and before that I was a total vs-code bro.
After watching Primeagen rage on and on about how could neovim was and watching him fly around the terminal
I forced myself to use neovim for a week straight. It was also one of the most painful things I've ever done
I was constantly not in insert mode while trying to type or leaving js and ks around trying to navigate files.
However, that's my main point of this post, if you think your dev environment could be better in any way just
change it and force yourself to use it until you love it or hate it. But give it a chance so you can articulate why
that workflow doesn't work for you. Worst case you learn something about your workflow and best case you get
some productivity gains. Neovim offers everything I need in an editor like language server while forcing me to get used
to navigating my code through hotkeys which after becoming muscle memory have increased my speed massive amounts.
I also re-evaluated what information was important in my editor. Using vs-code you're basically in a file explorer
with a code editor in the middle. With neovim the code is 100% of my screen and the only status bar I have is the
vim mode, git status, and error messages.
That being said I do not run a base neovim setup I have some plugins like an lsp, harpoon for file switching, and telescope for fuzzy file searching.
Check out my (dot files)[https://github.com/gbc-collib/dotfiles] for more if you're interested. I also love lua for scripting language but that's a topic for another time
I found that most of my file surfing I do anyway is through my LSP, like navigating to a function definition or to a variable definition which after
using neovim and realizing I could bind to hotkey gd which made my file surfing even faster.

