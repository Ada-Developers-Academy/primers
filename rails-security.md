The Basics of Rails Security

Refer to the Rails Guides at: http://guides.rubyonrails.org/security.html

First of all, NEVER publish your <code>secret_token</code> to Github. Your <code>secret_token</code> can be found under your <code>config</code> directory. If you do, anyone can <a href="http://robertheaton.com/2013/07/22/how-to-hack-a-rails-app-using-its-secret-token/">HACK</a> your rails app!

To prevent this, follow the protocol described in "Sessions" in <a href="http://guides.rubyonrails.org/security.html">the Rails Guides</a>.

Sometimes, you'll encounter an exception caused by a line of code which gets automatically generated when you type <code>rails g controller ...</code>. This line contains </code>protect_from_forgery</code>, and you might feel tempted to delete it. After all, the exception will go away if you do. However, you open yourself up to CSRF(cross-site-request-forgery) attack. If your session cookie is not set to permanent, or if you use a cookie in addition to your session cookie, you need to handle it correctly, as described in the Rails Guides.

Keep an eye out for SQL injection vulnerabilities. See <a href="http://xkcd.com/327/">this comic</a>. Be sure to use <a href="http://en.wikipedia.org/wiki/Prepared_statement">prepared statements</a> and proper character escaping to avoid this.

... but how do I know if my Rails app is vulnerable?

If your app handles sensitive information, this is of huge importance. Run <a href="http://brakemanscanner.org/">Brakeman</a>. It's super easy -- <code>gem install brakeman</code> and then type <code>brakeman</code> into your terminal. It'll tell you what's up.

Now you're totally excited about maintaining iron-clad security in your Rails app. When the user gives you their password, you hash it. You're tempted to use the <i>fastest</i> hashing algorithm to do this because you're all about optimization BUT WAIT!
A slow hashing algorithm is more secure in this case, because if someone tries to <a href="http://en.wikipedia.org/wiki/Collision_attack">find a collision</a>in your hash, they can do it more quickly. The HTTP request will be your bottleneck anyway, so go ahead and use bcrypt.

Now what? Just Wikipedia-surf about this stuff -- there's a plethora of info out there on these topics. Generate your own PGP key. Sign my PGP key. Be secure!
