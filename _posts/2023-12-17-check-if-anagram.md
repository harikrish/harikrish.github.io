---
layout: post
title:  "Check if string is anagram?"
date:   2023-12-17 07:22:00 -0800
categories: [JavaScript, Interview, Coding]
---

Steps:
- Pass two strings `word` and `anagram`
- Iterate over first string `word`, get character at `i`
- If character present in `anagram`, then remove character from `anagram`
- Iterate until `anagram` is empty


{% highlight javascript %}
function isAnagram(word, anagram) {
    if (word.length !== anagram.length) {
        return false;
    }
    for (let i = 0; i < word.length; i++) {
        let c = word[i];
        let index = anagram.indexOf(c);
        if (index === -1) {
            return false;
        }
        anagram = anagram.substring(0, index) + anagram.substring(index + 1, anagram.length);
    }
    return anagram.length === 0;
}

isAnagram('hello', 'olleh');
{% endhighlight %}



### References:
- [How to check if two Strings are Anagrams in Java](https://java2blog.com/check-if-two-strings-are-anagrams-in-java-example-program/)