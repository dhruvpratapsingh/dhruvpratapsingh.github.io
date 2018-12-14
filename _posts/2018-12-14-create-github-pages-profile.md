---
title:  "0001: Start Creating Your Data Scientist Profile Using Github Pages"
---
![GitHub Pages](https://source.unsplash.com/hRZDd1ekhrA/1200x600)

# Summary:

1. Register a domain name.
2. Register for a Github account and configure Github pages.
3. Choose a Jekyll Theme and Setup your environment.
4. Setup Github Pages.
5. Add your Custom domain to Github Pages.

## 1. Register a your domain name. (Optional)

Personally, I am a fan of namecheap.com and they also offer FREE domain registrations for students. Check out https://nc.me/ to register your own domain name. If you are not a student you can still register for one with a small charge. You can also look at godaddy.com, 1&1.com etc...

Once you have a domain name registered jump on to the next section.


## 2. Register for a Github account.

Navigate to https://github.com/ and signup if you already don't have an account. Once you are logged in, click "+" icon on the upper right corner and select "New Repository" option from the dropdown. Repository name should be "username.github.io" , username is your Github username. Proceed by clicking on "Create repository" button.

## 3. Setup Jekyll environment and deploy it to Github Pages.
Follow the step below.
https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/

{% highlight c %}

static void asyncEnabled(Dict* args, void* vAdmin, String* txid, struct Allocator* requestAlloc)
{
    struct Admin* admin = Identity_check((struct Admin*) vAdmin);
    int64_t enabled = admin->asyncEnabled;
    Dict d = Dict_CONST(String_CONST("asyncEnabled"), Int_OBJ(enabled), NULL);
    Admin_sendMessage(&d, txid, admin);
}

{% endhighlight %}

#### **Bonus Resources**:
* [Free Jekyll Themes](https://jekyllthemes.io/free)
* [Git and Github learning resources](https://help.github.com/articles/git-and-github-learning-resources/)
* [Jekyll Tutorials](https://www.youtube.com/watch?v=T1itpPvFWHI&list=PLLAZ4kZ9dFpOPV5C5Ay0pHaa0RJFhcmcB)
