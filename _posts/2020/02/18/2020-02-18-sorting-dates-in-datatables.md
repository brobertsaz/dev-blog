---
layout: post
title: Sorting dates in datatables for Rails
date: "2020-02-18"
categories: ["rails","javascript"]
tags: ["rails"]
banner_image: /images/posts/data.jpg
permalink: /2020/02/18/sorting-dated-in-datatables
description: How I added sorting to jQuery datatables in Rails
---

I recently added jQuery Datatables to a Rails application. I have used datatables before with Rails but I have never run into the issue that I had the other day.

If you have never used datatables in Rails, [here](https://www.driftingruby.com/episodes/datatables) is a great tutorial to setting it all up.

I had a date field in my table that I had formatted prior to adding in datables. Once I had datatables working, I noticed that the date field was not sorting correctly.

I was using strftime to format the date in my table (shown in HAML):

```
%td= bill.introduced_on.strftime('%B %d %Y')
```

When I clicked on the column header for the date field, it was sorting the dates alphabetically and not as a date.

Thankfully, there is a quick fix for this.

```
td{"data-sort" => "#{bill.introduced_on}"}
  = bill.introduced_on.strftime('%B %d %Y')
```

Now the column sorts as a DATE but renders in the format that I want it in.
