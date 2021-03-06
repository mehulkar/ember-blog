---
title: The Ember Times - Issue No. 156
author: Chris Ng, Abhilash LR, Jared Galanis, Amy Lam
tags: Recent Posts, Newsletter, Ember.js Times, Ember Times, 2020
alias : "blog/2020/07/17-the-ember-times-issue-156.html"
responsive: true
---

👋 Emberistas! 🐹

Read the blog post on using ember-concurrency with TypeScript 🤝,
reusable DOM behavior in React vs Ember 🪔,
and last, but not least, Mirage JS with GraphQL 🏝!

READMORE

---

## [Using ember-concurrency with TypeScript 🤝](https://jamescdavis.com/using-ember-concurrency-with-typescript/)

[James C. Davis (@jamescdavis)](https://github.com/jamescdavis) wrote a blog post summarizing how to use [TypeScript](https://github.com/microsoft/TypeScript) with [ember-concurrency](https://github.com/machty/ember-concurrency) as well as some best practices.

ember-concurrency is an addon that manages asynchronous tasks in Ember applications. The addon traditionally exports a `task` function which is used similarly to a computed property.

```js
import { task } from 'ember-concurrency';

export default Component.extend({
  myTask: task(function*() {
    yield foo;
    return bar;
  })
}
```

The blog post goes through how to use ember-concurrency with Ember Octane and TypeScript. For Octane, we need to use Native Class Syntax. The [ember-concurrency-decorators](https://github.com/machty/ember-concurrency-decorators) package was created to make this work for ember-concurrency.

However, decorators cannot change the type of the thing they decorate. To allow TypeScript, the [ember-concurrency-ts](https://github.com/chancancode/ember-concurrency-ts) package was created to provide a couple of utility functions such as `taskFor`. 

Finally, the [ember-concurrency-async](https://github.com/chancancode/ember-concurrency-async) package provides a Babel transform that allows you to define ember-concurrency tasks using async/await rather than generator function. This simplifies using `taskFor` on assignment while providing complete type-safety for ember-concurrency tasks.

Read the [full blog post](https://jamescdavis.com/using-ember-concurrency-with-typescript/) with all the tips and tricks and try it out yourself today!

---

## [Reusable DOM behavior in React vs Ember 🪔](https://dev.to/rajask05/reusable-dom-behavior-in-react-vs-ember-4p04)

[Raja SK](https://github.com/RajaSK05) wrote a blog post comparing React and Ember's approach to creating reusable components that deal with DOM behaviors. He talks about how to approach the same using the following patterns:

- React's class-based and functional component approach
- Ember's mixin and **modifier** approach.

He also talks about how to use the [ember-modifier](https://github.com/ember-modifier/ember-modifier) addon if you have been using the Ember mixin patterns so far for DOM behaviors and sharing code between components.

Read the [full blog post](https://dev.to/rajask05/reusable-dom-behavior-in-react-vs-ember-4p04) today!

---

## [Mirage JS with GraphQL 🏝](https://github.com/miragejs/graphql)

 Have you been wanting to use [Mirage JS](https://miragejs.com/) with GraphQL? 
 
 Thanks to [Rocky Neurock (@jneurock)](https://github.com/jneurock), [Mirage GraphQL](https://github.com/miragejs/graphql) provides the ability to create a GraphQL route handler based on your GraphQL and Mirage schemas.

 Mirage GraphQL does a bunch of things: 

- It fulfills GraphQL requests by fetching data from Mirage's database.
- It filters records from Mirage's database by using arguments from your GraphQL queries.
- It handles create, update and delete type mutations automatically based on some conventions.
- It allows you to supply your own resolvers (for cases where the automatic query and mutation resolution isn't sufficient).

There's plenty of examples on how to get started using GraphQL with Mirage JS using Mirage GraphQL over at the repo, go ahead and [check them out for yourself](https://github.com/miragejs/graphql#example-use-cases). 

---

## [Contributors' corner 👏](https://guides.emberjs.com/release/contributing/repositories/)

<p>This week we'd like to thank <a href="https://github.com/kiwiupover" target="gh-user">@kiwiupover</a>, <a href="https://github.com/rwjblue" target="gh-user">@rwjblue</a>, <a href="https://github.com/pzuraq" target="gh-user">@pzuraq</a>, <a href="https://github.com/rjschie" target="gh-user">@rjschie</a>, <a href="https://github.com/arthirm" target="gh-user">@arthirm</a>, <a href="https://github.com/kategengler" target="gh-user">@kategengler</a>, <a href="https://github.com/richgt" target="gh-user">@richgt</a>, <a href="https://github.com/JoaoDsv" target="gh-user">@JoaoDsv</a>, <a href="https://github.com/snewcomer" target="gh-user">@snewcomer</a>, <a href="https://github.com/igorT" target="gh-user">@igorT</a>, <a href="https://github.com/st-h" target="gh-user">@st-h</a>, <a href="https://github.com/mansona" target="gh-user">@mansona</a>, <a href="https://github.com/pdud" target="gh-user">@pdud</a>, <a href="https://github.com/mehulkar" target="gh-user">@mehulkar</a>, <a href="https://github.com/bmish" target="gh-user">@bmish</a>, <a href="https://github.com/jaredgalanis" target="gh-user">@jaredgalanis</a>, <a href="https://github.com/abhilashlr" target="gh-user">@abhilashlr</a>, <a href="https://github.com/chrisrng" target="gh-user">@chrisrng</a>, <a href="https://github.com/jenweber" target="gh-user">@jenweber</a>, <a href="https://github.com/nickschot" target="gh-user">@nickschot</a>, <a href="https://github.com/sly7-7" target="gh-user">@sly7-7</a>, <a href="https://github.com/superlou" target="gh-user">@superlou</a>, <a href="https://github.com/amyrlam" target="gh-user">@amyrlam</a>, <a href="https://github.com/hergaiety" target="gh-user">@hergaiety</a>  for their contributions to Ember and related repositories! 💖</p>

---

## [Connect with us! 🤓](https://docs.google.com/forms/d/e/1FAIpQLScqu7Lw_9cIkRtAiXKitgkAo4xX_pV1pdCfMJgIr6Py1V-9Og/viewform)

<div class="blog-row">
  <img class="float-right small transparent padded" alt="Office Hours Tomster Mascot" title="Readers' Questions" src="/images/tomsters/officehours.png" />

  <p>Wondering about something related to Ember, Ember Data, Glimmer, or addons in the Ember ecosystem, but don't know where to ask? Readers’ Questions are just for you!</p>

  <p><strong>Submit your own</strong> short and sweet <strong>question</strong> under <a href="https://bit.ly/ask-ember-core" target="rq">bit.ly/ask-ember-core</a>. And don’t worry, there are no silly questions, we appreciate them all - promise! 🤞</p>

  <p>Want to write for the Ember Times? Have a suggestion for next week's issue? Join us at <a href="https://discordapp.com/channels/480462759797063690/485450546887786506">#support-ember-times</a> on the <a href="https://discordapp.com/invite/zT3asNS">Ember Community Discord</a> or ping us <a href="https://twitter.com/embertimes">@embertimes</a> on Twitter.</p>

  <p>Keep on top of what's been going on in Emberland this week by subscribing to our <a href="https://the-emberjs-times.ongoodbits.com/">e-mail newsletter</a>! You can also find our posts on the <a href="https://emberjs.com/blog/tags/newsletter.html">Ember blog</a>.</p>
</div>

---

That's another wrap! ✨

Be kind,

Chris Ng, Abhilash LR, Jared Galanis, Amy Lam and the Learning Team
