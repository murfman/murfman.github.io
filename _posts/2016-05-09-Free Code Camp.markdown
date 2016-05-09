---
categories: update
tag: code

---

While browsing around on [GitHub](http://github.com) a few days ago, I came across the repo for [Free Code Camp](https://www.freecodecamp.com) and was intrigued. I am by no means a programmer, at best I can stumble my way through some simple codes, and after a while I might be able to understand the thing on the page. But my brain just doesn't seem to work this way. So a step by step course to teach HTML, CSS, JQuery, JavaScript, and BootStrap might be fairly useful.

The first project was a simple landing page using HTML and CSS3. You can see the results [here](https://codepen.io/murfman/full/mPaZPP/).

The second was a more complex portfolio page made from scratch. I think I was supposed to use some JQuery, but I didn't, since I don't really know how as of yet. You can see that one [here](https://codepen.io/murfman/full/xVMxgN/).

I started the course a few days ago and have made it about 150 slides, pages?, in and have finally hit a brick wall. The HTML/CSS/Bootstrap was easy enough, I learned HTML 20+ years ago and the base language is still the same. I taught myself CSS2 years ago, and so CSS3 wasn't too much of a step forward. But JavaScript is wholly new to me. And so I have hit a wall on something that is apparently so simple that I am seeing past it, or so fairly under-explained that the course is flawed. I'm tending to think of the former rather than the later.

Apparently, I am supposed to create some sort of little MadLibs like script using string operators to create a sentence from an array of words. Here is the code:

{% highlight javascript %}
function wordBlanks(myNoun, myAdjective, myVerb, myAdverb) {
  var result = "";
  // Your code below this line


  // Your code above this line
  return result;
}

// Change the words here to test your function
wordBlanks("dog", "big", "ran", "quickly");
{% endhighlight %}

I must admit I thought I had a few different thoughts on how to make it work, but to be fair, I'm lost. I thought this would work,

{% highlight javascript %}
result = "The " + (wordBlanks[1]) + " " + (worldBlanks[0]) + " " +
(wordBlanks.length -2) + " " + (wordBlanks.length-1) ;

{% endhighlight %}

But apparently I did something wrong. I suppose I need some help. I'll have to get some help on this.

As it turned out, I didn't need help. I just needed to pay more attention. I didn't notice that the array wordBlanks was being parsed and set to individual variable within the function. Once I saw that I realized what needed to be done.

{% highlight javascript %}
result = "The " + myAdjective + " " + myNoun + " " + myVerb +
" " + myAdverb + ".";
{% endhighlight %}

And that did it. They really should have explained arrays more before asking for that solution. They were covered in detail just afterwards. Perhaps it was by design? Or perhaps it was me looking at it last night with weary eyes and muffled brains that hurt more than anything.
