---
layout: page
title: Playbook
comments: false
---

<div style="padding: 10px 20px; background-color: orange; color: white;
text-align: center">This document is working in progress...</div>

<h2>Introduction</h2>

This is my personal playbook to become a better developer each day.  Currently, my focuses are working with Ruby on Rails, Salesforce, Swift, and ReactJS development.  These are technologies I enjoy using and want to learn.

### My philosophy of being a good developer (Mission Statement):
Be humble yet confident. Learn new things each day to improve the world one code
at a time.

<h1>Table of Contents</h1>
<a id="test-driven-development" style="font-size: 1.25em">Editor</a>
<ul style="line-height: 1em;">
  <li><a href="#">Vim and Tmux</a></li>
</ul>
<a id="test-driven-development" style="font-size: 1.25em">Test Driven Development</a>
<ul style="line-height: 1em;">
  <li><a href="#">RSpec</a></li>
  <li><a href="#">Test Doubles</a></li>
  <li><a href="#">Stubs, Mocks, Spies, and Fakes</a></li>
</ul>

<h2 id="vim-and-tmux" style="padding-top: 30px;">Vim and Tmux</h2>

The editor you choose for your workflow speaks a lot about your dedication to
your craft, in our case that is developing software.

<h2 id="test-driven-development">Test Driven Development</h2>

I learned majority of my Test Drivent Development for Ruby on Rails from <a href="https://thoughtbot.com" target="_blank">Thoughtbot</a>'s resources: <a href="https://upcase.com" target="_blank">Upcase</a> program and <a href="https://gumroad.com/l/testing-rails?utm_source=giant-robots&utm_medium=blog&utm_campaign=announcement" target="_blank">Testing Rails</a> book.

My philosophy of writing tests are to be confident of your code, and to make it simple and easy to understand.


### Simple Feature Spec

{% highlight ruby %}
require "rails_helper"

feature "User submits Retreat Attendee Registration form" do
  scenario "successfully" do
    visit new_retreat_attendee_registration_path
    submit_new_retreat_registration_form

    expect(page).to have_content "Thank you, Doctor Who"
  end

  private

  def submit_new_retreat_registration_form
    retreat_attendee = create(:retreat_attendee_registration)

    fill_in "First Name", with: retreat_attendee.first_name
    fill_in "Last Name", with: retreat_attendee.last_name
    fill_in "Email Address", with: retreat_attendee.email_address
    fill_in "Country of Service", with: retreat_attendee.country_of_service
    fill_in "Current Status", with: retreat_attendee.current_status
    fill_in "Years Worked", with: retreat_attendee.years_worked
    fill_in "Sending Agency", with: retreat_attendee.sending_agency
  end
end
{% endhighlight %}
