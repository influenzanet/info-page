---
title: Automated Testing
date: 2019-05-21T18:29:54+01:00
draft: false
tags:
- technical documentation
- testing
- software development
---
**Testing software**

When it comes to delivering a product to customers, every company would make sure that the outcome meets certain quality criteria *before* handing it over. This is because as human beings  we are prone to make mistakes, and no matter how hard we try to keep every aspect and little detail in mind, we might still end up missing a key point or make a small mistake that is going to cost us a lot in later phases.
Same logic is relevant with software applications: we continuously run investigations to make sure the designed system satisfies user requirements and responds to all sorts of input correctly.

We prefer to run tests as early as possible, because both studies and experience have shown that a few tiny mistakes in early stages, if not dealt with in time, can cost us quite a lot: on the one hand, the later an error is found, the more areas it has affected. On the other hand, finding the cause of a failure is never an easy task, as it requires travelling back in time.

**Motivation for automated testing**

There are different approaches and variant techniques for testing software applications. Some are rather basic; for example when a developer adds a module to the system with the goal of fulfilling a certain requirement, he or she will definitely run the application once again to see if the module works as it should. A more advanced approach would require a team member to obtain the role of the “tester”, meaning he or she starts interacting with the system the way a normal user would. The tester tries to achieve specific goals, and keeps track of scenarios that were unsuccessful or lacked certain quality aspects. This approach is widely used, especially when it comes to evaluating the user experience, but it has its flaws: for one thing, we are relying on recollection and perception of our tester, who might forget to check a particular path or have some wrong assumptions about the requirements. And even with the most thorough, dedicated testers, the cost of manual quality assurance increases steadily as the codebase grows and more features are added to the system.

**Explanation of automated testing**

Here is where automation comes to the rescue: we make use of a seperate software to test our software. By describing the behaviour we expect from our system in a formal way, we get a chance to automatically check whether the actual outcome is the same as the expected outcome. We can define many test cases, each evaluating a single unit of our system or judging whether a sub-goal has been reached, and by running these individual tests, we evaluate our system as a whole.
This approach offers the possibility of reuse: every time a new feature is implemented, or a new module is added to the system, all the previous tests are re-run. This tactic takes care of possible regression of the system, and makes sure no new piece of code is breaking anything that used to be working correctly.


In some cases it is beneficial to write tests first, and then write code- correct and comprehensive code that complies with the defined test cases. In contradiction to the classic approach of “first coding and then testing” (which sometimes results in untested code specially near release dates!), the Test-Driven-Development makes sure no requirement is forgotten: it might not be implemented yet, but it will be eventually.

**How we make use of this approach in InfluenzaNet**

What was described so far applies for both backend and frontend of a software system, but the main goal of this article is to explain the techniques we are using to assess the frontend in InfluenzaNet project: do the web-pages look the way they should? How do users feel when interacting with the website? And of course, how we can find the answers to those questions in a fast and reliable way.
We started with creating the sign-up module, having the long-term goal of attracting more people to be part of InfluenzaNet. First, we discussed the behaviour we would expect from this module: what it *should* do, and the things that *could* go wrong. You can see a list of behaviors below:

<img src="/images/blog/2019-05-21/automated_test_figure.png" alt="Figure about automated testing." width="100%">

Next step was to actually write tests. In the examples below, you can see how we checked whether a certain word is included in our page (in this case, “Email” in the first example), and how we would check whether the system would reject an invalid email address (second example), and accept a valid one (third example).

**Example 1:**

```js
it(`should have as text 'Email'`, async(() => {
    expect(comp.text).toEqual('Email');
}));
```

**Example 2:**

```js
it(`should not accept invalid email`, async(() => {
    comp.signUpForm.controls['email'].setValue('www.john-doe.come');
    expect(comp.signUpForm.valid).toBeFalsy();
}));
```

**Example 3:**

```js
it(`should accept valid email`, async(() => {
    comp.signUpForm.controls['email'].setValue('john@doe.com');
    expect(comp.signUpForm.valid).toBeTruthy();
}));
```

**Our story: challenges**
As the system and its provided features grow, so does the number of tests: every new module brings along its related tests, and over time we come up with new ideas on further assessment of old modules. This is the beauty of automated testing; we get more confident about our system as more and more tests are passing, and the cost of running those tests does not increase significantly.

So, what could go wrong?

Seeing certain tests failing is a natural part of the process. But when a test keeps failing despite all the effort the developer puts into fixing it, it can be annoying. One solution for the described situation is to try to understand the test better, and picture what goal the author had originally in mind when writing this test. If that didn’t help, the now frustrated developer should sit down with the author of the test, and together they could find a solution.

Unfortunately, this is not always possible, as the original author might not be present at that time. In such cases, one bad approach would be to simply remove the tests that are not passing (“after all, we don’t know what was meant to happen here!”). However, there are practices to follow to avoid such situations. One of the strategies, we have learned to employ is to emphasize the importance of documenting the tests we write: even if the author of a test is present, the test should be self-explanatory. We are looking for other tactics as well, and we are positive that as the challenges we face grow, so does our level of expertise.

*Ala Harirchi*

