# Bio and Abstracts
Abstracts and bios and such. No presentations - those have their own repos.

Note to self: 2017 marks 20 years professional exp.

# Bio - general purpose
Seth has been programming for 27 years, 20 of them professionally. He is a full-stack developer/architect and enjoys bouncing between the database, .NET and JavaScript. He is passionate about bringing order to chaos through clean architecture, simple designs and testable code. Seth lives in Columbus, OH and is an active participant in the Midwest developer community.

# Bio - for testing talks
Seth has been programming for 27 years, 20 of them professionally.  He got "test infected" in 2004 and has been practicing TDD ever since. He is passionate about bringing order to chaos through clean architectures, expressive patterns and testable code. Seth lives in Columbus and is an active participant in the Midwest developer community.

# Bio - for management/leadership talks
Seth has been programming for 27 years, 20 of them professionally as a full-stack developer and architect. He currently leads a small but powerful team in search of elegant, maintainable solutions to hard problems. When not juggling Gantt charts and TPS Reports, Seth can be found playing tabletop games or sneaking in a quick code change to keep his skills sharp. He loves working from home outside of Columbus, OH.

# Patterns of Effective Test Setup
Writing clean, effective and manageable tests begins with the "fixture", the set of data used in the test. If you've ever struggled with the "arrange" part of a test, or if you've ever looked at someone else's "arrange" and struggled to understand the context it establishes, then you've suffered the pains of poor fixture setup.

In this session you'll learn a collection of patterns and techniques that will help you write smaller, more expressive tests that are easier to read, understand and maintain. We'll talk about patterns for constructing test data for unit tests, patterns for saving that data in the database for integration tests, and some common anti-patterns that you may not realize you're following. Code samples will be in C# and NUnit but the core concepts will be presented in a language-agnostic way.

"Clean setup begets clean tests". Let me show you how.

> REVIEWER NOTES:
> I've delivered this talk at CodeMash (twice), CodePalousa, and to CONDG. Both CodeMash sessions were very well attended and I've received a lot of feedback that the material is well organized and helpful.
> 
> I'd call this an intermediate session. I assume the audience has some basic experience writing tests, and then I walk them through a collection of patterns that I've used on a large, ongoing project to manage increasing testing costs caused by an explosion in app complexity.


# Stop Writing Secure Code! (Start Building Secure Frameworks)
The best way to build secure systems is to stop writing security-related code on a daily basis.

Developers have their hands full with complex business rules, technical edge cases, responsive UIs, etc. Security requirements are repetitive to implement, hard to test, and often get crowded out by other demands. When developers handle security on a feature-by-feature basis the result is a wildly inconsistent mess of security holes.

In this session developers and architects will learn real-world techniques for designing security into the application framework itself, rather than leaving it up to individual features. You’ll see how to implement access control in your data access layer, declaratively handle permission checks with Attributes, use PostSharp to create new "hooks" to tap into, and automate security audits using Reflection. Come learn how secure software design can dramatically reduce the day-to-day burden of secure coding.

Code samples will be in C# and ASP.NET MVC but many techniques have parallels in other platforms.

> REVIEWER NOTES:
> This was new for CodeMash 2017. I cover a number of different techniques for extracting various types of security concerns (CSRF, authentication, authorization, access control, etc) from feature-level code and handling them at a lower level.
> 
> Multiple people told me after the session that it was very helpful and contained innovative ways of solving problems they'd been wrestling with.
> 
> Based on the "real world" timings at CodeMash, I can add another 5-7 minutes of content and still have time for questions, so I'll probably elaborate and flesh out the section on row-level security in SQL Server. I'm also considering adding a little more JS content so that it isn't quite so MVC focused.


# Securing Your API Endpoints - A Practical Guide to API Authentication
It's never been easier to expose services over HTTP. It's also never been harder to choose an authentication system for those services. This session is designed for the average developer/architect that wants a brief overview of API security techniques without deep dives into cryptography or complex authentication frameworks. You'll learn about OAuth, API Keys, HMAC authentication, and more. Don't worry if those things sound foreign; they'll be explained in a clear, practical way and you'll leave able to make informed decisions when choosing an authentication strategy for your own apps.

> REVIEWER NOTES:
> This has been presented at CodeMash, StirTrek, and DogFoodCon, to very full rooms in all cases. I've received a lot of positive feedback and it seems like this addresses a knowledge gap for a ton of developers.
> 
> Basically, this session gives people a working knowledge of different authentication techniques, from Basic Auth to bearer tokens to OAuth, so that they can make an appropriate choice for their own project. I don't show how to implement anything, just a roadmap to the overall landscape so that people can make informed choices.
> 
> I'd call this a beginner to intermediate session. I do talk about some complex stuff (like OAuth), but the intent is to simplify and clarify to make it approachable. In my experience, this information is useful and relevant to both junior coders and those with long experience.


# Automated Visual Regression Testing: A Picture's Worth A Thousand Tests
Regression testing via the browser is expensive, but until someone implements "assert.stillLooksPretty()" it's the only way to *truly* verify that your app looks and behaves well across multiple configurations, browsers, and device breakpoints.

This session is a case study in one team's use of automation to solve this problem. You'll learn how to take screenshots during your UI tests, how to detect when the images change, and how to integrate human intelligence into the re-approval process. The presented solution uses Canopy and ApprovalTests, but multiple tools will be discussed at each step along the way so that you can choose the combination that best suits your stack or platform.

Breaking CSS is easy, testing it is hard - unless you're smart about it. Come learn how.

> REVIEWER NOTES:
> This session will show off a project my team has been working on to automate the collection of screenshots via Canopy tests and then to automatically examine them for visual regressions.
> 
> I intend to create a stand-alone demo app to show the techniques we've used, and I also intend to identify other libraries/tools that could be swapped in (for instance, using Capybara on Ruby rather than Canopy on F#).


# Taking Your App's Temperature - Building A Diagnostic Engine in C#
Do you know how "healthy" your application is, right now, in production? A diagnostic engine can provide realtime, environment-specific feedback about things that are impossible to unit test. It can tell you if your app has read/write access to configurable file paths, if the 3rd party services you depend on are up and responding to your requests, if any of your app config settings are invalid or configured in contradictory ways, and so much more.

This session is a code-centric walkthrough of an open-source diagnostic engine that you can integrate into your own app. You'll see how diagnostic rules are managed in an extensible way, how to automate diagnostic reports, and how to automatically re-run the diagnostics after specific events happen in your system.

Come see how to write integration tests for your PROD environment, and stop being caught by surprise when things fail at runtime.

> REVIEWER NOTES:
> I manage an extremely configurable SAAS product and we depend heavily on an in-app diagnostic engine that helps us identify issues that would cause runtime failures *before* a user hits the code that blows up. We've augmented this system with features over time and it's turned into a nice, extensible, extremely useful system.
> 
> For this session I intend to extract those pieces into an OSS library or product, add some additional features, and then walk the audience through how it all works.
> 
> The goal isn't to pimp my specific product, but to show people how to create an extensible rules engine, how to easily deploy those rules, how to automatically run them when the configuration changes, etc. At the end, I want people to be knowledgeable enough to incorporate these concepts into their own app OR able to download my OSS product and integrate.