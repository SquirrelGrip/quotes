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
* If needs a DevOps department, you have failed at DevOps.
* Premature Optimization (or Early Optimization).
* Make it work THEN make it better.
* Git will never hurt you. It will, however, confuse you, make you look stupid and often make you wish you never started using it, but it will never lose your changes.
* What does the error message say?
  * What does the actual message say?
* What is the difference between ++i, i++, i=+1 or i=i+1. They are all the same however no one will ever dispute i=i+1 meaning as it is the clearest.
* Name your exceptions in a way that the name tells you what went wrong, for example, NameNotFoundException or ValueRequiredException.
* I work in a bank. We pride ourselve on being trusted with people's money. And when you deal with people's money, they don't want you losing it, even that 2 trillionth of a cent is important...Don't rely on double or float to store currency amounts.
* Don't send emails for every notification, eventually people will create an email rule to ignore them, only to have that 1 message in a 1000 that is interesting, be ignored.
* Don't optimise until you have 3 variants. When you have 1, there is no variation, when you have 2 variants, you can use an if/else statement. You should consider a different pattern once you have 3 or more variants.
* It's better to throw back an unknown fish than to keep a poisonous one.
* Less Code === Saving Dolphines. 
  * Less Code -> Less Disk Space -> Less Space Used -> Less Waste -> Less Rubbish -> Less Pollution -> Less Dolphines being killed by Pollution

## IDE
* The IDE is your friend, let it help you.
* Use the IDE Luke...Let go!
* Start using a Real IDE.
* The red squiggle is trying to get your attention. Please don't ignore!

## Kotlin
* Null Safety.
* Extension Functions.
* Operator Functions.
* Data classes. (Record classes are now in Java and Kotlin 1.5 takes advantage of them)
* Public by default.
* Final by default.
* companion objects

## Testing
* Stop putting the word test in front of your tests...the @Test should be enough to signify it is a test.
* Use Date.now() + arbitrary amount to create a date in the future instead of hard coding a future date that will eventually come and your tests start breaking.
* Rocks over Mocks...Prefer the use of a real class over a mock.

## Test Driven Development
* Red Green Refactor
* What is motivating you to make that change.
* Write a failing test, instead of writing a test that fails.
* Instead of trying think if the test is going fail, run it to see if it fails and why.
* Write the bare minimum to make that test pass.

# Observations
* Reliability always trumps Performance...If you cannot finish the race, it doesn't really matter how fast you are.
* When someone, who has never done TDD before, writes their first failing test and they run it and see it fail, they feel a sense of horror. A seasoned TDDer gets used to that feeling and embraces it.
* Does every exception need a message? Exception messages are there to provide more information to the user or because the exception itself is vague and/or ambiguous. The name (or type) of the Exception should be enought to determine what went wrong. If there are any further details that can be passed to the Exception should be. A useful message should be constructed from the information and that should be the only place the message is created.
** Consider Internationalisation excercise to translate all error message...if all the possible messages are created inside the Exception itself.

