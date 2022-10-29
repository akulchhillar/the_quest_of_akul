# How I built this blog (Tech Stack)

When I initially thought of building this blog, my first impression was to use something like `Notion` as I use it for my most of my knowledge collection.

However since my Diwali leaves were approaching and I had around 9 days of leaves, the programmer itch in me started bugging me. And then I decided that I will build this blog from scratch instead of using a blogging platform.

My first decision was to figure out what framework should I use as I knew Vue and Flask at the time of building the blog. But since I was more comfortable with Flask and had built other projects with it in the past, I went ahead with it (Sorry Vue 🙏)

The next thing was to figure out how the blog would look as I wanted my blog to look a little different from the popularly used CSS frameworks such as `Bootstrap` or `Tailwind`. For this, I already had a [CSS library](https://www.getpapercss.com/) in my mind.

Moving ahead, I wanted to decide what features would I like to have in my blog as I would be building the entire platform from scratch. A few of the questions that I needed to answer before I could move forward were:

- How would I store that content
- Do I need an editor for writing the blogs
- Where would I deploy the blog

And a few others as well.

Since I am not a professional blogger, I knew I would require a minimal setup that a developer like me [^1] would require.
For this reason, I went ahead with using markdown files for writing the content and the idea was to host them in the `Github` repository of this blog. Additionally, all the assets belonging to the blogs would also be hosted there.

And since we are dealing with markdown files here, I thought it will be better not to have an editor on this blog rather I will be using the good old `VS Code` to write the blogs and then upload them on the repo. (A lot of hard work here 😩)

Once all these grounding questions were answered, it was time to code.

But before that, let me put some [music](https://www.youtube.com/watch?v=x5faT66jmG4) for motivation 😉.

Since we are dealing with `Flask` here, the first step was to create a bunch of routes that will be accessible on my blog.

For this purpose I built the following routes:

- Index Route (/)
- Posts Route (/posts/)
- A particular blog post (/post/)
- About Me (/about)
- 404 Page

Additionally, I also created 2 functions that would help me deal with the API calls for retrieving the data from the repo of the blog and dealing with markdown files as I would be required to convert the markdown to HTML to render it.

On a high level that is what the backend looks like.

Talking about the front end, since I have mostly worked on backend-related projects I did not have enough experience with it thus I wanted minimal interaction with the front end.

The idea was to create a minimal UI of the blog and for that, I had been looking for a few CSS libraries but then suddenly one of my previously saved links came to use.

Once the CSS library was decided, it was piece of cake to design the UI. I had several different layouts in my mind for the blog inspired by various pre-existing sites such as `Medium`. 

Here are 2 of the layouts that I had thought of initially.

![Layout](https://raw.githubusercontent.com/akulchhillar/the_quest_of_akul/main/assests/Layout.png)

![Layout 2](https://raw.githubusercontent.com/akulchhillar/the_quest_of_akul/main/assests/Layout%202.png)


But since I was creating everything from scratch, I decided to use my own layout (which again was heavily inspired by various sites where I read 😛).

In the end, I went for a minimalistic layout look to save the reader from clutter and let him/her focus on only the essentials.

Once the front end and the back end were done, then I went ahead with the following 3rd party plugins.

- Disqus for comments on the blog
- Mailerlite for managing the emailing list

Once everything was running on my local machine, it was time to deploy it on the cloud.
In the past, I have had experience deploying applications on `Heroku` and `Repl` but since I was using my work laptop to deploy the blog, I could not download Heroku CLI and thus I went ahead with `Repl`. 

Post deploying, I made sure that my blog was always "live" as I use the free version of `Repl` which puts the application to sleep if there is not enough activity. For this, I use `Uptime Robot` which keeps pinging my application every 5 minutes, making sure that my application never sleeps.

The last step here was to then connect the subdomain of the website to the application hosted on `Repl`. For that, it was a mapping of the DNS. However, this step had the hardest part in it i.e. waiting for the DNS to get mapped.

And voila! With that my blog went live.

The whole point of writing this blog was to document my entire experience. Maybe someone might be reading this in the future and may get some help from this.

---

[^1]: A self taught programmer who does not have any CS degree and has a academic background in commerce/business.







