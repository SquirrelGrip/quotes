# Quotes
Quotes from the BigA

# Acronyms
* YAGNI...Yet
* DRY
* SOLID

# Sayings

## General
* If you going to use Lombok, consider using Kotlin instead.
* Tactical Solutions are always permanent.
* If you have a DevOps department, you have failed at DevOps.
* Premature Optimization (or Early Optimization).
* Make it work THEN make it better.
* Git will never hurt you. It will, however, confuse you, make you look stupid and often make you wish you never started using it, but it will never lose your changes.
* What does the error message say?
  * What does the actual message say?
* What is the difference between ++i, i++, i=+1 or i=i+1. They are all the same however no one can ever dispute i=i+1 meaning and clarity.
* Name your exceptions in a way that the name tells you what went wrong, for example, NameNotFoundException or ValueRequiredException.
* I work in a bank. We pride ourselve on being trusted with people's money. And when you deal with people's money, they don't want you losing it, even that 2 trillionth of a cent is important...Don't rely on double or float to store currency amounts.
* Don't send emails for every notification, eventually people will create an email rule to ignore them, only to have that 1 message in a 1000 that is interesting, be ignored.
* Don't optimise until you have 3 variants.
  * When you have 1 way of doing something, there is no variation. Hoard Code it.
  * When you have 2 variants, you can use an if/else statement.
  * You should consider a different pattern once you have 3 or more variants.
* It's better to throw back an unknown fish than to keep a poisonous one.
* Less Code === Saving Dolphines. 
  * Less Code -> Less Disk Space -> Less Space Used -> Less Waste -> Less Rubbish -> Less Pollution -> Less Dolphines being killed by Pollution

## IDE
* The IDE is your friend. Let it help you.
* Use the IDE Luke...Let go!
* Start using a Real IDE.
* The red squiggle is trying to get your attention. Please don't ignore!

## Kotlin
* Null Safety.
* Extension Functions.
* Operator Functions.
* Infix Function.
* Data classes. (Record classes are now in Java and Kotlin 1.5 takes advantage of them)
* Enum classes.
* Public by default.
* Final by default.
* companion objects
* objects

## Testing
* Stop putting the word test in front of your tests...the @Test should be enough to signify it is a test, within the classes that has the word Test at the end of it and is in the test part of your code. What more do you need to remind you you that testing is important.
* Use Date.now() + arbitrary amount to create a date in the future instead of hard coding a future date that will eventually come and your tests start breaking.
* Rocks over Mocks...Prefer the use of a real class over a mock.
* Mock what you do not own.

## Test Driven Development
* Red Green Refactor
* What is motivating you to make that change?
* Write a failing test, instead of writing a test that fails.
* Instead of trying think if the test is going fail, run it to see if it fails and why. (A habit of people new to TDD will often try to figure out what will happen during the test, which is built up from many years of not testing)
* Write the bare minimum to make that test pass. No more.

# Mocking
* Prefer real objects of mocks
** If you can use a real object over a mock, then do so. Mocks are pretend objects and in some cases they can pretend to do different things than the real ones. If the real object changes, then the behaviour it exhibits will change also. On the otherhand, mocks will continue to exhibit the same behaviour, even when the real object change.
* Mock what you don't own
** If you do not have full control over the interface, then this is a candidate for mocking. If you do own it, prefer to use the real. 
* Mock to improve performance and reliability
** In some cases the interface you are using can be slow or even be offline (eg. a database or web service). In this situation, a mock can give you better performance and stability.
* Mock for complex boundary conditions
** In situations where an exception is thrown, or a condition that is difficult to reproduce, a mock can be a great way to get the code in the right situation to get to those lines that need testing.
** For example, testing what to do when an SqlException is thrown, but that will only be thrown when the database goes down.

# Observations
* Reliability always trumps Performance...If you cannot finish the race, it doesn't really matter how fast you are at the beginning.
* When someone, who has never done TDD before, writes their first failing test and they run it and see it fail, they feel a sense of horror. A seasoned TDDer gets used to that feeling and embraces it.
* Does every exception need a message? Exception messages are there to provide more information to the user or because the exception itself is vague and/or ambiguous. The name (or type) of the Exception should be enought to determine what went wrong. If there are any further details that can be passed to the Exception should be. A useful message should be constructed from the information and that should be the only place the message is created.
  * Consider Internationalisation excercise to translate all error message...if all the possible messages are created inside the Exception itself.

# Ravings of a Mad Man
I sometimes need to just brain dump. Writing things down, just so I do not have to think about them and then it just clears my brain to think about other things. The following is some of those...

## The Structure of Software
There are certain tools that once developed, will never need to be redeveloped and will remain a fixture forever. These form the backbone of engineering. For example a screw driver, a hammer, a spanner. Once they exist these exist and a reused over and over again. However there is always variants of these tools that fit different circumstances and the tools themselves are not a one size fits all and each tool comes with many different shapes and sizes.

Software it is the same. There are many different tools, that do the same thing. These tools are often associated with the operating system and have dirrent options to accomodate each use case. For example, file system tools, network tools, calculators, string processing tools, etc.

Then there are the next layer of tools that use the underlying tools to meet a core business component. For example employee directory, client database, email, shared drives, etc. These are often tools built on top of the operating system that form the backbone of the business. 

Then there are set of tools to manipulate data. Word Processing, Spreadsheet, Prensentation Tools, etc. which form the basis of an Office Toolset. These are generic and many already exist.

Then there are the specialised systems. The Systems that form the differentiator for the business. These are the tools that give the business their competitive advantage. Having the right tool for the job can make the users life much easier and leverage the company. These systems are highly tuned, complex and fragile systems. Often draw upon all of the layers and can be quite disruptive. 

The next level is the intelligent systems. The Systems that aid in decision making and often guide the user. These are still emerging, but a lot already exist and are used daily but everyone. And they will get better. 

## Development and Maintenance
There is a difference between a tool and a machine. Tools do not break and if they do we simply replace them. It is not worth fixing and maintaining a tool as they are usually cheap and expendable. 

A machine, however, needs to maintained and constantly tinkered with, upgraded, fixed and monitored. Car need fuel, they need new tires, they need brakes replaced and oil changed, and every now and then thy need to be overhauled and have major repairs. 

Machine are always being built that are better than their predecessor. New ideas emerge and constant improvements are taking place. 

The more important the machine, the more investment you put into it and the more it is maintained. 

## Rocket Ship Model
When it comes to software, it is often considered a tool. Which means that once the tool is built, we deploy it and the tool is launched, with little to no improvements and minimal maintenance. This can often be seen by project teams that get budget to build something, and then have the tool deployed and the team is rolled off to build another tool.

Rockets are perfecet example of this. Once the rocket is launched, we can no longer reach the rocket, change it, upgrade it, etc. We simply launch the rocket and let it go. Sometimes they even explode after launch, sometimes spectacularly.

## Car Racing Model
Machines are maintained. If you have a racing car, you want it to be fast and reliable. The difference between success and failure is often put down to skill of the team and the engine itself. A good car, does not need a great driver, but a great driver can make a poor car do better. We see this all the time in car racing. 
The key to success in car racing is not speed, but reliability. If you car is not able to finish a race, there is no chance of winning. So at a very minimum, you need to have a reliable machine. Without that, it does not matter how fast the engine can go, if you only complete a few races. There are so many factors just to be reliable.
