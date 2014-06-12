Outline:

1. Principles of Test Driven Development
  a. Test First
  b. Red-Green-Refactor
  c. What to test
  d. Tests within the workflow
2. Setting up RSpec
3. Model Validation Testing
4. REST Controller Testing
5. Testing API calls

Principles of Test Driven Development

Different people have different learning styles. I like to delve into the principles and philosophy before jumping in so that is where I'm starting. If that doesn't work for you, feel free to jump in with "Setting up RSpec."

Test First:

Red-Green-Refactor:

What to test:

Tests within the workflow:

Setting up RSpec:

First step whenever you are working with a new gem is to check out the README. There is usually some great setup information. Check out the information for applying rspec to rails here. https://github.com/rspec/rspec-rails

Make sure that you have:
- Set up the Gemfile correctly
- Run bundle install
- Generated the rspec installation

There are other things you can configure at this point in the spec-helper.rb file.

At this point I recommend you also add the simplecov gem. It allows you to look at how extensively your code is covered by your tests. This can help by showing you things that you have forgotten to test. Particularly looking at more than just the happy path. https://github.com/colszowka/simplecov

Again, make sure that you have:
- Set up the Gemfile correctly
- Run bundle install
- Edit the spec_helper.rb file




