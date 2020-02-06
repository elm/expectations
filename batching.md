
# Batching

Work on issues and pull requests happens in periodic batches, not one-by-one as they come in.

This means that a &ldquo;simple&rdquo; issue on `elm/core` may be blocked by ongoing work on the package website or compiler, but we think this has some important and worthwhile benefits.


### Coherent Design

Issues that look &ldquo;simple&rdquo; are often much more interconnected than they seem.

Imagine there are 20 suggestions on how to make something better. Taken *individually*, each one is probably pretty easy to deal with. Taken *together*, you are talking about quite serious design changes. Does that design have a coherent vision? Is it directed at the needs of your intended users? Do all the parts fit together? Can you find a simpler design that addresses all 20 suggestions in a nicer way?

The major benefit of batching is that the review process is *structured* for coherent design. By allowing time for folks to share their experiences and suggestions, it becomes possible to consider them all together and better balance their needs. Shifting towards real-time responses on everything would necessarily degrade the overall design quality.


### Focus

Doing this kind of design work requires focus. Compiler work requires getting deeply immersed in the problems people face and the details of the code. What is needed? What is possible? Same for the package manager, the REPL, the documentation, the core packages, etc. The problem is:

  1. It is not possible to be deeply immersed in all of these projects at the same time.
  2. An unfocused process does not tend to produce coherent design.

Batching really helps with this. Focusing on high quality work has produced some of the best ideas in Elm. For example, while adding the `--output=json` flag, we realized that type error messages could really great. No one thought that was possible with ML-family languages before! Even the designer of Elm! Same thing happened with the parser. While improving parser performance, we realized that the parse error messages could be very dramatically improved. The very best parts of Elm have all come from focused exploration, not from rigid scheduling or unstructured online discussion.


## An Example

I think [this issue](https://github.com/elm-lang/elm-package/pull/177) shows what batching and holistic design mean in practice.

It took about a week to revamp all the error messages for `elm-package`, ultimately leading to the fix in this case. Should [Elm 0.17](http://elm-lang.org/blog/farewell-to-frp) have blocked for an extra week for this? Is it smart to have so many changes in a single release? Do these changes fit into the overall narative of the release?

In the year 2017 or 2030, users will only know if things are nice or if they suck. January or July of 2016 makes no difference to them. So waiting a few months feels like a long time to us, but it is not about us!

When a project is going to live for decades, it is better to do things *right* than to do things *right now*.
