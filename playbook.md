---
layout: page
title: Playbook
comments: false
---

<div style="padding: 10px 20px; background-color: orange; color: white;
text-align: center">This document is working in progress...</div>

<h2>Introduction</h2>

This is my personal playbook to become a better developer each day.  My focuses are working with Ruby (RoR), Javascript (ReactJS, D3, etc), Salesforce, and Swift (Hobby).  These are technologies I enjoy using and learning everyday.

### Mission Statement
Be humble yet confident. Learn new things each day to improve the world one code
at a time.

<h3 id="vim-and-tmux" style="padding-top: 30px;">My Editor of Choice: Vim and Tmux</h3>

The editor you choose for your workflow speaks a lot about your dedication to your craft, in our case that is developing software.  Text editor is my essential tool, and my favorite is Vim.  I was inspired by developers from <a href="https://thoughtbot.com/" target="_blank">Thoughtbot</a> years ago when I saw how fast it can improve your Rails development. If you are curious, here are my <a href="https://github.com/antwonlee/dotfiles" target="_blank">dotfiles</a>.


<h2 id="test-driven-development" style="padding-top: 30px;">Test Driven Development</h2>

I learned majority of my Test Drivent Development for Ruby on Rails from <a href="https://thoughtbot.com" target="_blank">Thoughtbot</a>'s resources: <a href="https://upcase.com" target="_blank">Upcase</a> program and <a href="https://gumroad.com/l/testing-rails?utm_source=giant-robots&utm_medium=blog&utm_campaign=announcement" target="_blank">Testing Rails</a> book.

My philosophy of writing tests are to be confident of your code.  I strive to write tests that tell good stories and documentation of your application, while making it simple and easy to understand for other developers.


### Simple Feature Spec

Here is a simple feature spec that follows <a href="https://robots.thoughtbot.com/how-we-test-rails-applications" target="_blank">four phases of Testing: Setup, Exercise, Verification, Teardown</a>.  I also try to avoid rspec `let` arguments that can sometimes cause duplication in your test code and making it more complicated for other people to understand.

<script src="https://gist.github.com/antwonlee/ba28c43be278e28ff31cd26c787d169c.js"></script>

<h2 id="how-i-solved-the-code-challenge" style="padding-top: 50px;">Code Challenge and Solution in Production</h2>


**Challenge:** 

<ul style="line-height: 1.5em;">
  <li>
    As a donor I want be able to give one time or recurring donation, so that I have the choice to give the amount and frequency I desire to give.
  </li>
  <li>
    As a donor I want to get email donation receipt, so that I don't have to deal with paper mail.
  </li>
</ul>



**My Solution:** 

+ Use Stripe API for payment system, because it gives developer maximum flexibility.
+ Build relational database in Postgres that mirrors the Stripe structure to
  keep the data clean and prevent duplication in Stripe during payment process.
+ Use Redis and Sidekiq for queueing email receipts so it diminishes delay time
  for users during payment process.
+ Write clear meta data for Strip so you have more control regards API integrations in the future.
+ Create pre-dunning, dunning emails to not lose recurring donors.
+ Use Baremetrics for measuring MRR, churn, and other business data.

<h4 style="padding-bottom: 35px;">Code Sample</h4>

This are production code for <a href="https://thriveministry.org" target="_blank">Thrive Ministry</a>.

<script src="https://gist.github.com/antwonlee/db50b861b47919c2d18478cdb4d599db.js"></script>

<h2 id="rest-api-implementation-sample" style="padding-top: 30px;">REST API Implementation Sample</h2>

One of the biggest challenge developers face is integrating multiple systems. [WIP... start from here again.]

<script src="https://gist.github.com/antwonlee/7a66a0ddc415bf25a7517bd3aacbf9db.js"></script>

<h2 id="javascript-json-ajax-endpoints" style="padding-top: 30px;">Style: Sandi Metz Rules</h2>

<div style="width: auto; margin: 0 auto; text-align:center;">
  <img src="https://hectorperezarenas.files.wordpress.com/2015/10/poodr.jpg" style="width: 150px;">
</div>

+ [WIP: Add description]
+ [WIP: Add Code Samples]

<h2 id="javascript-json-ajax-endpoints" style="padding-top: 30px;">Javascript,
REACTJS, D3, JSON, AJAX, Endpoints</h2>

Post some ReactJS, D3, and other javascript samples of my work...

[WIP: Add demo app that read, parse and print data with node.js]

<script src="https://gist.github.com/antwonlee/a735b4e675570c3513c47257364dbb01.js"></script>

+ [WIP: Add description]
+ [WIP: Add Code Samples]

<h2 id="design" style="padding-top: 30px;">Styles</h2>

+ [WIP: Add description]
+ [WIP: Add Code Samples]

<h2 id="good-git-commits" style="padding-top: 30px;">Good Git Commits</h2>

+ [WIP: Add description]
+ [WIP: Add Code Samples]

<h2 id="tools-i-use" style="padding-top: 30px;">Tools I Use</h2>

+ [WIP: Add description]
+ [WIP: Add Code Samples]
