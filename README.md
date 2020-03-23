# Postmortem Templates

This is a collection of postmortem templates derived from various sources such as the [Site Reliability Engineering](https://landing.google.com/sre/) book, [The Practice of Cloud System Administration](http://the-cloud-book.com/) book and other online resources.

## Template List
* [Template from Site Reliability Engineering book](templates/postmortem-template-srebook.md)
* [Template from The Practice of Cloud System Administration book](templates/postmortem-template-thecloudbook.md)
* [Template from Google Developers Blog post](templates/postmortem-template-google-api-infra.md)
* [Template from Azure status history posts](templates/postmortem-template-azure.md)
* [Template from Michael Kehoe's blog post](templates/postmortem-template-michael.kehoe.md)
* [Template from the Real-World SRE book](templates/postmortem-template-real-world-sre.md)
* [Template from Elastic Cloud incident report](templates/postmortem-template-elastic.md)

## Load templates automatically

It is possible to load the postmortem templates automatically without copy pasting from the files or manually writing the structure every time you want to author an incident report.

### Vim
You can add the following line into your `.vimrc` file:

    au BufNewFile postmortem-*.md 0r ~/postmortem-templates/templates/postmortem-template-srebook.md

### Emacs
You can add the following line into your `.emacs` file:

    (add-hook 'text-mode-hook (lambda () (when (and (string-prefix-p "postmortem-" (buffer-name)) (= (point-max) (point-min))) (insert-file-contents "~/postmortem-templates/templates/postmortem-template-srebook.md"))))


In both cases the filename pattern is `postmortem-*`. For example, if you create a file named `postmortem-api-outage-2017-05-29.md` it will load automatically the predefined template into that file. You can replace both the postmortem template and pattern to match your.

### Examples
* [Google Compute Engine Incident #16007](https://status.cloud.google.com/incident/compute/16007?post-mortem)
* [Azure status history](https://azure.microsoft.com/en-us/status/history/)
* [Buildbucket Postmortem: 6% builds lost on 2015-04-22](https://docs.google.com/document/d/1AyeS2du6wp_Pw8Grg8WovbE_A_HV4EUMqdiqeq1KUZ8/edit#)
* [Google API infrastructure outage incident report](https://developers.googleblog.com/2013/05/google-api-infrastructure-outage_3.html)
* [Gitlab - Postmortem of database outage of January 31](https://about.gitlab.com/2017/02/10/postmortem-of-database-outage-of-january-31/)
* [Summary of the Amazon DynamoDB Service Disruption and Related Impacts in the US-East Region](https://aws.amazon.com/message/5467D2/)
* [Elastic Cloud Incident Report: February 4, 2019](https://www.elastic.co/blog/elastic-cloud-incident-report-feburary-4-2019)

### Postmortem resources
* [Learn out of mistakes. Postmortems to the rescue.](https://fernandocejas.com/2020/03/21/learn-out-of-mistakes-postmortems/)
* [A collection of post-mortems](https://github.com/danluu/post-mortems)
* [Blameless PostMortems and a Just Culture](https://codeascraft.com/2012/05/22/blameless-postmortems/)
* [A Tale of Postmortems](https://blog.box.com/blog/a-tale-of-postmortems/)
* [Building a Blameless Post-Mortem Culture with Jason Hand](http://runasradio.com/Shows/Show/486)
* [The infinite hows](https://www.oreilly.com/ideas/the-infinite-hows)
* [Failure is Always An Option: How a Blameless Culture Leads to Better Results](https://victorops.com/blog/blameless-culture/)
* [How to write an Incident Report / Postmortem](https://sysadmincasts.com/episodes/20-how-to-write-an-incident-report-postmortem)
* [SysAdvent - Day 1 - Why You Need a Postmortem Process](https://sysadvent.blogspot.com/2016/12/day-1-why-you-need-postmortem-process.html)
* [Etsy’s Debriefing Facilitation Guide for Blameless Postmortems](https://codeascraft.com/2016/11/17/debriefing-facilitation-guide/)
* [Writing Your First Postmortem](https://medium.com/production-ready/writing-your-first-postmortem-8053c678b90f)
* [How to Write Great Outage Post-Mortems](https://artsy.github.io/blog/2014/11/19/how-to-write-great-outage-post-mortems/)
* [Postmortem Action Items: Plan the Work and Work the Plan](https://www.usenix.org/conference/srecon17americas/program/presentation/lueder)
* [Site Reliability Engineering resources](https://github.com/dastergon/awesome-sre)
* [Postmortem culture: how you can learn from failure](https://rework.withgoogle.com/blog/postmortem-culture-how-you-can-learn-from-failure/)
* [Postmortem Culture: Learning from Failure](https://landing.google.com/sre/book/chapters/postmortem-culture.html)
* [re:Work- Postmortem discussion template](https://docs.google.com/document/d/1ob0dfG_gefr_gQ8kbKr0kS4XpaKbc0oVAk4Te9tbDqM/edit)
* [Wheel of Misfortune Game](https://dastergon.gr/wheel-of-misfortune/)
* [Post-Incident Review Template by VictorOps](https://victorops.com/blog/the-post-incident-review-template-you-ve-always-needed)
* [Atlassian Incident Handbook: Incident Postmortems](https://www.atlassian.com/software/jira/ops/handbook/incident-postmortems)
* [Collection of Kubernetes Failure Stories](https://github.com/hjacobs/kubernetes-failure-stories)
* [Best engineering practices: how to fix a bug?](https://sobolevn.me/2019/01/how-to-fix-a-bug)
