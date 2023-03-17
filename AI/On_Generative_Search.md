# On Generative Search

There's a new set of search engines coming, which instead of searching existing data generate (or supplement) it using AI models. 

I first saw a version of this on a Hacker News discussion[<sup>1</sup>](#cite1) where Google could not find anything about the equivalent of a particular island is Thailand for someone who was looking in Croatia. I considered Google's behavior here to be correct: no one had ever written anything like that on the visible web. 

However, in the comments someone tried GPT3. I tried this (using [GPT-NeoX 20B](https://textsynth.com/playground.html)):

> **The most similar island to  Koh Yao Yai in Croatia** is Ugljan. Ugljan has an area of 24.85 square kilometres, a highest altitude of 220 metres above sea level and has a population of about 450 people. The main language is Italian and there are also people of different nationalities living there. 
> There is a ferry connection with Ugljan via the port of Labin, where ferries to both Ugljan and Kastela depart. 

(prompt in **bold**).

To my ears, this sounds a perfectly reasonable if somewhat dry result. 

The next thing that piqued my interest was image generation, in particular texture generation for use in art programs. My son is a keen Blender user, and got the Stable Diffusion texture generation plugin working. Suddenly instead of searching for textures he was generating them. 

In environments like Unreal Engine that have asset stores it won't be long before they are generating missing assets on demand. 

It's pretty easy to imagine this being extended to code search in documentation. I foresee plugins for Docusaurus that extend the search to do StackOverflow-like question answering for specific projects. 

No, this won't be accurate much of the time. But for small projects that don't have a large userbase the ability to sometimes answer a question will be enough to make it useful. Models will improve on this quickly. 


## Problems with Generative Search

See that "search result" about Ugljan above? It's wrong. 

According to [Wikipedia](https://en.wikipedia.org/wiki/Ugljan), Ugljan has an area of 50.21 km<sup>2</sup>, population of 6049 and is connected to another island by a bridge. 

Currently this is a hard thing to detect and harder to fix. There is work in automated fact checking, and structured knowledge bases offer some partial solutions. But none are end-to-end or offer the high quality written text that language models give. 

We see similar issues with image generation. People think fake news images will be things posted on Twitter, but worse will be fake images posted as search results. What will the results for *Hollywood set used for fake moonlanding" look like? Or for "politician X doing Y with Z"?






























---
<a name="#cite1" >1.</a>
A discussion about the decline of Google Search results which I can no longer find.