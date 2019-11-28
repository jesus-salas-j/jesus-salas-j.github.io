<br/><br/>
## Introduction

I have based this article on the Vaughn Vernon book titled "Implementing Domain Driven Design". At the time of writing this
article I have to recognize that I am not an expert in DDD so it is probably that this content doesn't answer all your 
questions about Strategic DDD although I hope I help you to understand this approach. It is a complex subject and I have needed to read several times some of the chapters in the book 
to understand the large amount of concepts that are explained there. Many of the concepts are quite abstract and although the 
book contains some examples it has been difficult for me to think how these concepts could fit in the projects I am currenly 
working on.<br/><br/>
Nevertheless I am going to do my best in explaining the main concepts in the simplest possible way and provide some more examples that 
those provided by the book so you can achieve a better understanding.<br/><br/>
Before reading the Vernon's book I had read lots of articles in internet about DDD, forum discussions, youtube videos, and 
more. Until I read the book I didn't quite understand what DDD was, the information I found sometimes was confusing 
and other times contradictory. I understood it as a one more architecture, a kind of extended hexagonal architecture, but 
as we are going to see next it is much more than that.


<br/><br/><br/>
## What does DDD mean

Domain Driven Design. The domain, though later I will explain it in detail, basically is the business itself, so when we 
talk about DDD we are talking about software design guided by the business or the business idea.
DDD talks about both technical implementations and business strategy. It doesn't only talk about architecture but also 
about company philosophy, a way to organize and a way to do. It is oriented to work with small, agile and autonomous teams.
Teams must be permanently connected with the business experts, as well as very involved in obtaining and discovering 
knowledge about the business.<br/><br/>
Then DDD involves the entire organization, if the company is not aligned with this approach it cannot be applied. In our 
day to day, as good professionals we are, we try to write code that has no errors, we apply best practices, design patterns 
when they make sense, we implement new features doing pair programming, we add unit, integration and behaviour tests in 
our projects in order to guarantee the quality of our work... Nevertheless this high quality code couldn't be reflecting 
faithfully the idea for what it was created. If this is so it will not be considered a good solution since it will not be useful. A high quality software besides being very well crafted must reflect the business idea for what it was ordered.<br/><br/>
On the other hand implementing DDD is expensive. Implies expending lots of resources and efforts in building projects 
where this approach is used. It has not been thought for developing all systems using this approach, but for developing 
those systems that are the business core, those systems that are expected to obtain more benefit, in the end those who are 
the heart of the business, and build a very high quality software for them.

<br/><br/><br/>
## DDD in the company I am currenly working

In the company I am now working in a conscious or unconscious way we are using some DDD practices. We have relatively 
small teams oriented to specific missions and at least a member of every team is a business expert, the Product Owner.
This situation makes easier to the team to be continually connected with the business. Other members of the team 
must not take for granted that the product owner is going to be able to answer all the questions about the business, he or she 
simply can't know everything. It is a responability of the entire team to understand and discover the business. Obviously 
the product owner will do most of this task since he is the nexus between the team and the stakeholders.
Anyway this not frees the rest of the team members to disregard or not wanting to understand and discover the business. There is no product owner, no manager, no CEO, anybody that knows absolutely everything about the business. Everyone has to 
contribute to discover the business through the dialogue, discussions and so on.<br/><br/>
Moreover everyone of us apply some things of DDD in our developments. As we have product owners in our teams, we 
are continuosly talking with them using the same language that they use, the business language. This language is the one 
the business experts use between them and with the stakeholders, so we use it in our code. We name classes and 
methods in our code using this language in a natural way. In fact there should not be translations between the natural 
business language and the language used in the code we write. Even so, though we make use of some things that are aligned 
with DDD, there is a lot of work to do yet.

<br/><br/><br/>
## Strategic DDD

In this article I am going to explain only one part of DDD, what is called strategic DDD. This part is explained in the 
three first chapters of Vernon's book. This part of DDD neither talk about code, nor about message brokers, nor about 
databases, nor about events... It talks exclusively about business.<br/><br/>
Strategic DDD explains how to carry out a strategy for building software systems that are closer to business ideas. Many times 
developers are very far from the business experts, or these experts try to convey an idea to the developer 
teams but then the software that is built is quite different than the original idea and it can even lose the essence 
of that idea. Moreover many developer teams tend to build software systems that are difficult to change and in a world 
that evolves very fast and it is continuosly changing these systems doesn't have the necessary flexibility to allow 
fast changes and adaptation. The DDD approach is based in bringing near the developers and the business experts so they 
work together. This way the communication flows in a natural way and it is more likely that the software that is 
being built ends up being very much better aligned with the original idea, the software that business experts would have built if they were developers.

<br/><br/><br/>
## A brief explanation of Tactical DDD

