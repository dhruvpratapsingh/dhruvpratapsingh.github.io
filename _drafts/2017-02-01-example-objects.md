---
title:  "Example Objects"
date:   2017-02-01 22:30:00
categories: objects
---

Lorem **ipsum dolor** sit amet, consectetur adipiscing elit, `sed do eiusmod tempor` incididunt ut *labore* et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud ***exercitation*** ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute *irure dolor* in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.

The term was coined in 1964 by two [Australian](https://en.wikipedia.org/wiki/Australia) [CSIRO](https://en.wikipedia.org/wiki/CSIRO) researchers, Isabel Joy Bear and Richard G. Thomas, for an article in the journal [Nature](https://en.wikipedia.org/wiki/Nature_(journal)). In the article, the authors describe how the smell derives from an oil exuded by certain [plants](https://en.wikipedia.org/wiki/Plants) during dry periods, whereupon it is [absorbed](https://en.wikipedia.org/wiki/Absorption_(chemistry)) by [clay](https://en.wikipedia.org/wiki/Clay)-based [soils](https://en.wikipedia.org/wiki/Soil) and [rocks](https://en.wikipedia.org/wiki/Rock_(geology)).


Some scientists believe that humans appreciate the rain scent because ancestors may have relied on rainy weather for survival.

### Lists

#### Unordered

 * lorem
 * ipsum
 * dolor
 * sit amet

#### Ordered

1. lorem
2. ipsum
3. dolor
4. sit amet

### Code

{% highlight c %}

static void asyncEnabled(Dict* args, void* vAdmin, String* txid, struct Allocator* requestAlloc)
{
    struct Admin* admin = Identity_check((struct Admin*) vAdmin);
    int64_t enabled = admin->asyncEnabled;
    Dict d = Dict_CONST(String_CONST("asyncEnabled"), Int_OBJ(enabled), NULL);
    Admin_sendMessage(&d, txid, admin);
}

{% endhighlight %}


### Quote

> Pagination is the process of dividing a document into discrete pages, either electronic pages or printed pages.
>
> In reference to books produced without a computer, pagination can mean the consecutive page numbering to indicate the proper order of the pages, which was rarely found in documents pre-dating 1500, and only became common practice c. 1550, when it replaced foliation, which numbered only the front sides of folios.
>
> \- [Wikipedia](https://en.wikipedia.org/wiki/Pagination)

### Table

| First Header | Second Header | Third Header   | Fourth Header |
|--------------|---------------|----------------|---------------|
| First Entry  | Second Entry  | Third Entry    | Fourth Entry  |
| Fifth Entry  | Sixth Entry   | Seventh Entry  | Eight Entry   |
| Ninth Entry  | Tenth Entry   | Eleventh Entry | Twelfth Entry |

### Image

![subtle swirly bokeh in the background](https://upload.wikimedia.org/wikipedia/commons/thumb/3/32/Photography_by_Victor_Albert_Grigas_%281919-2017%29_000172050002_%2837159721864%29.jpg/1039px-Photography_by_Victor_Albert_Grigas_%281919-2017%29_000172050002_%2837159721864%29.jpg)

