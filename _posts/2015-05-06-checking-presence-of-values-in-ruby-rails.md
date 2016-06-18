---
layout: post
title:  "Checking the presence of values in Ruby and Rails"
date:   2015-05-06
excerpt: "Rails provides you with a few methods to check if a variable has a value or contents or is nil. Methods like any?, present? or nil?. When working with one type of variable they usually work as you expect, but i’ve come across situations where they might not work as you expect!"
tag:
- ruby
- rails
comments: true
---

Rails provides you with a few methods to check if a variable has a value or contents or is nil. Methods like any?, present? or nil?. When working with one type of variable they usually work as you expect, but i’ve come across situations where they might not work as you expect!

I was working on a project where i had a dynamic component where i needed to check if a value was not nil. But the value could be a string, number or boolean. And when it was a boolean it always failed. So i went to inspect why. Turns out, a boolean with value False returns false when checked with present?. Which i find ridiculous but it is what it is!
Why is that though? I assume present? is false when there’s no value attached to the variable. False is a value so why is it still false? Present? is the opposite of blank? and the Rails docs says this


> blank?() public
> An object is blank if it’s false, empty, or a whitespace string. For example, ”, ‘ ’, nil, [], and {} are all blank.

False just is blank or not present. So you could say just use nil?. But no because that returns false when its an empty string, and in my case that should be true. So i’m stuck between a rock and crazy place.
I just decided to create my own method.

```ruby
def present?(value)
  value != “” && value != nil
end
```

So a value = false would return true in this method, and an empty string would too. To clarify when what method for checking existence of values returns what i copied a table from this page.

Just keep this table next to you and you’ll be fine!
![table](https://cdn-images-1.medium.com/max/1600/1*YWr_HNb7v_IX4cxbdaZ4QA.png)