Explaining Tactical DDD is not the aim of this article, it is a very extensive topic so I will simply mention it in a very briefly way.<br/><br/>
Tactical DDD is related to code, patterns and architecture to build high quality software systems. It explains how we can craft small and specific models for a system that will be built for a specific company's area. It details patterns and best practices to build these models in a smart way so they end reflecting faithfully the business. The basic idea is to run away from bad practices and anemic models. Moreover these models must be easy to adapt to new scenarios and business changes and easy to maintain. With these excellently well crafted models later we will be able to build high quality software systems around them.<br/><br/>
This part of DDD also explains how to integrate these models and build efficient communication methods between them in order to be able to build, evolve and maintain large high quality software systems.<br/><br/>
It is very important to use DDD to model a complex domain in the simplest way possible, never use DDD to make your solution more complex.

<br/><br/><br/>
## Main concepts

### Domain

It refers to the entire business itself, the whole organization, its employees and processes. It is the what and the how of doing things in the company.

### Subdomain 

It is a single part of the business. In many articles and books, and in the developers community you will find that subdomains are commonly called domains. It is accepted talking about subdomains as domains, Vernon himself accepts this naming alghough he refers to them as subdomains in the entire book. Only you need to bear in mind this double meaning when you read about Strategic DDD and know the the reading's context and understand if it is refering to the domain meaning or subdomain meaning where the term domain is used.

### Core domain

It is the most important subdomain for the business, its essence. The company will put focus on it, it is of primary importance for the business. Most and best resources, humans and technicals, will be used to build and maintain necessary systems under the scope of this subdomain. It is the part where things need to be done with the highest quality. The core domain can change over time. The business is continuosly changing so in few months or years the main scope of the business can change, so it will change also which is the new core domain.

### Generic and supporting subdomains

A generic subdomain is that one that it is required for the whole business but not as important as the Core Domain. It can be purchased to a third party instead of being developed by the company.  
A supporting subdomain is that one that is essential for the business but not the most important, so it neither needs the best efforts nor the best quality.

### Ubiquous language

It is a linguistic boundary and alignment between the team and the business experts. It is not an universal language and it is only valid inside its context.  
A single word can have several differents meanings depending on what context is being used. We need to know what context are we refering when using a specific word.  
For example in a company the customer concept can have different meanings depending of the department where the word is used. In a department that maintains for example a backoffice where customers can manage their purchased products, a customer will be someone that logs in the backoffice and works with it. On the other hand in the billing department quite surely a customer is someone to bill. So a single customer for the billing department could be related with several customers for the backoffice maintainer department because it could exists a single payer for several backoffice users (for example commercials of a business). The opposite scenario could also exist. A business that haves a single backoffice user but he wants its billings to be split in several billings with different names, maybe splitted by geographical business areas.

### Bounded context

Is is one of the most missunderstood concepts in DDD. You will find many reading that explain it in different ways and as it is an abstract term it is difficult to understand so it is easy to make a wrong idea of what it exactly means.  
It is a conceptual boundary when a model can be applied, it provides a context for a specific ubiquous language that is spoken by the team and expressed in its carefully designed software model.  
It is not necessary that a subdomain has a single bounded context, although it is the desired scenario. 

### Domain model

It is a model used in a single bounded context. It must be never a huge model for the whole business, it must be the opposite, a relative small and specific well crafted model only useful for a single bounded context. It needs to reflect perfectly the concepts and behaviours provided by the bounded context in where it will be applied. This generalism leads in a natural way to build a too complex model since it is required to support all scenarios. This complex model leads to difficulties to scale our systems since they are too big.

<br/><br/><br/>
## Study cases

### Scenario: Single subdomain with multiple bounded contexts

The ideal scenario would be to achieve a relation 1:1 between subdomains and bounded contexts. But this is not always possible since in a company we have to deal with legacy systems, third party tools, customized processes and tens of different scenarios. Moreover a single subdomain with multiple bounded contexts it not necessary a bad situation, it depends of the business.<br/><br/>
Anyway this scenario can lead us in many cases to undesirable situations as the need of maintaining duplicated processes, and maybe duplicated software systems that are performing things that are conceptually the same but resolved or handled in different ways by different teams or departments. Also this scenario can lead to have a confusing language across the company, concepts that although represent the same idea are named different by different teams and departments. This situation difficulties communication through the company.

### Scenario: Single bounded context for several subdomains

This scenario leads our systems to be too generalists, having huge and complex models that must be applied and must fit in many cases. This situation makes software systems difficult to scale and evolve. It also limits the team's autonomy and creates too many dependencies, so the systems that are in this scenario are less flexible to change.
It is the opposite of the previous scenario, same vocabulary is being used for different things and employees are not able no differenciate in which context they are using each term.







 

 
