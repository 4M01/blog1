---
title: "Performance Testing : Few Takeaways"
date: 2020-04-05
tags: [""learning","performance testing"]
draft: false
author: "Amol Chavan"
---

# Performance Testing : Few Takeaways

You have been working on functional testing of software for while,  you may be proficient in taking help of tools and libraries like UFT and Selenium to ease your repeatable work but have you given any thought about non-functional testing? (like performance testing) Do you know how it is different from functional testing?

In this post, you will get insights into learnings that I had while working on Performance Testing of software.  This post will help you to understand some of the few skills required for performance testing. It will also give some insights about how to get most out of the JMeter ecosystem. Let me be explicit - I don't claim to be expert in the field, I just completed more than a year working in performance testing for my current employer. Prior to this engagement, when I was working at my last employer I got introduced to Performance Testing and JMeter  and I learned basics concepts in 5 months along with my daily job.

Without delay, I will start with the list of things I learned.

1. In Functional Testing, output generally treated as PASSED or FAILED for particular experiment/test (By the way, writing test cases is not testing) but that is not the case with the Performance testing. Performance Tests are performed/executed from the objective to get information about AUT which can be used to device future strategy about the work needs to be done.  Results cannot be always treated as PASSED or FAILED.
2. More often, it can happen that Page load time up-to 5 to 10 seconds is acceptable in Enterprise software where as, for End user facing applications it is big No-No.
3. Great companies and great people treat [performance as feature](https://blog.codinghorror.com/performance-is-a-feature/) of the application.
4. More importantly, entry level folks treat Knowledge of tool that they use to create a load profile as performance testing. Only knowledge of JMeter or Load Runner does not make you performance tester, It's essential to know the tools because it is very hard to created required load manually without help of tools but there are lot of other things which are equally important to be performance tester. [Similarly, knowledge of Selenium, does not makes you tester or test-automation engineer]
5. Result Analysis and Resource monitoring using APM tools is as important as creating Load profile which supposed to represent the real users.
6. Finding patterns in Response time and Resource utilization is very important skill which can distinguish good performance tester with average performance tester. In a sense, stronger analytical skills and curiosity is a treat required for this profile.
7. Performance testing is not Performance engineering.
8. Having Knowledge of architectural component helps to identify the root cause, component like Load balancer and its algorithm, Caching Mechanism, Service discovery mechanisms, proxies and reverse proxies are like essential for most of the software we use. It's important to understand why and when this components gets used.
9. Client Side Testing is underrated in the industry. Of course,  there are pioneers who has adopted it and promoting it for while.  But there is no traction as it deserves.
Link for [Google Trend](https://trends.google.com/trends/explore?q=Performance%20Testing,JMeter,Client%20Side%20Performance,Lighthouse%20Chrome,YSlow) :

    ![Trends for term - Performance Testing, JMeter, Client Side Performance, Lighthouse Chrome, YSlow](/Performance-Testing-Few-Takeaways/Trend-For-Term-Performance-Testing-JMeter-Client Side Performance-Lighthouse-Chrome-YSlow.png)_Last Year Trend Performance Testing, JMeter, Client Side Performance, Lighthouse Chrome, YSlow_

1.  [YSlow](http://yslow.org/), extension that was developed around 8 years ago,which is also [no more maintained](https://github.com/marcelduran/yslow), is something still being used and searched for client side performance testing.
2.    Yahoo! posted - [Best Practices for Speeding Up Your Web Site](https://developer.yahoo.com/performance/rules.html) long back, it's still good as it was produced yesterday.
3.  Comparison of the latest Performance tests results with baseline and previous result is going to take huge amount of time,  at least in JMeter ecosystem. [Influx DB](https://www.influxdata.com/) and [Grafana](https://grafana.com/) together can be very helpful for collecting the results at runtime and doing the comparison.
4.  In-Build JMeter functions and properties only can be used with [Backend Listener](https://jmeter.apache.org/usermanual/realtime-results.html) , there is no way of storing additional dynamic value in Influx DB.  If you really want to store in something in the Influx DB, think about using [JSR 223 Listener](https://jmeter.apache.org/usermanual/component_reference.html#JSR223_Listener) as Influx DB support writing to [DB](https://docs.influxdata.com/influxdb/v1.7/tools/api/#write-http-endpoint) over HTTP .
5.  Debugging code in JMeter is not at all user friendly. You will feel this very strongly specailly if you come from the background of using sophisticated IDE like IntelliJ. Uou cannot help but curse the user experience of using JMeter.
6.  Groovy is wonderful not only from the Performance aspect as compare to [Beanshell Scripting](https://beanshell.github.io/) but to ease of use. You can use online console for [Beanshell](https://tio.run/#beanshell)  and [Groovy](https://groovyconsole.appspot.com/) because it's lot faster to check your code working or not instead of using in JMeter directly. I personally prefer local instance of Groovy console. You can download it [here](http://groovy-lang.org/download.html)