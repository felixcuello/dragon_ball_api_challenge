# Dragon Ball API

## Introduction

Congratulations!, you have been selected to develop a new API to keep track of the Dragon Ball
fights.

In a dystopian world characters and villains are fighting each other in epic battles that
can last for a very long time (for the sake of simplicity in this API theyh are going to last just seconds).

You don't need to build a UI for this, because we already selected a great UI/UX
person that is going to built that part.

Instead, you have to create a robust API that they can use to perform operations on
the backend.

You have a week for this task because we need to present this to our stake hodlers.

_Please fork this repository to your personal github and create a PR on your github for code review_


## Challenge

The Dragon Ball API it' simple we need to store Characters and Fights where the fights between the
characers are stored.

A character is composed by just a few fields like "name", "power\_level" (which is an integer).

A villain, which is composed by just a few fields too like "name" and "power\_level" (which is an integer).

We need to perform CRUD operations for characters and villains in our API.

The API must send and receive JSON files.


## Constraints

Even though this is an MVP we have some constraints about the system that were listed as
requirements for our MVP.

First, any character can fight any villain, and we need to keep track of WHEN the fight started.

The second request is a request from our stakeholders that is that all the fights last 2 times the
minimum power level of each contender. For example if a character has a power of 10
and a villain has a power of 7, the fight will last 14 seconds (because the minimum level between
the contenders is 7, which multiplied by 2 is 14).

Also if both characters have the same level it's a draw.


You only need to have the following restrictions:

- All fights start at time 0, so after 2 seconds, each character loses 1 power level.
- When a fight starts, it can't be stopped.
- It takes 2 seconds times the min(power character, power villain) seconds to end the battle.

Besides the endpoints to read information about the character and the villain, I need an endpoint to
check what's the status of the fight (for example: GET /battle/1 should tell me if it's an ongoing
battle or if it finished already and who won or if it was a draw.


## Bonus points

- If you add some business logic to the tests (i.e. a character or villain can't fight two battles at the same time)

- If you build the system inside docker containers.

- If you add tests to the application

- If you handle errors gracefully

- If you check the JSON schemas

- If only authenticated users can create, update, delete, or change the characters or villains.
