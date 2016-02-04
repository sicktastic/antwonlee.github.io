---
layout: page
title: Playbook
comments: false
---

<div style="padding: 10px 20px; background-color: orange; color: white;
text-align: center">This document is working in progress...</div>

This is my personal playbook to become a better developer each day.  Currently, my focuses are working with Ruby on Rails, ReactJS, Swift, and Salesforce development.  These are technologies I enjoy using.

My philosophy of being a good developer is always to be humble and learn new things to improve the world. :sunglasses:

I am an avid learner.  My mentors include:

<ul style="line-height: 1em;">
  <li>Computer Science professors from Georgia Tech Masters Program</li>
  <li>Thoughtbot developers from Upcase program and blogs</li>
  <li>Pluarsight, Egghead, Treehouse, Lynda</li>
  <li>Peer developers</li>
</ul>

<br />

<h1>Table of Contents</h1>
<a id="test-driven-development" style="font-size: 1.25em">[Test Driven Development](#test-driven-development)</a>
<ul style="line-height: 1em;">
  <li><a href="#">Using RSpec</a></li>
  <li><a href="#">Simple Model Spec Style</a></li>
  <li><a href="#">Simple Feature Spec Style</a></li>
</ul>

<strong style="font-size: 1.25em">[External Services with Ruby on Rails](#)</strong>

<ul style="line-height: 1em;">
  <li><a href="#">Stripe Payment Process</a></li>
</ul>

<h1 id="test-driven-development">Test Driven Development</h1>

I learned majority of my Test Drivent Development for Ruby on Rails from <a href="https://thoughtbot.com" target="_blank">Thoughtbot</a>'s resources: <a href="https://upcase.com" target="_blank">Upcase</a> program and <a href="https://gumroad.com/l/testing-rails?utm_source=giant-robots&utm_medium=blog&utm_campaign=announcement" target="_blank">Testing Rails</a> book.

My philosophy of writing tests are to be confident of your code, and to make it simple and easy to understand.

####Simple Model Spec Style

```ruby
FactoryGirl.define do
  factory :author do
    name "Bat Man"
    bio "Batman is a fictional superhero."
  end
end
```


```ruby
require "rails_helper"

describe Author do
  it { should validate_presence_of :name }
  it { should validate_presence_of :bio }

  describe "#create_author" do
    it "creates author" do
      author = build(:author)

      expect(author.name).to eq("Bat Man")
    end
  end
end
```

This test simply validates the name and bio of Author model and tests if it successfully performs create_author method.

(WIP: Put simple code and descriptions?)

####Simple Feature Spec Style
```ruby
require "rails_helper"

feature "User sees" do
  scenario "their lead records successfully" do
    visit leads_path
    current_user = build(:user)
    fill_in "user_email", with: current_user.email 
    fill_in "user_password", with: current_user.password
    click_on "Log in"
    expect(page).to have_content current_user.guestbook_user_id
  end
end
```
