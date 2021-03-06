# CQRS & Event sourcing

## What we will cover

- What is CQRS and when can it be useful?
- What is Event sourcing and how can it help in a MicroService architecture?

## Notes

Question:

>Thanks a log sharing his video was very useful. Can you make some video implementing CQRS, Event sourcing and RabbitMQ with microservices please. I read a lot of DDD CQRS, but never seen some real project example?

CQRS (Command Query Responsibility Segregation) is a application architecture.
CQRS is best used in situations when you have a disproportionate amount of read and writes.

Event sourcing is about creating a View instead of a Model. The View is just like a normal Model but it is computed by applying Events to it.

You use events such as "CreateUser", "UpdateUsername" and "DeleteUser" to mutate the View.
Each event is stored like a log. This let's us replay our events to recreate the View.
This will let you see what the state of the View was at a given point in time. It also let's you track all the updates to the View that has happened.

