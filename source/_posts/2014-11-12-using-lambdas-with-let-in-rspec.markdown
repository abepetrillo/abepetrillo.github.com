---
layout: post
title: "Using lambdas with let (in rspec)"
date: 2014-11-12 19:36:57 -0500
comments: true
categories: [rspec, ruby, testing]
---

As many of you already know, `let` has been a great improvement on declaring instance variables
in our `before :each` blocks. Lazy loading on when it's used while being kept in memory for the
duration of the test. One way in which we use lets, for more complicated variable definitions, is to
use let, and provide it with arguments using a lambda:

```ruby
let(:user) {
    ->(name, email) {
      double("user", user: email, email: email)
    }
  }
```

You can then easily setup users in your test:

```ruby
describe 'Given a user' do
  context 'with internal address' do
    it 'redirects to intranet' do
      login_as user['Bob', 'bob@internal.com']
      ...
    end
  end
  context 'with external address' do
    let(:staff_user) { user['Bob', 'bob@internal.com'] }
    it 'redirects to external domain' do
      login_as user['Pete', 'pete@gmail.com']
      ...
    end
  end
end
```
