# Outline of Joe's Slides

This is an outline of notes for Joe's slides:

* slide: Who are we?
    * I'm Joe Purcell, I've been part of the web development community since 2003 and am currently an Engineer at Palantir.
    * I'm inspired by the discoveries being made from cross-disciplinary research and I enjoy adventure.
* slide: photo of smog
    * "smog" was coined in London, not LA
    * By the 1800's, London was the largest city in the world ([source](https://en.wikipedia.org/wiki/List_of_largest_cities_throughout_history)).
    * By 1950 there were over 8 million people living there ([source](http://www.londonspovertyprofile.org.uk/indicators/topics/londons-geography-population/londons-population-over-time/)).
    * It was the most technologically advanced and most wealthy city on the planet.
    * But, there was a problem: the primary source of energy was coal, which when burned combined with fog from the Themes river to make a thick yellowish green smog.
    * "Thick as pea soup", they would say, both because of density and color.
    * This smog would cause people to cough, some people would get ill, visibility was significantly reduced causing traffic to stop or even wrecks.
    * Because there was no easy accessible alternative energy, they would just cope with it using masks, traffic flares, cancelling events if the smog was too thick (even indoor events), and they would use detonators on train tracks to notify conductors of the approaching station.
    * Even animals were adapting: before 1800 there were no dark colored Peppered Moths. By 1900, the dark colored moths completely outnumbered light colored ones ([source](https://en.wikipedia.org/wiki/Peppered_moth_evolution)).
    * Efforts were made to control the level of air pollution. Most legislation didn't pass for the sake of the economy. Legislation that did pass either had no teeth to enforce it or people got around with loopholes. For example, one legislation said that "black smoke was a nuisance" to which companies argued their smoke was "dark brown" and therefore not a nuisance (["Environmental Chemistry in Society, Second Edition" by James M. Beard, pg 212](https://books.google.com/books?id=ehXSBQAAQBAJ&pg=PA212&lpg=PA212&dq=great+smog+legislation+dark+brown+smoke+vs+black+smoke&source=bl&ots=D2FBNRe6uQ&sig=LxucXqM0VqRJT04MLdl9vK5jtZc&hl=en&sa=X&ei=hgeKVaOpM87FogTakoCAAQ&ved=0CDcQ6AEwAw#v=onepage&q=great%20smog%20legislation%20dark%20brown%20smoke%20vs%20black%20smoke&f=false)).
    * The Industrial Revolution was being built on cheap energy, coal, so to be against coal or even regulating it was to be against progress.
* slide: Great Smog of '52
    * slide: initial
        * In December of 1952, there was a severe cold spell and a large amount of coal was being burned for heat. At the same time, there was an anticyclone event, meaning that the air was not circulating like normal, instead smog accumulated over the city.
        * Within weeks, over 4,000 people died. It is known as the "Great Smog" and is still today the worst air pollution tragedy in London's history.
        * But, it was also the most critical in building social awareness of the relationship between air pollution and health and in environmental reform; it inspired the environmental movement we know today.
        * The National Society for Clean Air (NSCA) says of this event, "It marks the dividing line between the general acceptance of air pollution as a natural consequence of industrial development, and the understanding that progress without pollution control is no progress at all."[Guardian](http://www.theguardian.com/uk_news/story/0,3604,850909,00.html)
        * In the aftermath, change wasn't immediate. Cover stories were made to minimize the impact by blaming deaths on an influenza epidemic.
        * Eventually, a committee was made to investigate the issue.
    * slide: what were the symptoms?
        * Illness was clearly being cause from the smog. Coughs and itchy throats turning into difficulty breathing from pnemonia and bronchitis.
        * Visibility was a major practical issue: traffic required road flares or even to be shut down.
    * slide: what were the causes?
        * They didn't have the technology we have today to analyze air pollution, so they just went after anything that makes smoke.
        * Today, we know that much of it was from burning dirty coal.
    * slide: What policies can mitigate the issue?
        * In 1956, the Clean Air Act was passed which did three things:
            * promoted the use clean coal, electricity, and gas to fuel homes
            * increased and regulated the height of chimneys
            * relocated power plants and factories away from cities
* slide: overview
    * slide: initial
        * So, how does this relate to technical debt?
        * In two ways: We believe that the monetary analogy communicates the wrong idea about hwo technical debt is measured and how it impacts business. We believe it is more similar to pollution.
        * As such, we are going to approach our talk in a similar manner to the Clean Air committee:
        * What is technical debt? What is the problem we are describing and how do we identify the symptoms of it.
        * What causes technical debt? Now that I know what it is, where does it come from?
        * Last, how do you deal with technical debt? Once you know the symptoms and causes of it, you need to know what policies are effective in mitigating it.
* slide: What is technical debt?
    * Now, what is technical debt?
    * Let's go back to the origin of the term.
    * Ward Cunningham was working at Wyatt Software developing a financial management system called WyCASH+.
    * Because their clients had changing needs which were highly important for them to quickly adapt to, they would release code based on their current understanding of their clients needs with the expectation they would change it later.
    * That is to say, they would make a prototype, release it, and then rewrite it later as their understanding evolved.
    * He wanted to communicate this idea to his boss, about the pros and cons of incremental growth, and decided to use a debt analogy which he eventually published in 1992 phrasing it this way:
* slide: shipping first time code
    * "Shipping first time code is like going into debt. A little debt speeds development so long as it is paid back promptly with a rewrite." ([source](http://c2.com/doc/oopsla92.html))
    * When a business is evaluating having software written, they want to know the return on investment (ROI) over time.
    * Sometimes it is more beneficial to release "not-quite-right" code.
        * Perhaps you want to shorten the time to market to get feedback in case you need to pivot.
        * Perhaps you want to preserve your startup capital and postpone rewrites until you have more cash flow.
        * Perhaps you simply want to delay the development expense to meet some other financial objective.
    * In any case, the idea is that you are delaying effort to meet some objective. This is good, and there are entire books written to explain how to compute the actual monetary benefit. (Note: further reading: [why take on debt, slide 11](https://resources.sei.cmu.edu/asset_files/Webinar/2012_018_101_24291.pdf) which discusses [Denne, M., Cleland-Huang, J. 2003. Software by Numbers, Prentice Hall](http://www.amazon.com/dp/0131407287/))
* slide: repayment
    * But, there is a danger here.
        * "The danger occurs when the debt is not repaid. Every minute spent on not-quite-right code counts as interest on that debt." ([source](http://c2.com/doc/oopsla92.html))
        * In finance, if you accumulate debt you also accumulate interest payments which takes away from your overall cash flow.
        * In a similar fashion, if you accumulate technical debt you also accumulate additional effort required to work around the "not-quite-right" code.
        * The danger is that projects can reach a critical point where paying effort on technical debt prevents being able to pay effort on new features or bug fixes.
        * You don't want to be in a situation where you discover a critical bug that requires a level of effort that pushes back a launch date or goes beyond what your SLA will allow.
        * If you take on debt, you have to repay it.
* slide: tech debt quadrant
    * There has been debate about what exactly is "not-quite-right code".
    * Cunningham Ward admitted that there has been some confusion that technical debt can be cruft, that is you can write code badly and fix it later and that's OK ([source](http://c2.com/cgi/wiki?WardExplainsDebtMetaphor)).
    * His opinion is that no, your code should always be clean enough to be able to refactor. There are those who back the stance that cruft is not debt.
    * However, let's be practical. Messy code acts the same as other forms of technical debt.
    * It doesn't matter whether its cruft or not, you still have code that isn't right that requires effort to fix. Cruft happens.
    * Martin Fowler takes this stance in his description of the four quadrants of technical debt.
    * What we've been talking about up until this point has been the right two quadrants.
    * When Cunningham and his team would decide to ship code that matched their current understanding of what the software should be with the expectation they would need to refactor, this was prudent and deliberate.
        * An example of this for them might be to abstract a class to meet a specific's client's needs with the intention to go back and consolidate that class into a concrete class.
        * Another example of this might be to delay adding caching to a future release: you are being prudent in that the software will still function and you are doing it deliberately knowing there will be future effort involved.
        * If you have ever cut a corner in a clean and deliberate way to meet a sprint deadline, that's what this is.
    * Implicit in what Cunningham and his team were doing was also the bottom right quadrant which is prudent and inadvertent debt.
        * They knew that client's needs would be changing. But, it was more valuable to have something than nothing, so they would release code even on a partial understanding until a clearer understanding was made.
        * It's prudent in that they are exercising good judgement, but it's inadvertent in that they do not know when and how their client's needs will change, but when they do they know they will need to refactor.
        * If you have ever been on a project where a requirement has changed and required you to rearchitect a portion of your code to properly support that change, that's what this is.
    * When Cunningham doesn't talk about and what is mostly debated are the left two quadrants.
    * The top left is reckless and deliberate debt.
        * When you have a deadline to meet and you skip following a design pattern or properly documenting your code, that's what this is. It's intentional cruft, if you will.
        * Or, perhaps you merge your own code without peer review and introduce a poorly implemented interface, that falls in this quadrant.
        * But, this can also be introduced from the business side: for example, the decision being made to short cut proper architecture without evaluating the impact.
        * In any case, you should never be deliberately reckless, but sometimes we do it especially when under pressure.
        * This is the worst kind of debt, because it can often be easily prevented by being prudent--by following sound software development practices.
    * The bottom left is reckless and inadvertent debt.
        * When you have junior developers or people who are not familiar with the framework being used or who lack the knowledge of the business requirements, they can unknowingly write incorrect code.
        * Cruft, in this case, can be unintentional.
        * An example of this might simply be not following coding standards.
        * Or, it could be putting a controller in the wrong directory, or incorrectly namespacing a class.
    * The main point here is that "what" technical debt is is not determined primarily by how it was introduced, but whether or not it can be described by the debt analogy.
    * Technical debt isn't inherently bad. It's about tradeoffs.
    * For those of you using agile, this is critical to understand: Agile actually encourages technical debt because of YAGNI--don't implement things until you actually need it.
    * We make decisions on a sprint-by-sprint basis to complete or defer effort.
* slide: productivity vs time
    * So, let's solidify this idea of technical debt with a chart.
    * In Robert Martin's book "Clean Code" he shows a diagram of what it's like to own a code mess over time.
    * While he is demonstrating productivity over time of a code mess, the same principle applies to technical debt.
    * As time increases, productivity declines because you need to spend time paying down debt rather than working on features.
    * And, don't be deceived: you cannot change the slope of this graph by adding more people.
    * In fact, it will make it worse.
        * New members need training from your existing team, which reduces your resource pool and therefore reduces your productivity.
        * Assuming you skip training, new members will not be able to distinguish between code that matches the correct direction versus that which doesn't, and unintentionally introduce more debt.
    * So, how do we frame in our minds what technical debt is on a project in relation to other kinds of effort?
* slide: what color is your backlog
    * Philippe Kruchten, a professor of software engineering, introduced the concept of describing effort using two planes: visible vs invisible and positive vs negative value.
    * On the top left, we have Feature which is visible and positive value. This is where all backlogs start. This is what businesses focus on because they can see it and it has positive value to their business.
    * However, as engineers we know that features require certain architecture, which is on the top right: this has positive value because it is required to support features, but to the user and to businesses, it is invisible. Sometimes this effort gets identified implicitly along with a feature, and sometimes its identified as a discrete chunk of effort.
    * Then we have Bugs on the bottom left. This is effort required to fix defects, which are visible, but it has negative overall value because it's time not spent on making progress on the software itself. These often make their way into a backlog or a ticketing system from some kind of testing.
    * Last, on the bottom right, we have technical debt. This is effort that both invisible and has negative value. Any work you spend here no one sees, no one knows, and often no one cares because time spent here does not add value to the software, it only corrects something that was wrong.
    * Typically, conversations tend towards the visible spectrum because where there is a gap in understanding you can at least take a screenshot or point at a screen and talk through what it is that needs to be different.
    * On the invisible side, it's often accepted by default that you need architecture, and as mentioned that effort often gets wrapped up into estimations on features.
    * But, this bottom right side, the invisible negative value effort, called technical debt is what we are focusing on today.
    * For project managers and business leaders, this is the area of effort that your project is telling you we need to spend time on, but because it's invisible and of negative value, you need to be certain you understand what the return is on this investment.
* slide: the monetary analogy communicates the wrong idea
    * By this point you should have an idea of what technical debt is. It's the gap of effort between where the code should be and where it is.
    * The problem with the monetary analogy is that it suggests you can think of money and technology in similar ways.
    * Is monetary debt measured by a single metric? Yes, typically USD.
    * Is technical debt measured by a single metric? No. In fact, we are still trying to figure out how exactly to quantify it.
    * Is it easy to measure monetary debt? Yes, we have tools readily available to not only tell us quantitative measures, but qualitative too, you have a credit score.
    * Is it easy to measure technical debt? No, it's extremely difficult. We don't have tools that can objectively tell you if a piece of code is "right".
    * Does monetary debt have a constant and expected impact? Yes, you should get reminders in the mail, email, phone calls to your friends and family reminding you of the exact amount you need to pay and when.
    * Does technical debt have a constant and expected impact? No, it's not constant--you may not touch one piece of code for a year and another every week. But, when the day comes for needing to modify that untouched stale code, you can't expect what the impact is going to be. This is why we've developed practices like continuous deployment.
    * Is monetary debt simple to understand? Yes, as long as you can understand basic arithmetic one can explain how compound interest works. You know the parties involved and you can quantify the entire transaction at any point with a single number.
    * Is technical debt simple to understand? No, that's why we are here today. "Not-quite-right" code is extremely hard to accurately identify let alone understand the relationship between it and other sections of code and business objectives.
* slide: the pollution analogy communicates the right idea
    * But, the pollution analogy does communicate the right idea.
    * Pollution is a contaminate that causes adverse change in a system.
    * Technical debt is code that causes adverse change in a system.
    * We believe the way in which we talk about pollution, how we measure it, and how we communicate the business impact is more similar than the monetary analogy and here's why:
    * Pollution is multi metric. Coal was over 90% of the energy source in London in 1950, and today it's only 30%. But, that doesn't mean air pollution has been eliminated. There are now millions of cars in London giving off pollutants.
    * Pollution is difficult to measure. When it comes to radiation there are at least four types of radiation that a Geiger counter can detect, but it depends on what the detector was designed to detect and whether it was calibrated recently. And, radiation is based on exposure over time per person, so you need dosimeters. Similarly, technical debt is difficult to measure--there is no single tool or metric to gauge it by.
    * Pollution has a variable and unexpected impact. London dealt with smog for decades before it demonstrated a tragic impact. For those of you who are coders how many times have you committed code or deployed something that you have nightmares about the day when that code will awaken and a bug will surface and you'll have to deal with it. Or, how many times have you had a portion of code you intentionally avoid because you know it's a mess? template.php anyone?
    * Pollution is difficult to understand. If you want to measure CO2 you would need a degree in physics or chemistry to understand how it is measured, and even then if you have a device you are only measuring parts per million in a given area--you need to know the volume of air and how homogeneous the reading is. Technical debt is hard to understand too--how do you predict if dependency injection is going to be a better fit than a service locator?
* slide: I am the lorax
    * So, where can we look for insights on pollution? The Lorax.
    * The Lorax is a story about a boy who visits the Once-ler who tells the story about how his town became so polluted. Back when the environment was healthy, the Once-ler had an idea for a new product called a Thneed. These Thneeds, which everyone needs, were made from Truffula trees which he began to cut down. Upon doing so, the Lorax appeared saying, "I am the Lorax. I speak for the trees. I speak for the trees, for the trees have no tongues." He proceeded to warn the Once-ler of the dangers of cutting down the trees. But, the Once-ler ignored him and began to bigger and bigger his business. The impact on the environment was devastating. The Brown Bar-ba-loots which fed on the Truffula trees became diseased with the Crummies because of gas and no food in their tummies, so the Lorax took them to find food. The smog from the Thneed factories gave the Swomee Swans sore throats, so they left too. The factories were dumping Gluppity Glup and Shloppity Shlop into the ponds where the Humming Fish live, making them unable to hum so they went away too. In the end, the Once-ler used up all the available resources and his business shut down. The Once-ler gives the boy a seed and tells him that if you plant it and grow a forest and protect it that the Lorax and all of his friends may come back.
    * INSERT TRANSITION STATEMENT TO Andrea's part on causes
TODO:

use these somewhere:

* I like how one person put it, "We have defeated one problem only to create another, and like the government of 1952 this one has yet to come to terms with the problem," [source](http://www.theguardian.com/uk_news/story/0,3604,850909,00.html)
* https://resources.sei.cmu.edu/asset_files/Webinar/2012_018_101_24291.pdf
