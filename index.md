## Introduction

I have based this article in the Vaughn Vernon book titled "Implementing Domain Driven Design". At the time of writing this
article I have to recognize that I am not an expert in DDD so it is probably that this content doesn't answer all your 
questions about Strategic DDD. It is a complex subject and I have needed to read several times some of the chapters in the book 
to understand the large amount of concepts that are explained there. Many of the concepts are quite abstract and although the 
book contains some examples it has been difficult for me to think how these concepts could fit in the projects I am currenly 
working on.  
Nevertheless I am going to do my best in explaining the main concepts in a simple way and provide some more examples that 
those provided by the book so you can achieve a better understanding.  
Before reading the Vernon's book I had read lots of articles in internet about DDD, forum discussions, youtube videos, and 
more. Until I read the book I didn't quite understand exactly what DDD was, the information I found sometimes was confusing 
and other times contradictory. I understood it as a one more architecture, a kind of extended hexagonal architecture, but 
as we are going to see next it is much more than that.

## Strategic DDD

In this article I am going to explain only one part of DDD, what is called strategic DDD. This part is explained in the 
three first chapters of Vernon's book. This part of DDD neither talk about code, nor about message brokers, nor about 
databases, nor about events... It talks exclusively about business.  
Strategic DDD explains how to carry out a strategy for building software systems that are closer to business ideas. Many times 
developers are or have been very far from the business experts, or these experts try to convey an idea to the developer 
teams but then the software that it is built is quite different than the original idea and it can even lose the essence 
of that idea. Moreover many developer teams tend to build software systems that are difficult to change and in a world 
that evolves very fast and it is continuosly changing these systems doesn't have the necessary flexibility to allow 
fast changes and adaptation. The DDD approach is based in bring near the developers and the business experts so they 
work together. This way the communication flows in a natural way and it is more likely that the software that it is 
being built ends up being very much better aligned with the original idea, the idea that would have been built the 
business experts if they were developers.


## What does DDD exactly means

Domain Driven Design. The domain, though later I will explain it in detail, basically is the business itself, so when we 
talk about DDD we are talking about software design guided by the business or the business idea.
DDD talks about both technical implementations and business strategy. It doesn't only talks about architecture but also 
about company philosophy, a way to organize and a way to do. It is oriented to work with small, agile and autonomous teams.
Teams must be permanently connected with the business experts, as well as very involved in obtaining and discovering 
knowledge about the business.  
DDD involves then all the organization, if the company it is not aligned with this approach DDD cannot be applied. In our 
day to day, as good professionals we are, we try to write code that has no errors, we apply best practices, design patterns 
when they make sense, we implement new features doing pair programming, we add unit, integration and behaviour tests in 
our projects in order to guarantee the quality of our work... Nevertheless this high quality code can not being reflecting 
faithfully the idea for what it was created. If this is so it will not be considered a good solution since it will not be useful. A high quality software besides being very well crafted must reflect the business idea for what it was ordered.  
On the other hand implementing DDD is expensive. Implies expending lots of resources and efforts in building the projects 
where this approach is used. It has not being thought for developing all systems with this approach, but for developing 
those systems that are the business core, those systems that are expected to obtain more benefit, in the end those who are 
the heart of the business, and build a very high quality software for them.


## DDD in the company I am currenly working

In the company I am now working in a conscious or unconscious way we are using some DDD practices. We have more or less 
small teams oriented to specific missions and at least a member of every team is a business expert, the Product Owner.
This situation makes easier to the team to be continually connected with the business. The other members of the team 
must not take for granted that the product owner to be able to answer all the questions about the business, he or she 
simply can't know everything. It is a responability of the entire team to understand and discover the business. Obviously 
the product owner will do most of this task since he is the nexus between the rest of the tem and the stakeholders.
Anyway this not frees the other team members to disregard or not want to understand and discover the business. It does not 
exists no product owner, no manager, no CEO, nobody that knows absolutely all things about the business. Everyone has to 
contribute to discover the business through the dialogue, discussions, debates and so on.  
On the other hand all of us also apply some things of DDD in our developments. As we have product owners in our teams, we 
are continuosly talking with them using the same language that they use, the business language. This language is the one 
the business experts use between them and with the stakeholders, and we use them in our code. We name the classes and 
methods in our code using this language in a natural way. In fact there would not be translations between the natural 
business language and the language used in the code we write. Even so, though we make use of some things that are aligned 
with DDD, there is a lot of work to do yet.
 

 
