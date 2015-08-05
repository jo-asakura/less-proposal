# LESS-Proposal

Woundering how to push LESS preprocessor as a company's standard? Here you go. This [document](less-proposal.md) I created to make LESS as a standard in one of the companies I worked for.

##Transition to LESS

CSS is awesome, but it's increasingly `less productive` to author directly in. You don't write HTML and CSS directly anymore. It's proven to be unproductive writing native things that browsers digest. Abstracting one layer away is coming. It's all about being productive and `enjoy your coding` experience. Slightly weird that we care so much about the code that browsers digest behind the scenes and that travels across the Internet. So, we sacrifice our authoring experience for it. We shouldn't care what actually goes across the wire, we `care about authoring` and care what happens on a website.

Nowadays websites are a lot more complicated than it was a decade ago. As the capabilities of the web grow, we take advantage of every last bit of it. Complexity goes up. This is why stepping up our abstraction allows us to manage that complexity. Preprocessing makes working on websites easier and less complicated. The best example is {COMPANY}'s main website that is developed by multiple teams. It's heavy loaded with different styles and standarts, at this point complexity jumps up. CSS preprocessors are here to manage all the complexity and get us better performance and coding experience.

There are two main players out there: `LESS and SASS`. Both have their pros and cons. So, why not SASS? SASS is great. It ships with rails and has lots of cool power functionality. That said it's better to take LESS over SASS because:

- **Styles compile 6x faster with LESS than with SASS**. There are a lot of benchmarks online you can find to prove this thing. One of the biggest LESS supporter is Twitter Bootstrap team, they measured the time it took to compile Bootstrap written in LESS vs Bootstrap written in SAAS. LESS version compiled in under 90 ms while the SASS version compiled around 540 ms.
- **LESS is implemented in JavaScript**. In {COMPANY} we write JavaScript everyday, not Ruby. This also makes it really easy to dive into LESS source and patch something or help to push a feature forward by doing the development work here in {COMPANY} and sending a pull request.
- **LESS is simple**. Writing LESS feels like authoring CSS. Declarative nature of LESS and how much thought has been put into it simple impresses. If you are a CSS ninja then it's a 5-10 minutes process to understand and probably only one hour to be a master. This is a huge advantage of LESS.

###Key features of LESS:

- **Variables**. Managing colors and pixel values in CSS can be a bit of a pain, usually full of copy and paste. Not with LESS. Assign colors or pixel values as variables and change them once in one place.
- **Mixins**. Those three border-radius declarations you need to make in regular old CSS? Now they are down to one line with the help of mixins, snippets of code you can reuse anywhere. Do you want to have a consistent style? Define your mixin and use it everywhere.
- **Operations**. Make your grid, leading and more super flexible by doing the math on the fly with operations. Multiply, divide, add, and subtract your way to CSS sanity.
- **Nested rules**. You can simply nest selectors inside other selectors. These can save you a lot of coding, and they make your code clearer.
- **Namespaces for grouping variables and mixins**. This is very useful if you want to avoid naming clashes. This is one of the most useful features to use while collaborating with several teams on a single project.

###Shift to LESS

So, how do you **transition to LESS**? It's actually really simple. First thing is `all .css files are valid .less files`, although it's one way compatible syntax. If you have an existing project take your style.css and rename it to style.less this is a good step one.

Inch your way through the features:

- Good thing to try is to replace all the #color with @colors. The good benefit is consistency and once you're going through this stuff you may find little mistakes you haven't noticed before.
- Nest a few highly-related selectors. Don't get too deep and crazy with it just try it out.
- Convert CSS3 stuff to mixins.

The syntax will take you an hour to learn. It takes like a minute to learn LESS syntax for people who know JavaScript. There are not much stuff in it to learn. It's not that crazy new syntax it's just a little bit of syntax flavor. It will take you literally an hour to learn LESS.

###Objections and concerns:

- **It complicates my work-flow**. Granted, now you have some way to compile your LESS to CSS. In the same time you have to set up it once and then your day to day work-flow should get a little bit better. Much better once you figure out what you can do with it. Live reload, full stack development directly inside of Web Inspector, style combining and compressing, and etc. With a little dev effort, writing in LESS can be easier than writing CSS.
- **This is a one-way street**. LESS can output fully "expanded" CSS that is highly readable and maintains comments. If one day you decided to kill it just export all the LESS files into individual CSS files and you're fine.
- **LESS output is bloated**. LESS output is exactly what you tell it to be. It's easy to envision output as you author. Take CoffeeScript for example and there is much harder to envision your output, LESS is much simpler. Just write your LESS how you want your output and you will be good.
- **LESS is only for really big sites**. Just because a site is "small", do that mean you don't have to care about performance? Does that mean it's OK to be inconsistent? Does that mean it's OK to make mistakes? Does that mean the authoring experience should be less comfortable?
- **I have to learn a whole new syntax**. That's going to take you like one hour.
- **It's harder to debug**. First thing is your LESS file structure is more organized than your CSS one. You get better vision of your styles. In a browser you have all your LESS styles compiled into one big CSS file. With new things like source maps you can turn on line-number support in Firebug and Web Inspector. It will tell you not only the exact line in original LESS but also what mixin or variable it came from. And lots of new things coming because of it's popularity.

## Author

**Alexander Marinenko**

+ [http://twitter.com/jo_asakura](http://twitter.com/jo_asakura)
+ [http://github.com/jo-asakura](http://github.com/jo-asakura)

## Copyright and license

[MIT](LICENSE.md)
